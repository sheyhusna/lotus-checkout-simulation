Here’s a **README.md draft** for your project that includes names, purpose, and clear steps for running both SimPy and NetLogo models:

***

# **Lotus Checkout Counter Simulation**

**Course:** TEB2103 – Modelling and Simulation  
**Instructor:** Dr. M Nordin B Zakaria  
**Team Members:**

*   Nur Izzah Irdina binti Norhisham (22001935)
*   Yasmeen binti Ahmad Toha (22000954)
*   Maisarah Hanim Binti Agus Norman (22010141)
*   Nur Shaheera Husna Mohd Shahril (22000926)
*   Maryam Khadeejah binti Zamri (22002567)

***

## **Project Overview**

This project simulates the checkout process at Lotus’s Seri Iskandar using two approaches:

*   **SimPy (Discrete-Event Simulation)** for precise numeric analysis.
*   **NetLogo (Agent-Based Simulation)** for visualizing queue dynamics and customer behavior.

The goal is to analyze:

*   Waiting time and service time variability.
*   Impact of basket size and payment method.
*   Counter performance under normal and peak-hour conditions.

***

## **Repository Contents**

*   `Lotus_Simulation.ipynb` – Google Colab notebook for SimPy simulation.
*   `FINALIZE_Lotus_Payment_SIM.nlogo` – NetLogo model file for agent-based simulation.
*   `Modelling_and_Simulation_REPORT.pdf` – Final report with analysis and recommendations.

***

## **How to Run the Simulations**

### **1. SimPy Model (Google Colab)**

**Steps:**

1.  Open the Google Colab link.
2.  Ensure required libraries are installed:
    ```bash
    pip install simpy pandas
    ```
3.  Run the notebook cells in order:
    *   **Setup Parameters:** Define counters, arrival rate, service time distributions.
    *   **Run Simulation:** Execute the main simulation loop.
    *   **View Results:** Check printed summary and exported CSV (`lotus_checkout_simulation.csv`).

**Outputs:**

*   Average waiting time.
*   Average service time.
*   Total customers served vs reneged.
*   Basket vs trolley efficiency comparison.

***

### **2. NetLogo Model**

**Steps:**

1.  Download and install NetLogo.
2.  Open `Lotus_NetLogo.nlogo`.
3.  Configure the interface:
    *   **Buttons:** `setup`, `go` (Forever).
    *   **Sliders:** `arrival-rate`, `ticks-per-minute`.
    *   **Monitors:** Customers in System, Customers Waiting, Being Served, Total Served, Avg Wait (ticks), Avg Service (ticks).
4.  Click **setup**, then **go** to start the simulation.
5.  Adjust sliders to test scenarios (e.g., peak hour).

**Visual Legend:**

*   White patches = Entrance.
*   Yellow patches = Exit.
*   Blue/Orange patches = Counters & queues.
*   Customer colors:
    *   White = Arriving
    *   Red = Waiting
    *   Green = Being served
    *   Yellow = Leaving
*   Violet = Staff.

***

## **Results Summary**

| Metric              | SimPy Result  | NetLogo Observation                |
| ------------------- | ------------- | ---------------------------------- |
| Avg Waiting Time    | 0.73 mins     | \~1.5–3.5 mins (varies by counter) |
| Avg Service Time    | 2.54 mins     | \~1.0–2.4 mins (basket vs trolley) |
| Peak Hour Queue Len | 3–4 customers | Up to 8 customers (visual)         |

***

## **Recommendations**

*   Introduce express lanes for small baskets.
*   Optimize MyKasih counter operations.
*   Implement dynamic staffing during peak hours.

***
