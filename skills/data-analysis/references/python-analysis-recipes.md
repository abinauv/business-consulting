# Python Analysis Recipes for Consulting

Ready-to-use Python code snippets for common consulting analytical tasks. All recipes use pandas, numpy, and matplotlib/seaborn with a **consulting-grade style theme** applied by default.

---

## 0. Consulting Style Theme (Apply First)

Import this at the top of every analysis script. It sets a McKinsey/BCG-grade visual style across all charts automatically.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.ticker as mticker
import matplotlib.patches as mpatches
import seaborn as sns
from matplotlib.colors import LinearSegmentedColormap

# ── Consulting Color Palette ──────────────────────────────────────────────────
COLORS = {
    "primary":    "#2F5496",   # Dark blue — main data, totals
    "secondary":  "#4472C4",   # Medium blue — secondary data
    "accent":     "#00B0F0",   # Teal — highlights, callouts
    "positive":   "#548235",   # Forest green — positive values, growth
    "negative":   "#C00000",   # Deep red — negative values, decline
    "warning":    "#ED7D31",   # Orange — warnings, thresholds
    "neutral":    "#A6A6A6",   # Gray — context, de-emphasized data
    "light_gray": "#D9D9D9",   # Light gray — gridlines, backgrounds
    "bg":         "#FFFFFF",   # White — chart background
    "text":       "#333333",   # Near-black — all text
}

# Ordered palette for multi-series charts (up to 8 series)
PALETTE = [
    COLORS["primary"], COLORS["accent"], COLORS["warning"],
    COLORS["positive"], "#7030A0", "#BF8F00", COLORS["secondary"], COLORS["neutral"]
]

# ── Apply Global Style ────────────────────────────────────────────────────────
plt.rcParams.update({
    # Figure
    "figure.figsize":       (12, 6.5),
    "figure.dpi":           150,
    "figure.facecolor":     COLORS["bg"],
    "figure.edgecolor":     "none",
    # Font
    "font.family":          "sans-serif",
    "font.sans-serif":      ["Calibri", "Arial", "Helvetica Neue", "DejaVu Sans"],
    "font.size":            11,
    # Axes
    "axes.facecolor":       COLORS["bg"],
    "axes.edgecolor":       COLORS["light_gray"],
    "axes.linewidth":       0.6,
    "axes.titlesize":       14,
    "axes.titleweight":     "bold",
    "axes.titlepad":        16,
    "axes.titlecolor":      COLORS["text"],
    "axes.labelsize":       11,
    "axes.labelcolor":      COLORS["text"],
    "axes.labelpad":        8,
    "axes.prop_cycle":      plt.cycler(color=PALETTE),
    "axes.spines.top":      False,
    "axes.spines.right":    False,
    # Grid
    "axes.grid":            True,
    "axes.grid.axis":       "y",
    "grid.color":           COLORS["light_gray"],
    "grid.linewidth":       0.5,
    "grid.alpha":           0.7,
    # Ticks
    "xtick.color":          COLORS["text"],
    "ytick.color":          COLORS["text"],
    "xtick.labelsize":      10,
    "ytick.labelsize":      10,
    "xtick.major.size":     0,
    "ytick.major.size":     0,
    "xtick.direction":      "out",
    "ytick.direction":      "out",
    # Legend
    "legend.fontsize":      10,
    "legend.frameon":       False,
    "legend.loc":           "upper right",
    # Lines
    "lines.linewidth":      2.2,
    "lines.markersize":     6,
    # Bars
    "patch.edgecolor":      "white",
    "patch.linewidth":      0.8,
    # Savefig
    "savefig.dpi":          200,
    "savefig.bbox":         "tight",
    "savefig.pad_inches":   0.3,
    "savefig.facecolor":    COLORS["bg"],
})

sns.set_palette(PALETTE)

# ── Helper Functions ──────────────────────────────────────────────────────────

def fmt_dollars(x, pos=None):
    """Format axis values as $XXM or $X.XB."""
    if abs(x) >= 1e9:
        return f"${x/1e9:.1f}B"
    elif abs(x) >= 1e6:
        return f"${x/1e6:.0f}M"
    elif abs(x) >= 1e3:
        return f"${x/1e3:.0f}K"
    return f"${x:.0f}"

def fmt_pct(x, pos=None):
    """Format axis values as XX%."""
    return f"{x:.0f}%"

def fmt_number(x, pos=None):
    """Format axis values with K/M suffixes."""
    if abs(x) >= 1e6:
        return f"{x/1e6:.1f}M"
    elif abs(x) >= 1e3:
        return f"{x/1e3:.0f}K"
    return f"{x:.0f}"

def add_source_note(ax, source_text, year=None):
    """Add a consulting-style source note to bottom-left of chart."""
    label = f"Source: {source_text}"
    if year:
        label += f", {year}"
    ax.annotate(label, xy=(0, 0), xycoords="figure fraction",
                xytext=(12, 8), textcoords="offset points",
                fontsize=8, color=COLORS["neutral"], style="italic")

def add_annotation(ax, x, y, text, color=None):
    """Add a callout annotation to a specific point."""
    ax.annotate(text, xy=(x, y), fontsize=9, fontweight="bold",
                color=color or COLORS["text"],
                ha="center", va="bottom",
                xytext=(0, 8), textcoords="offset points")

