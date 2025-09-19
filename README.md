# 🔍 Predictive Analysis on CytoFLEX Equipment Log Data  

This project focuses on **exploring, preprocessing, storing, and analyzing CytoFLEX equipment log data** for predictive maintenance and error trend insights.  

---

## 📂 Dataset Structure & Exploration  

- The dataset consists of **multiple folders**, where **each folder = one Equipment ID**.  
- Inside each equipment folder: multiple log files per equipment.  
- Each log file contains:  
  - `Timestamp`  
  - `Error Message`  
  - `Error Level` (Error / Fatal)  

---

## 🛠️ Data Preprocessing  

- Parsed and consolidated log files across all equipment folders into a **structured dataset**.  
- **Handled missing values** using **forward fill** to maintain continuity in timestamps.  
- Ensured **multiple errors per timestamp** were correctly aligned.  
- Verified data quality – minimal noise detected.  
- Implemented **RAGs (Retrieval-Augmented Generation)** for enhanced exploration and structured error retrieval.  
- Constructed a **final unified dataset** with columns:  

  | Timestamp | Error Message | Error Level | Equipment ID | File Name |  

---

## 📊 Data Overview  

- **Total Parsed Entries:** `1,728,570`  
- **Total Equipment:** `320`  
- **Normal Errors:** `1,711,047`  
- **Fatal Errors:** `17,523`  
- **Unique Errors:** `7,041`  
- **Unique Fatal Errors:** `285`  

---

## 🗄️ Database Integration  

- Stored the structured dataset in **MongoDB (NoSQL)** for:  
  - Scalable storage  
  - Faster retrieval  
  - Efficient querying across equipment IDs and log files  

---

## 📈 Visualization & Analysis  

Developed multiple visualizations to analyze error patterns and predictive signals:  

- **Top 20 Fatal Errors** → Tabular + Graphical  
- **Top 20 Normal Errors** → Tabular + Graphical  
- **All Errors Overview** → Comprehensive tables & visualizations  
- **Error Trend Graphs per Equipment** → Track error counts over time per equipment  

🔽 Implemented **interactive dropdown filters** to switch views:  
- Normal Errors  
- Fatal Errors  
- Unique Errors  

---

## 🚀 Next Steps  

- Develop **predictive models** to forecast equipment failure timelines.  
- Identify **parts most likely to fail** based on historical error trends.  
- Integrate **real-time monitoring dashboard** for proactive alerts.  

---

## 📌 Tech Stack  

- **Language:** Python  
- **Database:** MongoDB (NoSQL)  
- **Visualization:** Matplotlib, Seaborn, Plotly  
- **Data Handling:** Pandas, Regex, OS Pathlib  

---

