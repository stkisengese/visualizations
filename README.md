# visualizations
A hands-on exploration of Python data visualization libraries — Pandas, Matplotlib, and Plotly — with exercises covering bar plots, scatter plots, subplots, dual-axis charts, interactive line graphs, and box plots. Perfect for beginners and practitioners building dashboards or performing exploratory data analysis (EDA).


# Visualization Cheatsheet  

| Task | **Pandas `.plot()`** | **Matplotlib (`plt`)** | **Axes object (`ax`)** |
|------|----------------------|-------------------------|-------------------------|
| **Create plot** | `df.plot(kind="scatter", x="age", y="num_children")` | `plt.scatter(df["age"], df["num_children"])` | `ax.scatter(df["age"], df["num_children"])` |
| **Set title** | `df.plot(title="My Title")` | `plt.title("My Title")` | `ax.set_title("My Title")` |
| **Set x-label** | *(not direct, use plt or ax)* | `plt.xlabel("Age")` | `ax.set_xlabel("Age")` |
| **Set y-label** | *(not direct, use plt or ax)* | `plt.ylabel("Children")` | `ax.set_ylabel("Children")` |
| **Figure size** | `df.plot(figsize=(8,6))` | `plt.figure(figsize=(8,6))` | `fig, ax = plt.subplots(figsize=(8,6))` |
| **Grid** | *(not direct, use plt or ax)* | `plt.grid(True)` | `ax.grid(True)` |
| **Axis limits** | *(not direct)* | `plt.xlim(0,100)` / `plt.ylim(0,10)` | `ax.set_xlim(0,100)` / `ax.set_ylim(0,10)` |
| **Legend** | `df.plot(legend=True)` | `plt.legend(loc="upper left")` | `ax.legend(loc="upper left")` |
| **Line style** | `df.plot(linestyle="--", color="red")` | `plt.plot(x, y, linestyle="--", color="red")` | `ax.plot(x, y, linestyle="--", color="red")` |
| **Markers** | `df.plot(marker="o")` | `plt.plot(x, y, marker="o")` | `ax.plot(x, y, marker="o")` |
| **Subplots** | `df.plot(subplots=True, layout=(2,3))` | `plt.subplot(2,3,1)` etc. | `fig, ax = plt.subplots(2,3)` then `ax[i,j].plot(...)` |
| **Tight layout** | *(not direct)* | `plt.tight_layout()` | `fig.tight_layout()` |