def save_chart(fig, filename):
    """Save chart with consulting-quality settings."""
    fig.savefig(filename, dpi=200, bbox_inches="tight",
                facecolor=COLORS["bg"], edgecolor="none", pad_inches=0.3)
    print(f"Chart saved: {filename}")
```

---

## 1. Data Loading and Cleaning

```python
# Load data
df = pd.read_csv("data.csv")  # or pd.read_excel("data.xlsx", sheet_name="Sheet1")

# Quick overview
print(f"Shape: {df.shape[0]:,} rows × {df.shape[1]} columns")
print(f"\nColumn types:\n{df.dtypes.value_counts()}")
print(f"\nMissing values:\n{df.isnull().sum()[df.isnull().sum() > 0]}")

# Handle missing values
df["revenue"].fillna(df["revenue"].median(), inplace=True)
df.dropna(subset=["customer_id"], inplace=True)

# Detect outliers using IQR
def flag_outliers(series):
    Q1, Q3 = series.quantile(0.25), series.quantile(0.75)
    IQR = Q3 - Q1
    return (series < Q1 - 1.5 * IQR) | (series > Q3 + 1.5 * IQR)

df["revenue_outlier"] = flag_outliers(df["revenue"])

# Standardize columns
df.columns = df.columns.str.strip().str.lower().str.replace(" ", "_")

# Parse dates
df["date"] = pd.to_datetime(df["date"], format="%Y-%m-%d")
df["year"] = df["date"].dt.year
df["month"] = df["date"].dt.month
df["quarter"] = df["date"].dt.quarter
```

---

## 2. Pareto Analysis (80/20)

```python
customer_revenue = df.groupby("customer_name")["revenue"].sum().sort_values(ascending=False)
cumulative_pct = customer_revenue.cumsum() / customer_revenue.sum() * 100
n_80 = (cumulative_pct <= 80).sum()

fig, ax1 = plt.subplots()
# Bars — primary blue, top contributors highlighted
bar_colors = [COLORS["primary"] if i < n_80 else COLORS["light_gray"]
              for i in range(len(customer_revenue))]
ax1.bar(range(len(customer_revenue)), customer_revenue.values, color=bar_colors, width=0.8)
ax1.set_ylabel("Revenue ($)")
ax1.set_xlabel(f"Customers (ranked by revenue, n={len(customer_revenue):,})")
ax1.yaxis.set_major_formatter(mticker.FuncFormatter(fmt_dollars))

# Cumulative line — orange accent
ax2 = ax1.twinx()
ax2.plot(range(len(cumulative_pct)), cumulative_pct.values,
         color=COLORS["warning"], linewidth=2.5, zorder=5)
ax2.axhline(y=80, color=COLORS["negative"], linestyle="--", linewidth=1, alpha=0.6)
ax2.set_ylabel("Cumulative %")
ax2.yaxis.set_major_formatter(mticker.FuncFormatter(fmt_pct))
ax2.spines["right"].set_visible(True)
ax2.spines["right"].set_color(COLORS["light_gray"])

# Annotation at 80% cutoff
ax2.annotate(f"Top {n_80} customers ({n_80/len(customer_revenue)*100:.0f}%)\ndrive 80% of revenue",
             xy=(n_80, 80), fontsize=10, fontweight="bold", color=COLORS["negative"],
             ha="left", va="bottom", xytext=(10, 10), textcoords="offset points",
             arrowprops=dict(arrowstyle="->", color=COLORS["negative"], lw=1.2))

ax1.set_title(f"Top {n_80} customers drive 80% of total revenue — high concentration risk")
add_source_note(ax1, "Internal data")
save_chart(fig, "pareto_analysis.png")
```

---

## 3. Cohort Analysis (Retention Heatmap)

```python
df["order_date"] = pd.to_datetime(df["order_date"])
df["order_month"] = df["order_date"].dt.to_period("M")

cohort = df.groupby("customer_id")["order_month"].min().rename("cohort")
df = df.merge(cohort, on="customer_id")
df["period_number"] = (df["order_month"] - df["cohort"]).apply(lambda x: x.n)

cohort_data = df.groupby(["cohort", "period_number"])["customer_id"].nunique().reset_index()
cohort_pivot = cohort_data.pivot(index="cohort", columns="period_number", values="customer_id")
cohort_sizes = cohort_pivot[0]
retention = cohort_pivot.divide(cohort_sizes, axis=0) * 100

# Custom blue-to-white colormap (consulting-style)
cmap_consulting = LinearSegmentedColormap.from_list(
    "consulting", ["#FFFFFF", "#D6E4F0", "#9DC3E6", "#4472C4", "#2F5496"])

fig, ax = plt.subplots(figsize=(14, 8))
sns.heatmap(retention, annot=True, fmt=".0f", cmap=cmap_consulting,
            vmin=0, vmax=100, linewidths=1, linecolor="white",
            cbar_kws={"label": "Retention %", "shrink": 0.8},
            annot_kws={"fontsize": 9, "fontweight": "bold"}, ax=ax)

ax.set_title("Newer cohorts retain better — product improvements are working")
ax.set_xlabel("Months Since First Purchase", fontsize=11)
ax.set_ylabel("Cohort (First Purchase Month)", fontsize=11)
ax.tick_params(axis="y", rotation=0)

