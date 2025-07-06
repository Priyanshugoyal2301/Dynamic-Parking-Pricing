# 🚗 Dynamic Pricing for Urban Parking Lots

This project implements a dynamic pricing system for urban parking lots using historical and real-time data. It features three pricing models—baseline, demand-based, and competitive—and integrates with Pathway for real-time streaming and simulation. Visualizations are created using Bokeh, and the solution supports exporting results for analysis.

---

## 📦 Tech Stack

| Layer           | Technologies Used                        |
|----------------|-------------------------------------------|
| Programming     | Python 3.11                              |
| Visualization   | Bokeh                                    |
| Streaming       | Pathway (v0.24.1)                        |
| Data Handling   | Pandas, NumPy                            |
| Notebook        | Google Colab / Jupyter                   |
| Deployment      | GitHub                                   |

---

## 🧠 Model Workflow

### ✅ Model 1: Baseline
- Price increases over time based on simple occupancy ratio.
- Formula: `next_price = base_price + alpha * (occupancy/capacity)`

### ✅ Model 2: Demand-Based
- Incorporates occupancy, queue length, traffic, special day, and vehicle type.
- Formula: `price = base_price * (1 + λ * normalized_demand)`

### ✅ Model 3: Competitive Pricing
- Uses Haversine distance to find nearby lots and adjusts prices based on local competition and occupancy.
- Incorporates rerouting logic if conditions met.

---

## 🧪 Real-Time Simulation (Pathway)

- Schema defined using `pw.Schema`
- Streaming prices computed as:
```python
price = 10 + 2.0 * occupancy / capacity
```
- Live data is streamed into a Pathway table and printed in real time.

---

## 📊 Visualizations
- Bokeh is used to render line charts of pricing over time.
- Each model shows 5 sample parking lots.

---

## 📁 Folder Structure

```
📦dynamic-parking
 ┣ 📄 baseline_model.csv
 ┣ 📄 demand_model.csv
 ┣ 📄 competitive_model.csv
 ┣ 📄 DynamicPricingNotebook.ipynb
 ┣ 📄 README.md
```

---

## 📤 How to Run

1. Open `DynamicPricingNotebook.ipynb` in Google Colab or Jupyter.
2. Upload your dataset (`dataset.csv`) into the environment.
3. Run cells in order to:
   - Preprocess and clean data
   - Run all three pricing models
   - Visualize results
   - Run real-time simulation with Pathway

---

## 📄 Optional: Report
You can add a PDF project report summarizing:
- Methodology
- Observations
- Model Comparison
- Screenshots of results

---

## 🔗 GitHub Access
- Ensure your repository is public or share access with reviewers.
- Include all `.csv` outputs and notebook.

---

## 🙌 Contributors
- Priyanshu Goyal

---

Let me know if you'd like to convert this into a downloadable README.md file or need help uploading everything to GitHub.
