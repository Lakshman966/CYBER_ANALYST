 📍 GPS Trilateration Simulator — A6

Mathematics Mini Project — ABHIYAN

<p align="center">TEAM CYBER ANALYSTS

<br>Applying Systems of Linear Equations to GPS Trilateration

</p>---

🚀 Project Overview

GPS Trilateration Simulator (A6) is a Mathematics mini project that demonstrates how the position of a mobile device can be estimated using distances measured from three known cell towers.

The project takes a real-world positioning problem and converts it into a mathematical model using circle equations and systems of linear equations.

The core idea is:

3 Cell Towers
      ↓
Distance Measurements
      ↓
Circle Equations
      ↓
Subtract Pairs of Equations
      ↓
Linear Equations
      ↓
Solve for (x, y)
      ↓
Estimated Phone Location
      ↓
Visualize on Map

The project is implemented using Python, NumPy/SymPy, Matplotlib, and Google Colab, with an interactive web-style interface for presenting the simulation.

---

📌 1. Problem Statement

Three cell towers detect a mobile phone at distances:

d₁, d₂, d₃

Each distance defines a circle around its corresponding tower.

If the towers are located at:

T₁ = (x₁, y₁)
T₂ = (x₂, y₂)
T₃ = (x₃, y₃)

and the unknown phone location is:

P = (x, y)

then each tower produces a circle equation.

For a tower at "(xᵢ, yᵢ)":

(x - xᵢ)² + (y - yᵢ)² = dᵢ²

By subtracting pairs of these equations, the quadratic terms can be eliminated.

This produces a system of linear equations, which can then be solved to obtain the estimated location "(x, y)".

---

🧮 2. Mathematical Concept & Model

Core Mathematical Concept

«System of Linear Equations from Nonlinear Origins»

The original trilateration equations are nonlinear because they contain:

x² and y²

However, subtracting two circle equations eliminates these common quadratic terms.

The resulting equations have the form:

Ax + By = C

and

Dx + Ey = F

These equations form a system:

┌ A  B ┐ ┌ x ┐   ┌ C ┐
│      │ │   │ = │   │
└ D  E ┘ └ y ┘   └ F ┘

or:

A X = B

where:

A = coefficient matrix

X = unknown position vector

B = constant vector

The solution vector gives:

X = [x, y]ᵀ

---

📡 3. Trilateration Model

For three towers:

Tower 1

(x - x₁)² + (y - y₁)² = d₁²

Tower 2

(x - x₂)² + (y - y₂)² = d₂²

Tower 3

(x - x₃)² + (y - y₃)² = d₃²

Subtracting the first equation from the second gives one linear equation.

Subtracting the first equation from the third gives another.

Therefore:

Linear Equation 1
        +
Linear Equation 2
        ↓
Solve simultaneously
        ↓
(x, y)

The calculated point represents the estimated location of the phone.

---

⚙️ 4. Methodology & Algorithm

The project follows these major steps:

Step 1 — Input

Receive the coordinates of the three towers and their measured distances.

Step 2 — Mathematical Model

Convert each distance measurement into a circle equation.

Step 3 — Linearization

Subtract pairs of circle equations to eliminate the quadratic terms.

Step 4 — Matrix Formation

Convert the resulting equations into matrix/vector form.

Step 5 — Solve

Use a numerical linear algebra method to calculate the unknown coordinates.

Step 6 — Verification

Check whether the calculated location approximately satisfies the original distance equations.

Step 7 — Visualization

Render:

- Three reference towers
- Three distance circles
- Estimated phone position
- Coordinate grid
- Numerical output

---

🐍 5. Implementation Details

Development Environment

Google Colab
Python 3

Key Libraries

Library| Purpose
NumPy| Numerical calculations and linear algebra
SymPy| Symbolic mathematical operations
Matplotlib| Graphs and mathematical visualization
IPython| Rendering HTML inside Colab

Front-End Technologies

The project interface also uses:

HTML
CSS
JavaScript

to create a modern dashboard-style presentation.

---

🖥️ 6. User Interface

The project includes a GeoTrack interface designed specifically around the GPS/trilateration concept.

Main Navigation

Simulator
Sensitivity
Mathematics
How It Works
Applications

Interface Design

The UI uses:

- Dark technical theme
- GPS-inspired visualization
- Coordinate grid
- Tower markers
- Distance circles
- Estimated-location marker
- Responsive layout
- Mathematical explanation panels

The interface is designed to make the mathematical model easier to understand visually.

---

📊 7. Results & Discussion

The simulator produces a numerical estimate of the unknown location.

The expected result contains:

Estimated X-coordinate
Estimated Y-coordinate

along with a graphical representation showing the relationship between:

Tower 1 ─────┐
             │
Tower 2 ─────┼──→ Intersection → Estimated Location
             │
Tower 3 ─────┘

The visualization helps demonstrate how multiple distance measurements can constrain an unknown position.

---

📈 8. Sensitivity Analysis

A major part of the project is understanding how changes in measured distances affect the calculated position.

In a theoretical ideal case:

Exact distances
      ↓
Accurate circles
      ↓
Common intersection
      ↓
Accurate position

In practical systems, measurement errors can cause the circles to fail to intersect at exactly one point.

Therefore:

Measurement Error
        ↓
Circle Position Error
        ↓
Intersection Error
        ↓
Location Estimation Error

This provides an important connection between the mathematical model and real-world positioning systems.

---

📸 9. Screenshots & Proof of Work

