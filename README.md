# FairFlow 🚚⚖️

### AI-Powered Fair Dispatch System for Logistics

FairFlow is a fairness-aware route assignment system designed to ensure
**balanced workload distribution among delivery drivers**. Instead of
optimizing only distance and delivery speed, FairFlow focuses on
**long-term fairness**, preventing driver burnout and improving
workforce sustainability using effort scoring, fairness ledger tracking,
drift detection AI, and ML-based route recommendations.

------------------------------------------------------------------------

## Problem

Modern logistics routing systems optimize: - Distance - Fuel
consumption - Delivery time

However, they ignore **human fairness**.

This leads to: - Some drivers repeatedly receiving harder routes -
Driver fatigue and burnout - Reduced morale - High driver attrition
costs for companies

FairFlow solves this by introducing **fairness intelligence into
dispatch systems**.

------------------------------------------------------------------------

## Solution

FairFlow introduces a **three-layer fairness architecture**:

### 1️⃣ Fairness Ledger

Tracks driver workload history and assigns fairness credits based on
effort.

### 2️⃣ Fairness Drift AI

Monitors workload distribution over time using a **7‑day sliding
window** and detects imbalance.

### 3️⃣ ML Recommendation Engine

Suggests route difficulty assignments while ensuring fairness
constraints.

Together, these layers ensure **fair, transparent, and sustainable route
assignments**.

------------------------------------------------------------------------

## System Architecture

Route Data\
↓\
Effort Score Calculation\
↓\
Team Average Calculation\
↓\
Fairness Ledger (Credits System)\
↓\
Fairness Drift Detection AI\
↓\
ML Recommendation Engine\
↓\
Final Route Assignment

------------------------------------------------------------------------

## Key Features

-   Effort-based route difficulty scoring
-   Fairness credit ledger system
-   Sliding-window fairness drift detection
-   AI-based route recommendation
-   Explainable route assignment decisions
-   Driver feedback integration
-   Real-time fairness monitoring

------------------------------------------------------------------------

## Tech Stack

### Backend

-   Python
-   FastAPI
-   SQLAlchemy
-   JWT Authentication

### Frontend

-   React
-   Vite
-   JavaScript
-   CSS

### AI / ML

-   Rule-based explainable ML
-   Effort scoring model
-   Fairness drift detection algorithm

### Database

-   SQLite (Development)
-   PostgreSQL (Production Ready)

------------------------------------------------------------------------

## How It Works

### Step 1 --- Collect Route Data

The system collects delivery route features such as: - Apartments -
Stairs - Heavy packages - Traffic - Weather - Distance

### Step 2 --- Effort Score Calculation

Each route receives an **effort score** representing workload
difficulty.

### Step 3 --- Team Average Calculation

The system computes the **average workload across all drivers**.

### Step 4 --- Fairness Ledger Update

Drivers earn or spend **fairness credits** based on how their workload
compares to the team average.

### Step 5 --- Fairness Drift Detection

The AI monitors the **last 7 days of workload distribution** using a
sliding window to detect imbalance.

### Step 6 --- ML Recommendation

The ML module suggests the best driver‑route pairing while maintaining
fairness.

### Step 7 --- Final Route Assignment

Routes are assigned ensuring **balanced workload across the team**.

------------------------------------------------------------------------

## Example Scenario

### Without FairFlow

Driver A repeatedly receives apartment-heavy routes while Driver B
receives easier suburban routes.

Result: - Driver A becomes overloaded - Burnout occurs - Driver resigns

### With FairFlow

-   System tracks workload history
-   Detects fairness drift
-   Redistributes routes fairly

Result: - Balanced workload - Reduced burnout - Higher driver retention

------------------------------------------------------------------------

## Business Impact

Using FairFlow, logistics companies can achieve: - Reduced driver
attrition - Improved driver morale - Transparent route assignments -
Lower recruitment and training costs - Sustainable workforce management

------------------------------------------------------------------------

## Installation

### Backend

   cd backend 
   dir main.py
   uvicorn main:app --reload --port 8000

    
### Frontend

    cd frontend
    npm install
    npm run dev

------------------------------------------------------------------------

## API Documentation

After starting the backend server: http://localhost:8000/docs

------------------------------------------------------------------------

## Project Structure

    fairflow/
    │
    ├── backend/
    │   ├── main.py
    │   ├── models.py
    │   ├── logic.py
    │   ├── fairness_drift.py
    │   ├── ml_recommendation.py
    │   └── database.py
    │
    ├── frontend/
    │   ├── src/
    │   ├── components/
    │   └── pages/
    │
    └── README.md

------------------------------------------------------------------------

## Innovation

FairFlow introduces **fairness memory** into logistics dispatch systems.

Traditional systems ask: "What is the fastest route?"

FairFlow asks: **"What is the fairest workload over time?"**

------------------------------------------------------------------------

## License

MIT License
