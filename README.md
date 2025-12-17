# Optimizing Delivery Routes for a Local E-Commerce Company

## Project Overview
Small delivery companies face rising fuel costs, increasing customer expectations, and constantly changing traffic conditions. Manual route assignment or basic routing systems often result in longer routes, wasted fuel, overtime pay, and delayed deliveries.

This project applies Mixed Integer Programming (MIP) to optimize delivery route assignments. The model minimizes total travel distance while respecting real operational constraints such as truck capacity and customer coverage.

This project was completed as part of the GB730 Application Project.

## Problem Statement
Which delivery routes minimize total distance traveled while ensuring every customer is served exactly once and truck capacity limits are not exceeded?

## Objective
Minimize the total distance traveled by all delivery trucks while completing all customer deliveries.

## Methodology
- Optimization approach: Mixed Integer Programming
- Solver: Pyomo with CBC solver
- Decision variables:
  - Binary variable indicating whether truck t serves customer c
- Constraints:
  - Each customer is visited exactly once
  - Each truck has a maximum delivery capacity
  - Limited number of available trucks

## Model Inputs
- Trucks: 5 trucks (T1–T5)
- Customers: 15 customers (C1–C15)
- Truck capacity: Maximum of 5 deliveries per truck
- Customer demand: 1 delivery per customer
- Distance matrix: Simplified example distances for demonstration

## Results
The optimized model assigns customers to trucks efficiently while meeting all constraints:

- One truck assigned to 5 customers
- One truck assigned to 4 customers
- Remaining trucks assigned to 2 customers each

The model reduces unnecessary travel and balances delivery assignments under the given constraints.

## Tools and Technologies
- Python
- Pyomo
- CBC Solver
- Jupyter Notebook
- Google Colab

## Limitations
This model is simplified for learning and demonstration purposes. It does not currently include:
- Real-world distance or travel time data
- Traffic variability
- Delivery time windows
- Package weight or load constraints
- Multiple orders per customer
- Large-scale routing scenarios

Some trucks may be assigned more customers than others, which may not be optimal once additional constraints are introduced.

## Future Improvements
- Integrate real-world distance and travel time data
- Add delivery time windows and priority deliveries
- Incorporate traffic conditions
- Test scalability with larger datasets
- Enable real-time and dynamic route optimization

## Project Files

- `MN__GB730_Application_Project.ipynb` – Optimization model and analysis
- `Optimizing Delivery Routes for a Local E-Commerce Company.pptx` – Project summary slides

## Notebook Link
https://colab.research.google.com/drive/1hI7gGTCGKHOZtHftD00WK_3NLaZemcY7?usp=sharing
