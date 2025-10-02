# WeedNet-IoT-Simulator: Herbicide-based Weed Management

A proof-of-concept **software simulator** for a precision agriculture IoT system. This demo showcases bandwidth-efficient image transmission and targeted herbicide application using a novel **Graph-Based Image Compression** technique.

**Objective:** To maximize herbicide and bandwidth savings by only transmitting the necessary information (weed locations) across a distributed drone/sensor network.

## Demo Workflow (The Sci-Fi Visualization)

The project runs as a step-by-step simulation, visualized live using **Streamlit** and **Matplotlib/NetworkX** with a **dark, neon-themed aesthetic**.

1. **Input & Detection:** A farm image is loaded, and a binary **Weed Mask** is generated using a quick color-thresholding algorithm.
2. **Graph Generation & Compression:**
   * The image is segmented into **Superpixels (Nodes)**.
   * A custom compression algorithm identifies weed areas and merges all non-weed areas into large, efficient **Background Nodes**.
   * This compressed data is stored, and the reduction is calculated.
3. **Data Transmission Simulation:** The compressed data chunks (background blobs, weed segments) are routed as **Packets** through a simulated IoT network (Sensors, Relays, Sprayer). **The animated packet flow visualizes bandwidth efficiency.**
4. **Targeted Spraying:** Upon receiving a weed packet, the final **Sprayer Node** simulates a targeted herbicide pulse overlay on the original image.
5. **Scoreboard:** Real-time metrics are displayed to quantify the system's efficiency.

## Key Features

* **Novel Compression:** Graph-based approach reduces redundant background data transmission, achieving high **Compression Ratios**.
* **IoT Simulation:** Uses **NetworkX** to model complex node networks and animate the flow of data packets.
* **Targeted Control:** Calculates and visualizes precise **Herbicide Savings** versus traditional broadcast spraying.

## Installation & Running

### 1. Prerequisites

You need Python 3.8+ installed.

### 2. Setup

Clone the repository and install the dependencies in a virtual environment:

```
# Clone the repository
git clone https://github.com/[Your-Username]/WeedNet-IoT-Simulator.git
cd WeedNet-IoT-Simulator

# Install necessary Python packages
pip install -r requirements.txt
```

### 3. Running the Application

Launch the Streamlit app:

```
streamlit run app.py
```

---

## Simulation Stats Scoreboard

The demo prominently displays these three metrics:

| Metric             | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Compression Ratio  | Measures the reduction in data size (Initial Bytes / Compressed Bytes).     |
| Bandwidth Saved    | Percentage of data transmission avoided by using the compression method.    |
| Herbicide Saved    | Percentage of the total field area that was not sprayed, showcasing precision. |

---

## Export to Sheets

(Metrics can optionally be exported to CSV/Google Sheets for further analysis.)
