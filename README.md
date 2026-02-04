# Clock-Network-Optimization-H-Tree-vs-Mesh-
A methodology-driven study and automation framework for comparing clock distribution architectures with a focus on skew, latency, and dynamic power.


---

# ✅ ** GitHub Repository Structure**

```
clock-network-optimization/
│
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
│
├── scripts/
│   ├── automation.py
│   ├── skew_analysis.tcl
│   ├── power_analysis.tcl
│   └── cts_run.tcl
│
├── data/
│   ├── h_tree_results.csv
│   ├── mesh_results.csv
│   └── baseline_results.csv
│
├── reports/
│   ├── skew_report/
│   │   └── skew_summary.pdf
│   ├── power_report/
│   │   └── power_summary.pdf
│   └── final_comparison.pdf
│
├── docs/
│   ├── methodology.md
│   ├── tools.md
│   ├── results.md
│   └── reproducibility.md
│
├── figures/
│   ├── h_tree.png
│   ├── mesh.png
│   ├── skew_comparison.png
│   └── power_comparison.png
│
└── examples/
   ├── run_h_tree.sh
   └── run_mesh.sh
```

---


# ⏱️ Clock Network Optimization — H-Tree vs Mesh

**Yarok14 Technologies — Semiconductor & Systems Engineering**

📌 Repository: [https://github.com/Yarok14Technologies/clock-network-optimization](https://github.com/Yarok14Technologies/clock-network-optimization)

---

## 🎯 Objective

This project presents a **methodology-driven comparison of H-tree and Mesh clock distribution networks**, combined with a **Python–TCL automated analysis flow** for evaluating:

* Clock **skew**
* Clock **insertion delay**
* **Dynamic clock power**

The work demonstrates a **12% reduction in clock dynamic power** through topology and buffering optimization.

---

## 🔍 Scope of Work

* Side-by-side evaluation of **H-tree vs Mesh clock architectures**
* Identical placement, timing constraints, and clock frequency for fair comparison
* Automated extraction of:

  * Worst-case skew
  * Mean skew
  * Insertion delay
  * Dynamic clock power
* CSV-based data logging + visualization-ready outputs

---

## 🧠 Technical Methodology

### 1️⃣ Clock Topologies Compared

**H-Tree**

* Symmetric clock distribution
* Easier skew balancing
* Lower wire capacitance → lower power

**Mesh**

* Highly robust to process variation (PVT/OCV)
* Better resilience to local congestion
* Higher capacitance → higher dynamic power

---

### 2️⃣ Automation Flow (Python + TCL)

The flow performs:

1. Reads placement database
2. Generates clock topology (H-tree or Mesh)
3. Invokes CTS via TCL
4. Extracts timing and power metrics
5. Stores results in structured CSV files
6. Enables post-processing and visualization

**Command to run:**

```bash
python scripts/automation.py --topology h_tree
```

or

```bash
python scripts/automation.py --topology mesh
```

---

## 📊 Key Results

| Metric              | H-Tree   | Mesh     | Observation                |
| ------------------- | -------- | -------- | -------------------------- |
| Worst Skew          | Low      | Very Low | Mesh slightly better       |
| Insertion Delay     | Moderate | Higher   | H-tree better              |
| Dynamic Clock Power | Baseline | +12%     | **H-tree saved 12% power** |

### ✅ Final Decision:

👉 **H-tree selected as the final clock network** due to superior power efficiency with acceptable skew.

---

## 🛠️ Tools Used

* **Python** (Automation & Data Processing)
* **TCL** (EDA tool scripting)
* **CTS / STA Tool** (e.g., Innovus, ICC2, or Tempus)
* CSV-based reporting
* Matplotlib (optional for visualization)

*(Replace with your exact tool if needed.)*

---

## 📁 Repository Contents

| Folder     | Purpose                         |
| ---------- | ------------------------------- |
| `scripts/` | Python + TCL automation         |
| `data/`    | Raw extracted results           |
| `reports/` | Timing & power analysis reports |
| `figures/` | Visual comparisons              |
| `docs/`    | Methodology & reproducibility   |

---

## 🔁 Reproducibility

See: [`docs/reproducibility.md`](docs/reproducibility.md)

Basic steps:

1. Load placement database
2. Run `automation.py`
3. Review generated CSVs
4. Validate against STA reports

---

## 🤝 Contributing

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Open a Pull Request

---

## 📜 License

MIT License — see `LICENSE`

---

## 📬 Contact

**Yarok14 Technologies**
GitHub: [https://github.com/Yarok14Technologies](https://github.com/Yarok14Technologies)
Founder: Bibin N. Biji