add_source_note(ax, "Internal transaction data")
save_chart(fig, "cohort_retention.png")
```

---

## 4. Waterfall / Bridge Chart

```python
def waterfall_chart(categories, values, title, subtitle=None, show_connectors=True):
    """Consulting-grade waterfall chart with connector lines and smart labeling."""
    n = len(values)
    cumulative = np.zeros(n)
    cumulative[0] = values[0]
    for i in range(1, n):
        cumulative[i] = values[i] if i == n - 1 else cumulative[i-1] + values[i]

    bottoms = np.zeros(n)
    for i in range(1, n - 1):
        bottoms[i] = cumulative[i-1] if values[i] >= 0 else cumulative[i]
    # Last bar starts from zero (it's a total)

    colors = []
    for i, v in enumerate(values):
        if i == 0 or i == n - 1:
            colors.append(COLORS["primary"])
        elif v >= 0:
            colors.append(COLORS["positive"])
        else:
            colors.append(COLORS["negative"])

    fig, ax = plt.subplots()
    bars = ax.bar(categories, [abs(v) for v in values], bottom=bottoms,
                  color=colors, width=0.55, zorder=3)

    # Connector lines between bars
    if show_connectors:
        for i in range(n - 2):
            y = cumulative[i]
            ax.plot([i + 0.275, i + 0.725], [y, y],
                    color=COLORS["neutral"], linewidth=0.8, linestyle="--", zorder=2)

    # Value labels
    for i, (bar, val) in enumerate(zip(bars, values)):
        y_pos = bar.get_y() + bar.get_height()
        offset = max(abs(v) for v in values) * 0.015

        if i == 0 or i == n - 1:
            label = fmt_dollars(val)
        elif val >= 0:
            label = f"+{fmt_dollars(val)}"
        else:
            label = f"–{fmt_dollars(abs(val))}"
            y_pos = bar.get_y() - offset * 0.5

        ax.text(bar.get_x() + bar.get_width() / 2, y_pos + offset, label,
                ha="center", va="bottom", fontweight="bold", fontsize=10,
                color=colors[i] if i not in [0, n-1] else COLORS["text"])

    ax.yaxis.set_major_formatter(mticker.FuncFormatter(fmt_dollars))
    ax.set_title(title)
    if subtitle:
        ax.text(0.0, 1.02, subtitle, transform=ax.transAxes,
                fontsize=10, color=COLORS["neutral"], style="italic")

    ax.set_axisbelow(True)
    plt.xticks(rotation=25, ha="right")
    add_source_note(ax, "Internal data")
    return fig

# Example
categories = ["FY2024", "Volume", "Pricing", "New Products", "Churn", "FX Impact", "FY2025"]
values = np.array([50e6, 5e6, 3e6, 2e6, -4e6, -1e6, 55e6])
fig = waterfall_chart(categories, values,
    title="Revenue grew $5M driven by volume and pricing, partially offset by churn",
    subtitle="FY2024 → FY2025 revenue bridge ($M)")
save_chart(fig, "waterfall_bridge.png")
```

---

## 5. Tornado Chart (Sensitivity)

```python
def tornado_chart(assumptions, low_values, high_values, base_value, title,
                  value_label="NPV ($M)"):
    """Consulting-grade tornado chart for sensitivity analysis."""
    ranges = [h - l for h, l in zip(high_values, low_values)]
    sorted_idx = np.argsort(ranges)  # Smallest to largest (plot bottom to top)

    assumptions = [assumptions[i] for i in sorted_idx]
    low_values = [low_values[i] for i in sorted_idx]
    high_values = [high_values[i] for i in sorted_idx]

    fig, ax = plt.subplots(figsize=(12, max(5, len(assumptions) * 0.7 + 1.5)))
    y_pos = range(len(assumptions))

    # Low bars (left of base)
    low_widths = [l - base_value for l in low_values]
    ax.barh(y_pos, low_widths, left=base_value, color=COLORS["negative"],
            height=0.55, zorder=3, label="Downside")

    # High bars (right of base)
    high_widths = [h - base_value for h in high_values]
    ax.barh(y_pos, high_widths, left=base_value, color=COLORS["positive"],
            height=0.55, zorder=3, label="Upside")

    # Base line
    ax.axvline(x=base_value, color=COLORS["text"], linewidth=1.2, zorder=4)
    ax.text(base_value, len(assumptions) + 0.3, f"Base: {fmt_dollars(base_value*1e6)}",
            ha="center", va="bottom", fontweight="bold", fontsize=10, color=COLORS["text"])

    # Value labels on bars
    for i in range(len(assumptions)):
        ax.text(low_values[i] - 0.3, i, fmt_dollars(low_values[i]*1e6),
                ha="right", va="center", fontsize=9, color=COLORS["negative"], fontweight="bold")
        ax.text(high_values[i] + 0.3, i, fmt_dollars(high_values[i]*1e6),
                ha="left", va="center", fontsize=9, color=COLORS["positive"], fontweight="bold")

    ax.set_yticks(y_pos)
    ax.set_yticklabels(assumptions, fontsize=11)
    ax.set_xlabel(value_label)
    ax.set_title(title)
    ax.legend(loc="lower right")
    ax.grid(axis="x", alpha=0.3)
    ax.grid(axis="y", visible=False)

    add_source_note(ax, "Sensitivity analysis, ±20% assumption variation")
    return fig

