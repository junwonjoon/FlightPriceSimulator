# Cheapest Flight Finder (A* Pathfinding)

An interactive Streamlit web application that finds the **cheapest flight route** between two international airports by modeling flights as a weighted graph and applying the **A\*** shortest-path algorithm.

**Important:** All flight prices shown in this application are **simulated** and **not real-time or sourced from any airline or booking service**. Prices are generated for algorithmic demonstration purposes only.

Live Demo:  
https://cs315-dave-jun.streamlit.app/

---

## Project Overview

This project demonstrates how classical graph algorithms can be applied to a real-world inspired problem: flight route optimization.

Given a departure airport and a destination airport, the application:

1. Identifies popular intermediate airports geographically located between the two cities  
2. Filters routes based on travel direction (e.g., northbound flights only)  
3. Constructs a weighted graph where:
   - Nodes represent airports
   - Edges represent flights
   - Edge weights represent **simulated ticket prices**
4. Computes all possible paths and determines the cheapest route using the **A\*** algorithm
5. Visualizes airports, connections, and optimal paths using maps and graphs

---

## Features

- Airport selection for departure and arrival
- Geographic midpoint calculation between two airports
- Discovery of popular intermediate airports
- Direction-based flight filtering
- Table of all possible flight paths with simulated prices
- Interactive map visualization of airports and routes
- Graph visualization of all possible connections
- Cheapest path computation using A\* search
- Simplified visualization of the final optimal route

---

## How the Algorithm Works

### Graph Construction
- Each airport is modeled as a graph node
- Each flight is modeled as a weighted edge
- Edge weights represent **simulated flight prices**

### Pathfinding
- The A\* algorithm is used to compute the cheapest path
- Cost function: cumulative simulated price
- Heuristic: geographic distance between airports
- This significantly reduces the search space compared to uninformed algorithms

---

## Price Disclaimer (Important)

- All prices shown in tables, graphs, and maps are **simulated**
- Prices do **not** reflect real airline fares
- No real-time APIs, booking systems, or airline databases are used
- The purpose of pricing is to demonstrate:
  - Graph modeling
  - Pathfinding algorithms
  - Optimization techniques

---

## Tech Stack

- Python
- Streamlit (web interface)
- Pandas (data processing)
- NetworkX (graph construction and algorithms)
- Folium / map visualization tools
- A\* search algorithm

---

## Running the App Locally

```bash
git clone https://github.com/your-username/cheapest-flight-finder.git
cd cheapest-flight-finder
pip install -r requirements.txt
streamlit run app.py
