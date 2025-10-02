# WeedNet-IoT-Simulator  
**Smart Weed Control. Less Spray. Less Data.**  

A proof-of-concept **software simulator** for futuristic farming.  
It demonstrates how **Graph-Based Image Compression** combined with an **IoT packet network** can save both **herbicide** and **bandwidth** by transmitting only what matters — the weeds.  

---

## How It Works  

1. **Weed Detection** – Load farm image and create a quick binary weed mask.  
2. **Compression** – Split into superpixels, merge background, keep only weed nodes.  
3. **Transmission** – Send compressed chunks as packets across a simulated IoT network.  
4. **Targeted Spraying** – Sprayer node receives weed packets and applies herbicide only where needed.  
5. **Scoreboard** – Live dashboard shows efficiency metrics.  

*(Visualization built with Streamlit + Matplotlib in a dark neon theme.)*  

---

## Key Features  

- **Graph-Based Compression** – Removes redundant background data.  
- **IoT Network Simulation** – Visualizes packet flow across sensors, relays, and sprayers.  
- **Precision Spraying** – Demonstrates herbicide savings compared to broadcast spraying.  

---

## Quickstart  

```bash
git clone https://github.com/[Your-Username]/WeedNet-IoT-Simulator.git
cd WeedNet-IoT-Simulator
pip install -r requirements.txt
streamlit run app.py
```

---

## The Scoreboard  

``` 
| Metric            | Meaning                                  |
|-------------------|------------------------------------------|
| Compression Ratio | Initial Bytes ÷ Compressed Bytes          |
| Bandwidth Saved   | % of data skipped in transmission         |
| Herbicide Saved   | % of land left untouched by spray         |

```

---

## Export Options  

```
Results can be saved to CSV or Google Sheets for analysis and reporting.
```

---

**Not just a simulation. Not just code.  
This is a preview of how future farming could look.**  
