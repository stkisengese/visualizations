# Visualizations  

A hands-on exploration of Python data visualization libraries — **Pandas, Matplotlib, and Plotly** — with exercises covering bar plots, scatter plots, subplots, dual-axis charts, interactive line graphs, and box plots. Perfect for beginners and practitioners building dashboards or performing exploratory data analysis (EDA).  

---

## Visualization Cheatsheet  

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

---

## Key Learning Points  

### 📊 Matplotlib Subplots  
- `plt.subplots(rows, cols)` creates multiple plots in a grid  
- `subplots_adjust(hspace, wspace)` controls spacing between plots  
- Access individual subplots using `axes[row, col]`  
- `transform=axes.transAxes` positions text relative to subplot coordinates  

### 📈 Plotly Time Series  
- **Plotly Express**: High-level interface (`px.line()`) for quick plots  
- **Graph Objects**: Low-level interface (`go.Scatter()`) for more control  
- `init_notebook_mode()` enables offline plotting in Jupyter  
- Interactive features come built-in (zoom, pan, hover)  

### 📦 Plotly Box Plots  
- `go.Box()` creates box plots showing quartiles and outliers  
- Easy to compare distributions across different groups  
- Built-in interactivity (hover for statistics)  
- `marker_color` customizes appearance  
- `boxpoints` shows outliers, suspected outliers, all points, or none  

### 🎯 Overall Visualization Strategy  
- **Pandas** → Quick exploration and basic plots  
- **Matplotlib** → Fine-grained control and customization  
- **Plotly** → Interactive dashboards and presentations  
- ✅ Choose the right tool based on your **audience and purpose**!  
