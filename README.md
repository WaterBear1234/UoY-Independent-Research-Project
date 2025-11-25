# Applying AI Techniques in Networking: A Study on the Efficiency of BBO for the MLP

---

## 📌 Project Description

This project investigates three core objectives:

1. **How BBO performance changes under 10 different parameter configurations** across various MLP instances.
2. **How the best-case MLP tour cost from BBO compares to ACO and GA**.
3. **How the best-case computation time from BBO compares to ACO and GA**.

To accomplish this, the project performs:

- Multiple BBO runs per TSP/MLP instance across **10 parameter configurations**  
- **Shapiro–Wilk tests** to determine data normality  
- **ANOVA and Mann–Whitney U (MWU) tests** for statistical significance  
- **Pareto-front analysis** to identify the *best-case* BBO performance  
- Comparative statistical analysis between **BBO vs ACO vs GA**

---

## 🎯 Research Questions and Hypotheses

### **RQ1: Effect of BBO Parameter Configurations on MLP**
**H0:** BBO performance does not significantly differ across parameter configurations.  
**H1:** At least one parameter configuration produces significantly different performance.

**Result:**  
H0 accepted for nearly all TSP instances **except pr107.tsp (cost)** where H1 is accepted.

---

### **RQ2: Best-Case MLP Tour Cost — BBO vs ACO vs GA**
**H0:** No significant difference in best-case cost among BBO, ACO, and GA.  
**H1:** At least one algorithm produces significantly different best-case cost.

**Result:**  
MWU test found **no significant difference** — H0 accepted.

---

### **RQ3: Best-Case Computation Time — BBO vs ACO vs GA**
**H0:** No significant difference in computation time.  
**H1:** There is a significant difference.

**Result:**  
MWU test found **significant differences in time** — H1 accepted (BBO differs from ACO and GA).

---

## 🧪 Methodology Overview

### **Step 1 — Dataset Preparation**
All `.tsp` files from TSPLIB95 stored in `/data`.

### **Step 2 — BBO Parameter Experiments**
- 1 notebook per MLP instance  
- 10 parameter configurations per notebook  
- Outputs:
  - Tour cost  
  - Computation time  

### **Step 3 — Shapiro–Wilk Normality Analysis**
Determines whether:
- ANOVA (parametric)
- Mann–Whitney U (nonparametric)  
should be used.

### **Step 4 — ANOVA/MWU for RQ1**
Tests whether BBO performance differs across its 10 parameter settings.

### **Step 5 — Pareto-Front Determination**
Identifies **best-case cost and time** for each MLP instance.

These serve as the benchmark for RQ2 and RQ3.

### **Step 6–7 — Normality Tests for BBO vs ACO vs GA**
Normality tested separately for cost and time.

### **Step 8–9 — MWU Comparison Against ACO and GA**
Formal statistical verification of RQ2 and RQ3.

---

## ⚙️ Installation

### **Clone the repository** 

git clone https://github.com/WaterBear1234/UoY-Independent-Research-Project.git
cd UoY-Independent-Research-Project.git

### **Install dependencies** 

pip install numpy tsplib95 random math time pandas scipy matplotlib jupyter

---

## ▶️ How to Run the Project

### **Step 1 — Start Jupyter Notebook** 

jupyter notebook

### **Step 2 — Navigate to one of the project folders**

BBO-Parameter-Test/ to re-run BBO

Shapiro-Wilk-Test-All/ to reproduce normality tests

Pareto-Front-Test-All/ for best-case analysis

MWU-BBOvsACO/ or MWU-BBOvsGA/ for algorithm comparison

### **Step 3 — Run all cells sequentially** 

---

## 🧪 How to Use the Repository

### **To test a new MLP instance** 

1. Place .tsp file in /data.

2. Create a new notebook in BBO-Parameter-Test/.

3. Set the parameter configurations.

4. Run 10 experiments and save the results.

5. Follow Steps 3–9 for statistical verification.

### **To compare against new algorithms** 

Repeat Steps 6–9 with the new algorithm’s cost/time results.

---

## 👥 Credits

Developed by **Bui Hoang My Linh**

Supervised by **Dr. Johnson Eze** and **Dr. Bashir Dodo**

Based on MLP results from **Mafort & Ochi (ACO)** and **Ban & Nguyen (GA)**

---

## 📜 License

This project is licensed under the **MIT License**.