# Example
assumptions = ["Revenue growth rate", "Gross margin", "Discount rate (WACC)",
               "Terminal growth", "Capex intensity", "Customer churn"]
low = [38, 42, 52, 44, 46, 40]   # NPV in $M at low assumption
high = [62, 58, 48, 56, 54, 60]  # NPV in $M at high assumption
base = 50  # Base case NPV in $M

fig = tornado_chart(assumptions, low, high, base,
    title="Revenue growth and gross margin are the two most impactful assumptions")
save_chart(fig, "tornado_sensitivity.png")
```

---

## 6. Correlation Heatmap

```python
numeric_cols = ["revenue", "units", "price", "marketing_spend", "headcount", "satisfaction_score"]
corr_matrix = df[numeric_cols].corr()

# Custom diverging colormap
cmap_diverging = LinearSegmentedColormap.from_list(
    "consulting_div", [COLORS["negative"], "#F2DCDB", "#FFFFFF", "#D6E4F0", COLORS["primary"]])

fig, ax = plt.subplots(figsize=(10, 8))
mask = np.triu(np.ones_like(corr_matrix, dtype=bool))
sns.heatmap(corr_matrix, mask=mask, annot=True, fmt=".2f", cmap=cmap_diverging,
            center=0, vmin=-1, vmax=1, square=True, linewidths=1.5,
            linecolor="white", cbar_kws={"shrink": 0.75, "label": "Correlation"},
            annot_kws={"fontsize": 11, "fontweight": "bold"}, ax=ax)

ax.set_title("Marketing spend and revenue show strongest positive correlation (0.82)")
ax.tick_params(axis="both", labelsize=10)
add_source_note(ax, "Internal data, Pearson correlation")
save_chart(fig, "correlation_heatmap.png")
```

---

## 7. Time Series — YoY Comparison

```python
monthly = df.groupby(df["date"].dt.to_period("M"))["revenue"].sum().reset_index()
monthly["date"] = monthly["date"].dt.to_timestamp()
monthly["year"] = monthly["date"].dt.year
monthly["month_num"] = monthly["date"].dt.month

fig, ax = plt.subplots()
years = sorted(monthly["year"].unique())
for i, year in enumerate(years):
    yd = monthly[monthly["year"] == year]
    style = {"linewidth": 3, "zorder": 5} if year == years[-1] else {"linewidth": 1.5, "alpha": 0.5}
    ax.plot(yd["month_num"], yd["revenue"], marker="o", markersize=5, label=str(year), **style)

ax.set_xlabel("Month")
ax.set_ylabel("Revenue")
ax.yaxis.set_major_formatter(mticker.FuncFormatter(fmt_dollars))
ax.set_xticks(range(1, 13))
ax.set_xticklabels(["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"])
ax.legend(title="Year", title_fontsize=10)
ax.set_title(f"FY{years[-1]} revenue tracking ahead of prior years across all months")
add_source_note(ax, "Internal data")
save_chart(fig, "revenue_yoy.png")
```

---

## 8. Stacked Bar — Composition Over Time

```python
# Assumes: df with columns date, segment, revenue
pivot = df.pivot_table(index=df["date"].dt.year, columns="segment",
                       values="revenue", aggfunc="sum").fillna(0)

fig, ax = plt.subplots()
pivot.plot(kind="bar", stacked=True, ax=ax, width=0.65, color=PALETTE[:len(pivot.columns)])

# Total labels on top of each bar
for i, year in enumerate(pivot.index):
    total = pivot.loc[year].sum()
    ax.text(i, total + total * 0.01, fmt_dollars(total),
            ha="center", va="bottom", fontweight="bold", fontsize=10, color=COLORS["text"])