The project development was documented across multiple stages.

Day 1 — Setup

Google Colab setup
Python environment
Initial "Hello World"

Day 2 — MVP

AI-assisted Vibe Coding
Initial simulator interface
Basic visualization

Day 3 — Custom Development

Custom analysis
Visualization improvements
Mathematical sections
Interactive-style interface

Screenshots and additional proof-of-work material can be added to:

assets/screenshots/

---

🌍 10. Real-World Impact

Trilateration is an important mathematical concept behind location estimation systems.

The underlying idea can be applied to areas such as:

- 📍 Location estimation
- 🛰️ Navigation
- 📱 Mobile positioning
- 🤖 Robotics
- 📡 Wireless sensor networks
- 🚗 Navigation systems
- 🌐 Geolocation technologies

Important Note

The project demonstrates the mathematical principle of trilateration.

A commercial GPS receiver involves significantly more engineering, including satellite timing, atmospheric corrections, coordinate transformations, signal processing, and error correction.

Therefore, this project should be understood as an educational mathematical simulator rather than a complete GPS receiver implementation.

---

⚠️ 11. Limitations & Assumptions

The current mathematical model assumes idealized conditions.

Assumptions

- Tower coordinates are known accurately.
- Distance measurements are available.
- The problem is represented in a 2D coordinate system.
- Measurement errors are limited.
- The input values fall within valid bounds.
- The linear system has a valid solution.

Real-world limitations

Actual positioning systems may experience:

- Signal noise
- Multipath effects
- Measurement inaccuracies
- Atmospheric effects
- Clock errors
- Coordinate-system differences

---

🔮 12. Future Scope

The project can be extended considerably.

Planned / Possible Improvements

- [ ] Real-time simulation
- [ ] Interactive distance controls
- [ ] Measurement-noise simulation
- [ ] Error visualization
- [ ] Accuracy calculation
- [ ] Real geographic maps
- [ ] 3D trilateration
- [ ] Multiple-object positioning
- [ ] Real-time data integration
- [ ] Cloud/API integration
- [ ] Matrix-based solution visualization
- [ ] Automatic equation generation
- [ ] Exportable results
- [ ] Automated testing
- [ ] Web deployment

---

🧠 13. Learning Outcomes

Through this project, the team explored the connection between mathematical theory and software implementation.

Mathematical Learning

- Circle equations
- Coordinate geometry
- Linear equations
- Matrix representation
- Numerical methods
- Mathematical modelling

Programming Learning

- Python
- NumPy
- SymPy
- Matplotlib
- HTML
- CSS
- JavaScript
- Google Colab

Software Engineering Learning

- Git
- GitHub
- Repository organization
- Documentation
- Iterative development
- Visualization
- AI-assisted development

---

📂 14. Project Structure

The repository is based around the Google Colab implementation:

CYBER_ANALYST/
│
├── CyberAnalyst.ipynb
│
├── README.md
│
└── assets/
    │
    └── screenshots/
        ├── day1-setup.png
        ├── day2-mvp.png
        └── day3-analysis.png

As the project evolves, additional Python, JavaScript, CSS, testing, and configuration files can be added.

---

🛠️ 15. How to Run

Google Colab

Open the notebook in Google Colab and execute the cells sequentially.

The notebook renders the GeoTrack interface and mathematical visualization.

Basic workflow

Open Notebook
      ↓
Run Cells
      ↓
Enter / Load Simulation Data
      ↓
Execute Calculation
      ↓
View Numerical Result
      ↓
View Visualization
      ↓
Analyze Mathematics

---

🔀 16. Git Workflow

The project can be developed collaboratively using Git and GitHub.

Example workflow:

git clone <repository-url>
cd CYBER_ANALYST

Create a feature branch:

git checkout -b feature/trilateration-improvement

Commit changes:

git add .
git commit -m "feat: improve trilateration visualization"

Push the branch:

git push origin feature/trilateration-improvement

Then create a Pull Request for review.

---

👥 17. Team Information

Team Name

CYBER ANALYSTS

Project: GPS Trilateration Simulator — A6

Category: Mathematics Mini Project — ABHIYAN

---

Team Members

Name| Roll Number
Lakshman Rawat| "26B21A4631"
G.Y. Mohan Reddy| "26B21A4635"
V. Chaitanya Sai Teja| "26B21A4629"
P. Hari Charan| "26B21A4626"

---

🎯 18. Project Objective

The primary objective of this project is to demonstrate that mathematical concepts taught in engineering mathematics can be applied directly to real-world technological problems.

The project transforms:

Mathematical Theory
        ↓
Mathematical Model
        ↓
Algorithm
        ↓
Python Implementation
        ↓
Visualization
        ↓
Real-World Interpretation

This approach helps bridge the gap between classroom mathematics and software-based problem solving.

---

⭐ 19. Conclusion

The GPS Trilateration Simulator (A6) demonstrates how a positioning problem based on circle equations can be transformed into a system of linear equations.

The project combines:

Mathematics
    +
Programming
    +
Visualization
    +
Real-World Application

to provide an interactive way of understanding trilateration.

The most important mathematical idea demonstrated by this project is:

«A nonlinear-looking problem can sometimes be transformed into a linear system through algebraic manipulation.»

---

<p align="center">📍 GeoTrack

GPS Trilateration Simulator — A6

TEAM CYBER ANALYSTS

Mathematics • Programming • Visualization • Real-World Applications

</p>