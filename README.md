# CYBER_ANALYST

GeoTrack — GPS Trilateration Simulator

<p align="center">
  <strong>TEAM A6 • B.Tech Mathematics</strong>
</p><p align="center">
  An interactive GPS trilateration simulator that demonstrates how a position can be estimated from distance measurements using systems of linear equations.
</p><p align="center">
  <img src="https://img.shields.io/badge/Project-GPS%20Trilateration-18d6a5?style=for-the-badge" alt="Project">
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" alt="Google Colab">
  <img src="https://img.shields.io/badge/HTML-CSS-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML CSS">
  <img src="https://img.shields.io/badge/Team-A6-3776AB?style=for-the-badge" alt="Team A6">
</p>---

Overview

GeoTrack is a mathematical visualization project built around the idea of GPS trilateration.

The project demonstrates how three distance measurements from known reference points can be represented as three circles. The intersection of these circles gives an estimate of the unknown position.

Instead of treating GPS positioning as a black-box technology, GeoTrack breaks the problem down into a mathematical process that students can visualize and understand.

Core idea

«Three known points + three measured distances → three circle equations → system of linear equations → estimated position "(x, y)"»

This project connects linear algebra, coordinate geometry, and a real-world positioning problem.

---

Problem Statement

Three cell towers detect a mobile phone at distances:

- "d₁" from Tower 1
- "d₂" from Tower 2
- "d₃" from Tower 3

Each distance defines a circle around its corresponding tower.

The unknown phone location "(x, y)" must satisfy all three circle equations.

For a tower at "(xᵢ, yᵢ)" with measured distance "dᵢ":

(x - xᵢ)² + (y - yᵢ)² = dᵢ²

Although these equations initially contain squared terms and are therefore nonlinear, subtracting pairs of equations eliminates the "x²" and "y²" terms.

This produces a system of linear equations that can be solved for the unknown coordinates.

---

Why This Project?

GPS and location technologies are used every day, but the mathematics behind positioning can feel abstract.

GeoTrack makes the concept visual.

Instead of only solving equations on paper, the simulator provides a graphical representation of:

- Reference towers
- Distance circles
- Estimated location
- Coordinate relationships
- Mathematical derivation

The goal is to connect classroom mathematics with a practical technology used in navigation and communication systems.

---

Key Features

Interactive Simulator

The simulator is designed around a visual coordinate-map interface where reference points and distance circles can be represented graphically.

GPS Trilateration Visualization

Three distance measurements can be represented as circles around known reference points.

Their intersection represents the estimated position.

Mathematical Explanation

The project includes a dedicated mathematics section explaining how the original circle equations are transformed into a system of linear equations.

Sensitivity Analysis

The interface includes a Sensitivity section intended to demonstrate how changes in distance measurements can affect the calculated location.

Responsive Interface

The UI is designed with responsive CSS so the project can adapt to different screen sizes.

Mathematical + Real-World Connection

The project connects:

Coordinate Geometry
        ↓
Circle Equations
        ↓
Algebraic Elimination
        ↓
Linear Equations
        ↓
Position Estimation
        ↓
GPS / Location Technology

---

Mathematical Foundation

Suppose three known towers are located at:

T₁ = (x₁, y₁)
T₂ = (x₂, y₂)
T₃ = (x₃, y₃)

and the unknown phone location is:

P = (x, y)

with measured distances:

d₁, d₂, d₃

Circle equations

For Tower 1:

(x - x₁)² + (y - y₁)² = d₁²

For Tower 2:

(x - x₂)² + (y - y₂)² = d₂²

For Tower 3:

(x - x₃)² + (y - y₃)² = d₃²

Elimination

Subtracting the first equation from the second removes the common "x²" and "y²" terms.

This produces a linear equation of the form:

Ax + By = C

Repeating the process with another pair gives:

Dx + Ey = F

Therefore, the original trilateration problem becomes:

Ax + By = C
Dx + Ey = F

which is a system of two linear equations with two unknowns.

Solving this system gives the estimated coordinates:

P = (x, y)

---

Conceptual Workflow

                ┌─────────────────────┐
                │  Known Tower        │
                │  Coordinates        │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Distance Measurements│
                │      d₁ d₂ d₃       │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Circle Equations    │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Subtract Equation   │
                │ Pairs                │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Linear Equations    │
                │ Ax + By = C         │
                │ Dx + Ey = F         │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Solve for x and y   │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Estimated Position  │
                │       (x, y)        │
                └─────────────────────┘

---

Interface

GeoTrack uses a dark, technical interface designed around a navigation/GPS theme.

Navigation

The interface provides sections for:

- Simulator
- Sensitivity
- Mathematics
- How It Works
- Applications

Visual Design

The interface uses:

- Dark navy background
- Cyan/teal accent color
- Grid-based coordinate visualization
- Interactive-style panels
- Responsive layout
- Satellite/reference-point visualization
- Highlighted estimated position

The visual design is intended to make the mathematical model feel like a small location-analysis dashboard rather than a traditional static assignment.

---

Technology Stack

Technology| Purpose
Python| Google Colab environment and project integration
HTML| Structure of the interface
CSS| UI, layout, animations and responsive design
JavaScript| Intended for interactive simulator behaviour
Google Colab| Development and demonstration environment
Git| Version control
GitHub| Source-code hosting and collaboration

---

Project Structure

The repository can be organized approximately as follows:

CYBER_ANALYST/
│
├── CyberAnalyst.ipynb
├── README.md
│
└── assets/
    └── screenshots/

«If additional source files are added later, update this section so the documentation always reflects the actual repository structure.»

---

Running the Project

Option 1 — Google Colab

The current project is designed to work with Google Colab.

1. Open the notebook.
2. Run the required cells sequentially.
3. The HTML interface will be rendered inside the notebook.
4. Enter the required simulation values.
5. Run the simulator.
6. Explore the mathematical and visualization sections.

Option 2 — Local Development

For a future standalone version, the interface can be separated into:

index.html
style.css
script.js

and served using a local development server.

---

Example

Suppose three towers have known coordinates:

T₁ = (0, 0)
T₂ = (10, 0)
T₃ = (5, 10)

and the measured distances are:

d₁
d₂
d₃

Each measurement produces a circle.

The phone location is the point that satisfies the three distance relationships.

The simulator's objective is to make this mathematical relationship visually understandable.

---

Real-World Applications

The mathematical principle demonstrated by GeoTrack has applications in many areas, including:

- GPS positioning
- Mobile positioning systems
- Wireless sensor networks
- Navigation systems
- Robotics
- Location-aware applications
- Geolocation systems
- Signal-based positioning

The project demonstrates the underlying mathematical idea rather than attempting to reproduce the complete engineering implementation of a commercial GPS receiver.

---

Educational Value

This project demonstrates how a seemingly nonlinear problem can be transformed into a linear algebra problem.

Students can learn:

- Coordinate geometry
- Circle equations
- Systems of linear equations
- Algebraic elimination
- Coordinate-based positioning
- Mathematical modelling
- Visualization of mathematical concepts
- Connection between mathematics and technology

---

Limitations

This project is an educational simulator.

Real-world positioning systems involve additional factors such as:

- Measurement noise
- Signal propagation delay
- Atmospheric effects
- Clock errors
- Multipath propagation
- Three-dimensional coordinates
- Geodetic coordinate systems

Therefore, the simulator should be viewed as a mathematical model rather than a production-grade GPS positioning engine.

---

Future Improvements

Possible future versions could include:

- [ ] Fully interactive distance inputs
- [ ] Automatic trilateration calculation
- [ ] Real-time circle updates
- [ ] Error/noise simulation
- [ ] Position accuracy measurement
- [ ] 2D → 3D trilateration
- [ ] Real geographic map integration
- [ ] Mobile-responsive improvements
- [ ] Exportable simulation results
- [ ] Step-by-step equation generation
- [ ] Matrix-based solution using linear algebra
- [ ] Multiple test scenarios
- [ ] Automated unit tests
- [ ] GitHub Actions CI
- [ ] Standalone web deployment

---

Team

TEAM A6

Project: GeoTrack — GPS Trilateration Simulator

Academic Area: B.Tech Mathematics

Topic: System of Linear Equations from Nonlinear Origins

The project was developed as an academic demonstration of how mathematical modelling can be applied to a real-world positioning problem.

---

Development Philosophy

This project follows a simple principle:

«Don't just solve the equation. Visualize what the equation means.»

The goal is to combine mathematical reasoning with software development so that the underlying mathematics becomes easier to explore, test, and understand.

---

Contributing

Contributions and improvements are welcome.

A typical workflow is:

git clone <repository-url>
cd CYBER_ANALYST

Create a feature branch:

git checkout -b feature/your-feature

Make your changes, test them, and commit:

git add .
git commit -m "Add: description of change"

Push the branch:

git push origin feature/your-feature

Then open a Pull Request on GitHub.

For a larger team project, keeping changes in separate branches and reviewing them through pull requests makes collaboration easier. GitHub also recommends using repository documentation such as README files to communicate project purpose and usage.

---

License

This project does not currently specify an open-source license.

If you intend to allow others to freely use, modify, and distribute the project, add an appropriate "LICENSE" file to the repository.

---

Project Status

Status: Academic Project / Prototype

Current focus: GPS trilateration visualization and mathematical demonstration.

Future releases can evolve the prototype into a complete interactive positioning simulator.

---

<p align="center">
  Built by <strong>Team A6</strong> with mathematics, programming, and curiosity.
</p>