ax.yaxis.set_major_formatter(mticker.FuncFormatter(fmt_dollars))
ax.set_xlabel("")
ax.set_ylabel("Revenue")
ax.set_xticklabels(pivot.index, rotation=0)
ax.legend(title="Segment", bbox_to_anchor=(1.02, 1), loc="upper left", frameon=False)
ax.set_title("Enterprise segment grew from 35% to 52% of revenue, now the largest segment")
add_source_note(ax, "Internal data")
save_chart(fig, "stacked_composition.png")
```

---

## 9. KPI Dashboard (Multi-Panel)

```python
def kpi_dashboard(metrics, title="Key Performance Indicators"):
    """Create a consulting-style KPI summary dashboard.

    metrics: list of dicts with keys:
        name, value, unit, change, change_label, status ('green'/'yellow'/'red')
    """
    n = len(metrics)
    cols = min(n, 4)
    rows = (n + cols - 1) // cols

    fig, axes = plt.subplots(rows, cols, figsize=(3.5 * cols, 2.8 * rows))
    fig.suptitle(title, fontsize=16, fontweight="bold", y=1.02, color=COLORS["text"])

    if rows == 1 and cols == 1:
        axes = np.array([axes])
    axes = axes.flatten() if hasattr(axes, "flatten") else [axes]

    status_colors = {
        "green": COLORS["positive"], "yellow": COLORS["warning"], "red": COLORS["negative"]
    }

    for i, m in enumerate(metrics):
        ax = axes[i]
        ax.set_xlim(0, 1)
        ax.set_ylim(0, 1)
        ax.axis("off")

        # Status indicator bar at top
        bar_color = status_colors.get(m.get("status", "green"), COLORS["neutral"])
        ax.add_patch(plt.Rectangle((0, 0.88), 1, 0.12, facecolor=bar_color, transform=ax.transAxes))

        # Metric name
        ax.text(0.5, 0.75, m["name"], ha="center", va="center", fontsize=10,
                color=COLORS["neutral"], fontweight="bold", transform=ax.transAxes)

        # Value
        ax.text(0.5, 0.48, f"{m['value']}{m.get('unit', '')}", ha="center", va="center",
                fontsize=24, fontweight="bold", color=COLORS["text"], transform=ax.transAxes)

        # Change indicator
        change = m.get("change", 0)
        arrow = "▲" if change > 0 else "▼" if change < 0 else "●"
        change_color = COLORS["positive"] if change > 0 else COLORS["negative"] if change < 0 else COLORS["neutral"]
        change_text = f"{arrow} {abs(change):.1f}% {m.get('change_label', 'vs. prior')}"
        ax.text(0.5, 0.2, change_text, ha="center", va="center", fontsize=10,
                color=change_color, transform=ax.transAxes)

        # Border
        for spine in ax.spines.values():
            spine.set_visible(True)
            spine.set_color(COLORS["light_gray"])
            spine.set_linewidth(0.8)

    # Hide unused axes
    for j in range(i + 1, len(axes)):
        axes[j].set_visible(False)

    plt.subplots_adjust(hspace=0.4, wspace=0.3)
    return fig

# Example
metrics = [
    {"name": "Revenue", "value": "$56", "unit": "M", "change": 12.0, "change_label": "YoY", "status": "green"},
    {"name": "Gross Margin", "value": "68", "unit": "%", "change": 2.5, "change_label": "YoY", "status": "green"},
    {"name": "EBITDA Margin", "value": "18", "unit": "%", "change": -1.2, "change_label": "YoY", "status": "yellow"},
    {"name": "NPS", "value": "42", "unit": "", "change": 8.0, "change_label": "vs. Q1", "status": "green"},
    {"name": "Customer Churn", "value": "3.2", "unit": "%", "change": 0.8, "change_label": "vs. prior quarter", "status": "red"},
    {"name": "NRR", "value": "118", "unit": "%", "change": 5.0, "change_label": "YoY", "status": "green"},
    {"name": "CAC Payback", "value": "14", "unit": " mo", "change": -2.0, "change_label": "vs. prior", "status": "yellow"},
    {"name": "Rule of 40", "value": "38", "unit": "", "change": 3.0, "change_label": "vs. prior", "status": "yellow"},
]

fig = kpi_dashboard(metrics, title="Q4 2025 Performance Dashboard")
save_chart(fig, "kpi_dashboard.png")
```

---

## 10. Football Field Chart (Valuation Range)

```python
def football_field(methods, low_values, high_values, title,
                   highlight_method=None, current_price=None):
    """Consulting-grade football field chart for valuation summary."""
    n = len(methods)
    fig, ax = plt.subplots(figsize=(12, max(4, n * 0.9 + 1.5)))

    y_pos = range(n)
    bar_colors = []
    for m in methods:
        if m == highlight_method:
            bar_colors.append(COLORS["primary"])
        else:
            bar_colors.append(COLORS["secondary"])

    # Horizontal range bars
    for i in range(n):
        ax.barh(i, high_values[i] - low_values[i], left=low_values[i],
                color=bar_colors[i], height=0.45, alpha=0.85, zorder=3)
        mid = (low_values[i] + high_values[i]) / 2
        ax.plot(mid, i, "D", color="white", markersize=8, zorder=4)

        # Range labels
        ax.text(low_values[i] - 0.3, i, f"${low_values[i]:.0f}",
                ha="right", va="center", fontsize=10, fontweight="bold", color=COLORS["text"])
        ax.text(high_values[i] + 0.3, i, f"${high_values[i]:.0f}",
                ha="left", va="center", fontsize=10, fontweight="bold", color=COLORS["text"])

    # Current price line
    if current_price is not None:
        ax.axvline(x=current_price, color=COLORS["negative"], linewidth=1.5,
                   linestyle="--", zorder=5)
        ax.text(current_price, n - 0.1, f"Current: ${current_price:.0f}",
                ha="center", va="bottom", fontsize=10, fontweight="bold",
                color=COLORS["negative"])

    ax.set_yticks(y_pos)
    ax.set_yticklabels(methods, fontsize=11)
    ax.set_xlabel("Enterprise Value ($M)")
    ax.set_title(title)
    ax.grid(axis="y", visible=False)
    ax.grid(axis="x", alpha=0.3)

    add_source_note(ax, "Management projections, public filings, Capital IQ")
    return fig

# Example
methods = ["DCF (Base)", "DCF (Upside)", "Comps (EV/Revenue)", "Comps (EV/EBITDA)",
           "Precedent Transactions", "LBO (20% IRR)"]
