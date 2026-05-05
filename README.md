# 📊 Performance Modeling Mini Project – Spotify Streaming Analysis

**Module:** Performance Modeling – EEX5362  
**Author:** G.L.T.S. Gamalath 

A data-driven performance analysis of Spotify's music streaming platform, using **queueing theory (M/M/1 model)** to evaluate playback behavior under different real-world network conditions.

---

## 🎯 Project Overview

This project evaluates how network conditions affect Spotify's streaming experience — measuring start delays, buffer counts, and total buffer times across Wi-Fi, 4G, and 3G networks in Colombo, Sri Lanka.

---

## 📁 Repository Contents

```
├── dataset.csv              # Manually collected playback data (40 test sessions)
├── dataAnalysis.ipynb       # Jupyter Notebook with full analysis & visualizations
└── README.md
```

> 📄 **Full report:** Available separately (not included in the repository).

---

## 🔬 Methodology

Data was collected manually by streaming songs across different conditions:

| Measured Variable | Description |
|-------------------|-------------|
| Network Type | Wi-Fi, 4G, 3G |
| Network Speed (Mbps) | Measured via Speedtest.net |
| RTT / Ping (ms) | Measured via Termux ping commands |
| Start Delay (s) | Time from pressing play to audio start |
| Buffer Count | Number of playback interruptions |
| Total Buffer Time (s) | Total duration of buffering |
| ISP | Dialog, SLT Mobitel, Airtel |
| Time of Day | Morning, Afternoon, Evening, Night |

**Modelling technique:** M/M/1 Queue — each play request is treated as an arrival, and network delivery speed defines the service rate.

---

## 📈 Key Findings

- **Wi-Fi** had the lowest start delays and zero buffering in almost all cases
- **3G** caused the highest start delays and some complete playback failures
- **Dialog** was the fastest ISP among those tested in Colombo
- **Night-time** sessions had the highest average start delay
- Spotify's pre-buffering strategy successfully eliminated mid-playback interruptions in 95%+ of tests

---

## ▶️ Run the Analysis

```bash
# Clone the repo
git clone https://github.com/TishaSachi/Performance-Modelling-Mini-Project.git
cd Performance-Modelling-Mini-Project

# Install dependencies
pip install pandas matplotlib jupyter

# Open the notebook
jupyter notebook dataAnalysis.ipynb
```

---

## 📌 Status

> ✅ Complete — submitted as academic coursework

---

## 👤 Author

**Tishani Gamalath**  
Undergraduate Software Engineering Student 
S-number: s22010117
