[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-Enabled-red?logo=streamlit)](https://streamlit.io/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-yellow?logo=scikit-learn)](https://scikit-learn.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-GNN-orange?logo=pytorch)](https://pytorch.org/)
[![PyTorch Geometric](https://img.shields.io/badge/PyTorch%20Geometric-Graph%20Learning-lightgrey?logo=pytorch)](https://pytorch-geometric.readthedocs.io/)
[![Folium](https://img.shields.io/badge/Folium-Map-green?logo=leaflet)](https://python-visualization.github.io/folium/)
[![Last Updated](https://img.shields.io/badge/Updated-April%205%2C%202025-success)](https://github.com/)



# ✈️ Flight Route Optimizer with GNN and Map Visualization

Find and visualize optimized global flight routes using:
- Real airline data (`airports.dat`, `routes.dat`)
- A Graph Neural Network (GNN) for smart airport embeddings
- Interactive widgets for user input
- Folium map for visualization

---

## 🚀 Features

- 📡 Real-world flight data
- 🧠 GNN-based route optimization
- 🧭 Path filtering by stops and airlines
- 🗺️ Interactive Folium map
- 🎛️ Widgets for intuitive user control

---

## 📂 Files

| File                     | Description                                             |
|--------------------------|---------------------------------------------------------|
| `airports.dat`           | Airport metadata (IATA code, name, lat/lon, etc.)       |
| `routes.dat`             | Actual routes (source, destination, airline)            |
| `flight_gnn_notebook.ipynb` | Main Jupyter Notebook                              |
| `README.md`              | This documentation file                                 |

---

## 🧰 Requirements

Install dependencies:

```bash
pip install torch torch-geometric networkx pandas folium ipywidgets scikit-learn
```

## 🛠️ How to Run

1. Download `airports.dat` and `routes.dat` from [OpenFlights](https://openflights.org/data.html)

2. Launch the notebook:

    ```bash
    jupyter notebook
    ```

3. Open `flight_gnn_notebook.ipynb`

4. Run all cells and interact via widgets

## 🎮 Interactive UI (Widgets)

The notebook provides the following interactive widgets:

| **Widget**                | **Description**                                                |
|--------------------------|----------------------------------------------------------------|
| `Source` dropdown        | Select source airport (IATA)                                   |
| `Destination` dropdown   | Select destination airport (IATA)                              |
| `Max Stops` slider       | Limit number of layovers (0 to 5)                              |
| `Allowed Airlines` textbox | Comma-separated airline codes (e.g., `AA,BA,LH`)               |
| `Find Route` button      | Run optimizer and visualize route on map                       |

Once clicked, the notebook prints the best route and displays it on a world map using **Folium**.

## 🧠 Model Overview

- Graph is built from real-world routes (`routes.dat`)
- Each node = airport, each edge = route
- Node features: Latitude, Longitude
- GNN learns structure and similarity between airports
- Route selection optimized via:
  - NetworkX shortest path
  - Optional: learned GNN distance metric

---

## 🗺️ Visualization

- Interactive Folium map shows the optimized route
- Markers for each airport
- Polyline connecting the full path
- Automatically centers the world map on route

## 🧑‍💻 Author

**Ekaansh Sawaria**  
Manipal University Jaipur  
email: [sawariaekaansh@gmail.com](sawariaekaansh@gmail.com)