low =  [180, 210, 160, 170, 190, 150]
high = [240, 310, 220, 250, 270, 200]

fig = football_field(methods, low, high,
    title="DCF and precedent transactions support a valuation range of $190M–$270M",
    highlight_method="DCF (Base)", current_price=195)
save_chart(fig, "football_field_valuation.png")
```

---

## 11. Harvey Ball Matrix

```python
def harvey_ball_matrix(options, criteria, scores, title, recommended=None):
    """Consulting-grade Harvey ball comparison matrix.

    scores: 2D list [options × criteria] with values 0-4
        0 = empty, 1 = quarter, 2 = half, 3 = three-quarter, 4 = full
    """
    n_opts = len(options)
    n_crit = len(criteria)

    fig, ax = plt.subplots(figsize=(2.5 + n_crit * 1.4, 1.5 + n_opts * 0.9))
    ax.set_xlim(-0.5, n_crit - 0.5)
    ax.set_ylim(-0.5, n_opts - 0.5)
    ax.set_aspect("equal")
    ax.axis("off")

    # Header row
    for j, c in enumerate(criteria):
        ax.text(j, n_opts, c, ha="center", va="bottom", fontsize=9,
                fontweight="bold", color=COLORS["text"], rotation=30)

    # Option labels
    for i, o in enumerate(options):
        y = n_opts - 1 - i
        weight = "bold" if o == recommended else "normal"
        color = COLORS["primary"] if o == recommended else COLORS["text"]
        label = f"★ {o}" if o == recommended else o
        ax.text(-0.7, y, label, ha="right", va="center", fontsize=11,
                fontweight=weight, color=color)

    # Harvey balls
    for i in range(n_opts):
        for j in range(n_crit):
            y = n_opts - 1 - i
            score = scores[i][j]
            # Outer circle (always drawn)
            circle = plt.Circle((j, y), 0.28, fill=False,
                                edgecolor=COLORS["neutral"], linewidth=1)
            ax.add_patch(circle)
            # Filled portion
            if score > 0:
                if score == 4:
                    filled = plt.Circle((j, y), 0.28, facecolor=COLORS["primary"],
                                        edgecolor=COLORS["neutral"], linewidth=1)
                    ax.add_patch(filled)
                else:
                    angle = score * 90  # 90° per quarter
                    wedge = mpatches.Wedge((j, y), 0.28, 90, 90 - angle,
                                          facecolor=COLORS["primary"], edgecolor=COLORS["neutral"],
                                          linewidth=1)
                    ax.add_patch(wedge)

    # Title
    ax.set_title(title, fontsize=14, fontweight="bold", pad=40, color=COLORS["text"])

    # Legend
    legend_y = -1.0
    for val, label in [(0, "None"), (1, "Weak"), (2, "Moderate"), (3, "Good"), (4, "Strong")]:
        x_pos = val * 1.2 + (n_crit / 2 - 2.4)
        circle = plt.Circle((x_pos, legend_y), 0.18, fill=False,
                            edgecolor=COLORS["neutral"], linewidth=0.8)
        ax.add_patch(circle)
        if val > 0:
            if val == 4:
                ax.add_patch(plt.Circle((x_pos, legend_y), 0.18,
                             facecolor=COLORS["primary"], edgecolor=COLORS["neutral"]))
            else:
                ax.add_patch(mpatches.Wedge((x_pos, legend_y), 0.18, 90, 90 - val*90,
                             facecolor=COLORS["primary"], edgecolor=COLORS["neutral"]))
        ax.text(x_pos, legend_y - 0.45, label, ha="center", fontsize=8, color=COLORS["neutral"])

    plt.subplots_adjust(left=0.3)
    return fig

# Example
options = ["Option A: Organic", "Option B: Acquisition", "Option C: Partnership"]
criteria = ["Strategic Fit", "Speed", "Cost", "Risk", "Control"]
scores = [
    [3, 1, 3, 4, 4],  # Organic
    [4, 4, 1, 2, 4],  # Acquisition
    [3, 3, 4, 3, 2],  # Partnership
]
fig = harvey_ball_matrix(options, criteria, scores,
    title="Option B (Acquisition) scores highest on strategic fit and speed",
    recommended="Option B: Acquisition")
save_chart(fig, "harvey_ball_matrix.png")
```

---

## 12. Marimekko / Mekko Chart

```python
def marimekko_chart(segments, widths, heights, title, x_label="Market Share (%)",
                    y_label="Segment Size ($M)"):
    """Consulting-grade Marimekko chart (width = size, height = metric)."""
    fig, ax = plt.subplots()

    total_width = sum(widths)
    norm_widths = [w / total_width for w in widths]

    x_start = 0
    for i, (seg, nw, h) in enumerate(zip(segments, norm_widths, heights)):
        color = PALETTE[i % len(PALETTE)]
        ax.bar(x_start + nw / 2, h, width=nw * 0.95, color=color, edgecolor="white",
               linewidth=1.5, zorder=3)

        # Segment label inside bar
        ax.text(x_start + nw / 2, h / 2, f"{seg}\n{h:.0f}%",
                ha="center", va="center", fontsize=9, fontweight="bold",
                color="white" if h > 20 else COLORS["text"])

        # Width label below
        ax.text(x_start + nw / 2, -2, f"${widths[i]:.0f}M",
                ha="center", va="top", fontsize=9, color=COLORS["text"])

        x_start += nw

    ax.set_xlim(0, 1)
    ax.set_ylim(-5, max(heights) * 1.15)
    ax.set_ylabel(y_label)
    ax.set_title(title)
    ax.set_xticks([])
    ax.yaxis.set_major_formatter(mticker.FuncFormatter(fmt_pct))
    ax.grid(axis="x", visible=False)

    add_source_note(ax, "Market data, company estimates")
    return fig

# Example: Market segments by size (width) and margin (height)
segments = ["Enterprise", "Mid-Market", "SMB", "Consumer"]
widths = [120, 85, 60, 35]      # Segment size in $M
heights = [42, 35, 22, 15]      # Margin %

fig = marimekko_chart(segments, widths, heights,
    title="Enterprise segment offers both the largest market and highest margins")
save_chart(fig, "marimekko.png")
```

---

## 13. Driver Decomposition (Revenue Bridge)

```python
df_prior = pd.DataFrame({
    "segment": ["Enterprise", "Mid-Market", "SMB"],
    "units": [100, 500, 2000],
    "revenue": [1_000_000, 1_500_000, 2_000_000]
})
df_current = pd.DataFrame({
    "segment": ["Enterprise", "Mid-Market", "SMB"],
    "units": [120, 480, 2200],
    "revenue": [1_320_000, 1_536_000, 2_090_000]
})

df_prior["asp"] = df_prior["revenue"] / df_prior["units"]
df_current["asp"] = df_current["revenue"] / df_current["units"]

volume_effect = ((df_current["units"] - df_prior["units"]) * df_prior["asp"]).sum()
price_effect = ((df_current["asp"] - df_prior["asp"]) * df_current["units"]).sum()
total_change = df_current["revenue"].sum() - df_prior["revenue"].sum()
mix_effect = total_change - volume_effect - price_effect

print(f"Total Revenue Change: {fmt_dollars(total_change)}")
print(f"  Volume Effect: {fmt_dollars(volume_effect)}")
print(f"  Price Effect:  {fmt_dollars(price_effect)}")
print(f"  Mix Effect:    {fmt_dollars(mix_effect)}")

# Visualize as waterfall
categories = ["FY Prior", "Volume", "Price", "Mix", "FY Current"]
values = np.array([df_prior["revenue"].sum(), volume_effect, price_effect,
                   mix_effect, df_current["revenue"].sum()])
fig = waterfall_chart(categories, values,
    title="Revenue growth driven by volume (+$246K) and pricing (+$166K)")
save_chart(fig, "driver_decomposition.png")
```

---

## 14. Two-Variable Sensitivity Heatmap

```python
def sensitivity_heatmap(row_values, col_values, result_matrix, row_label, col_label,
                        title, base_row=None, base_col=None, fmt="dollar"):
    """Consulting-grade 2-variable sensitivity table as a heatmap."""
    fig, ax = plt.subplots(figsize=(max(8, len(col_values) * 1.5 + 2),
                                    max(5, len(row_values) * 0.8 + 2)))

    # Format function
    if fmt == "dollar":
        cell_fmt = lambda x: fmt_dollars(x)
    elif fmt == "pct":
        cell_fmt = lambda x: f"{x:.1f}%"
    else:
        cell_fmt = lambda x: f"{x:.1f}"

    # Color map: red for low values, white for mid, green for high
    cmap_sens = LinearSegmentedColormap.from_list(
        "sens", [COLORS["negative"], "#FCE4EC", "#FFFFFF", "#E8F5E9", COLORS["positive"]])

    result_array = np.array(result_matrix, dtype=float)
    sns.heatmap(result_array, annot=True, fmt="", cmap=cmap_sens,
                linewidths=1.5, linecolor="white", cbar=False,
                annot_kws={"fontsize": 10, "fontweight": "bold"},
                xticklabels=[f"{v:.0%}" if isinstance(v, float) and v < 1 else str(v) for v in col_values],
                yticklabels=[f"{v:.0%}" if isinstance(v, float) and v < 1 else str(v) for v in row_values],
                ax=ax)

    # Overwrite annotations with formatted values
    for i in range(len(row_values)):
        for j in range(len(col_values)):
            ax.texts[i * len(col_values) + j].set_text(cell_fmt(result_array[i, j]))

    # Highlight base case cell
    if base_row is not None and base_col is not None:
        ri = list(row_values).index(base_row)
        ci = list(col_values).index(base_col)
        ax.add_patch(plt.Rectangle((ci, ri), 1, 1, fill=False,
                                    edgecolor=COLORS["primary"], linewidth=3))

    ax.set_xlabel(col_label, fontsize=12, fontweight="bold")
    ax.set_ylabel(row_label, fontsize=12, fontweight="bold")
    ax.set_title(title)
    ax.tick_params(axis="both", labelsize=10)

    add_source_note(ax, "Sensitivity analysis")
    return fig

# Example: NPV sensitivity to growth rate and discount rate
growth_rates = [0.10, 0.15, 0.20, 0.25, 0.30]
discount_rates = [0.08, 0.10, 0.12, 0.14, 0.16]
base_revenue = 50e6

npv_matrix = []
for g in growth_rates:
    row = []
    for d in discount_rates:
        fcf_yr5 = base_revenue * (1 + g)**5 * 0.15  # 15% FCF margin
        terminal = fcf_yr5 * (1 + 0.03) / (d - 0.03)
        npv = sum(base_revenue * (1+g)**yr * 0.15 / (1+d)**yr for yr in range(1, 6)) + terminal / (1+d)**5
        row.append(npv / 1e6)
    npv_matrix.append(row)

fig = sensitivity_heatmap(growth_rates, discount_rates, npv_matrix,
    row_label="Revenue Growth Rate", col_label="Discount Rate (WACC)",
    title="NPV is most sensitive to discount rate at high growth scenarios",
    base_row=0.20, base_col=0.12)
save_chart(fig, "sensitivity_heatmap.png")
```

---

## 15. Quick EDA Summary

```python
def consulting_eda(df, target_col=None):
    """Generate a quick EDA summary suitable for consulting analysis."""
    print("=" * 60)
    print("DATASET OVERVIEW")
    print("=" * 60)
    print(f"Rows: {len(df):,}  |  Columns: {len(df.columns)}")

    dt_cols = df.select_dtypes("datetime64")
    if len(dt_cols.columns) > 0:
        print(f"Date range: {dt_cols.min().min()} to {dt_cols.max().max()}")

    print(f"\nMissing values:")
    missing = df.isnull().sum()
    for col in missing[missing > 0].index:
        print(f"  {col}: {missing[col]:,} ({missing[col]/len(df)*100:.1f}%)")
    if (missing > 0).sum() == 0:
        print("  None")

    print(f"\nNumeric columns summary:")
    numeric = df.describe().T
    numeric["cv"] = numeric["std"] / numeric["mean"]
    print(numeric[["count", "mean", "std", "min", "50%", "max", "cv"]].round(2).to_string())

    print(f"\nCategorical columns:")
    for col in df.select_dtypes("object").columns:
        n_unique = df[col].nunique()
        top = df[col].value_counts().head(3)
        print(f"  {col}: {n_unique} unique values. Top 3: {dict(top)}")

    if target_col and target_col in df.columns:
        print(f"\nTarget variable ({target_col}) distribution:")
        print(df[target_col].describe().round(2))

consulting_eda(df, target_col="revenue")
```

---

## 16. RFM Customer Segmentation

```python
snapshot_date = df["order_date"].max() + pd.Timedelta(days=1)

rfm = df.groupby("customer_id").agg(
    recency=("order_date", lambda x: (snapshot_date - x.max()).days),
    frequency=("order_date", "count"),
    monetary=("revenue", "sum")
).reset_index()

rfm["r_score"] = pd.qcut(rfm["recency"], 5, labels=[5, 4, 3, 2, 1])
rfm["f_score"] = pd.qcut(rfm["frequency"].rank(method="first"), 5, labels=[1, 2, 3, 4, 5])
rfm["m_score"] = pd.qcut(rfm["monetary"].rank(method="first"), 5, labels=[1, 2, 3, 4, 5])

def segment(row):
    r, f, m = int(row["r_score"]), int(row["f_score"]), int(row["m_score"])
    if r >= 4 and f >= 4: return "Champions"
    if r >= 3 and f >= 3: return "Loyal"
    if r >= 4 and f <= 2: return "New Customers"
    if r <= 2 and f >= 3: return "At Risk"
    if r <= 2 and f <= 2: return "Lost"
    return "Needs Attention"

rfm["segment"] = rfm.apply(segment, axis=1)

# Visualize segments
seg_summary = rfm.groupby("segment").agg(
    count=("customer_id", "count"),
    avg_monetary=("monetary", "mean")
).sort_values("avg_monetary", ascending=True)

seg_colors = {"Champions": COLORS["primary"], "Loyal": COLORS["secondary"],
              "New Customers": COLORS["accent"], "Needs Attention": COLORS["warning"],
              "At Risk": "#ED7D31", "Lost": COLORS["negative"]}

fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(14, 6))

# Left: customer count by segment
colors = [seg_colors.get(s, COLORS["neutral"]) for s in seg_summary.index]
ax1.barh(seg_summary.index, seg_summary["count"], color=colors, height=0.6)
for i, v in enumerate(seg_summary["count"]):
    ax1.text(v + seg_summary["count"].max() * 0.02, i, f"{v:,}",
             va="center", fontweight="bold", fontsize=10)
ax1.set_xlabel("Number of Customers")
ax1.set_title("Champions and Loyal represent 40% of customer base")

# Right: avg monetary by segment
ax2.barh(seg_summary.index, seg_summary["avg_monetary"], color=colors, height=0.6)
for i, v in enumerate(seg_summary["avg_monetary"]):
    ax2.text(v + seg_summary["avg_monetary"].max() * 0.02, i, fmt_dollars(v),
             va="center", fontweight="bold", fontsize=10)
ax2.set_xlabel("Average Lifetime Value ($)")
ax2.set_title("Champions spend 5× more than average — protect and grow this segment")

plt.suptitle("RFM Customer Segmentation", fontsize=16, fontweight="bold", y=1.02)
add_source_note(ax1, "Internal transaction data")
save_chart(fig, "rfm_segmentation.png")
```
