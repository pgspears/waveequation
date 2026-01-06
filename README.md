# Schrödinger's Equation Explorer

An interactive educational web application that provides a comprehensive introduction to Schrödinger's equation—the fundamental equation of quantum mechanics. This app combines detailed explanations, historical context, and hands-on simulations to make quantum mechanics accessible to learners at all levels.

![Quantum Mechanics](https://img.shields.io/badge/Physics-Quantum%20Mechanics-blueviolet)
![Vanilla JS](https://img.shields.io/badge/Built%20With-Vanilla%20JS-yellow)
![License](https://img.shields.io/badge/License-Proprietary-red)

---

## Overview

Schrödinger's equation describes how the quantum state of a physical system evolves over time. Published in 1926 by Erwin Schrödinger, it revolutionized our understanding of atomic and subatomic phenomena and remains the cornerstone of non-relativistic quantum mechanics.

This application breaks down the equation piece by piece, demonstrates it in action through interactive simulations, and places it in historical context—all in a visually engaging, single-page web app.

---

## Features

### 📚 Comprehensive Educational Content

- **Dual-Level Explanations**: Toggle between beginner-friendly and advanced explanations for each term in the equation
- **Term-by-Term Breakdown**: Detailed coverage of every symbol (i, ℏ, ∂/∂t, Ψ, Ĥ) with physical interpretations
- **Step-by-Step Derivation**: Complete walkthrough of solving the particle-in-a-box problem, demonstrating how energy quantization emerges from boundary conditions

### 🔬 Interactive Simulations

#### Particle in a 1D Infinite Square Well
- Visualize wave functions (Ψ) and probability densities (|Ψ|²)
- Adjust quantum number n (1-10) to see different energy eigenstates
- Modify box width L to observe size-dependent effects
- Control animation speed for time evolution
- Toggle visibility of real part, imaginary part, and probability density
- Real-time display of:
  - Energy levels (in electron volts)
  - De Broglie wavelength
  - Number of nodes
  - Oscillation period

#### Quantum Superposition Demonstrator
- Create superpositions of two energy eigenstates
- Adjust mixing ratios to control state composition
- Observe probability density oscillations (quantum beating)
- See the beat frequency emerge from energy differences

### 📜 Historical Timeline

An interactive timeline covering the development of quantum mechanics from 1900-1933:

- **1900**: Planck's quantum hypothesis
- **1905**: Einstein's photon concept
- **1913**: Bohr's atomic model
- **1924**: de Broglie's matter waves
- **1925-26**: Schrödinger's wave equation
- **1926**: Born's probability interpretation
- **1927**: Copenhagen interpretation
- **1933**: Nobel Prize

Includes expandable sections on:
- The famous Christmas vacation story of the equation's discovery
- The wave mechanics vs. matrix mechanics debate

### 🌟 Significance & Applications

Exploration of how Schrödinger's equation impacts:
- Atomic structure and the periodic table
- Chemical bonding and molecular orbital theory
- Semiconductor physics and electronics
- Nuclear physics and radioactive decay
- Quantum biology
- Quantum computing

Additional deep-dive sections on:
- The measurement problem and quantum interpretations
- Schrödinger's cat thought experiment

---

## How to Use

### Getting Started

1. Open `schrodinger-equation-explorer.html` in any modern web browser
2. No installation, build process, or dependencies required
3. Works offline once loaded

### Navigation

Use the fixed navigation bar at the top to jump to any section:
- **The Equation**: Hero section with the main equation display
- **Terms Explained**: Detailed breakdown of each symbol
- **Interactive Simulation**: Hands-on quantum mechanics
- **Step-by-Step**: Worked example solving the particle in a box
- **History**: Timeline of quantum mechanics development
- **Significance**: Real-world applications and philosophical implications

### Using the Particle-in-a-Box Simulation

1. **Quantum Number (n)**: Drag the slider to change energy levels
   - n=1 is the ground state (lowest energy)
   - Higher n means more nodes and higher energy
   - Watch how the wave function develops more oscillations

2. **Box Width (L)**: Adjust the confinement size
   - Smaller boxes → higher energies (E ∝ 1/L²)
   - This demonstrates why quantum effects matter at atomic scales

3. **Animation Speed**: Control how fast time evolves
   - The wave function phase rotates at frequency ω = E/ℏ

4. **Toggle Buttons**:
   - "Show/Hide Ψ": Toggle the wave function display
   - "Show/Hide |Ψ|²": Toggle the probability density
   - "Pause/Resume Time": Freeze or continue the animation

5. **Information Display**: Monitor real-time values for energy, wavelength, nodes, and oscillation period

### Using the Superposition Simulation

1. **State 1 (n₁)** and **State 2 (n₂)**: Select which two energy states to superpose

2. **Mixing Ratio**: Adjust the probability amplitudes
   - 50:50 gives equal weight to both states
   - Moving toward 100:0 emphasizes the first state

3. **Observe**: Watch how the probability density oscillates back and forth—this is quantum beating, with frequency proportional to the energy difference between states

### Exploring Explanations

- Click **"Beginner Explanation"** or **"Advanced Details"** tabs to switch depth levels
- Click any **collapsible section** header (with ▼ arrow) to expand/collapse additional content

---

## Physics Concepts Covered

### The Time-Dependent Schrödinger Equation

```
iℏ ∂Ψ/∂t = ĤΨ
```

Where:
- **i** — Imaginary unit (√-1), ensures unitary time evolution
- **ℏ** — Reduced Planck constant (h/2π ≈ 1.055 × 10⁻³⁴ J·s)
- **∂/∂t** — Partial derivative with respect to time
- **Ψ** — Wave function, contains all quantum information
- **Ĥ** — Hamiltonian operator, represents total energy

### The Time-Independent Schrödinger Equation

```
ĤΨ = EΨ
```

An eigenvalue equation whose solutions give allowed energy levels and stationary states.

### Key Concepts Demonstrated

1. **Quantization**: Only certain discrete energy values are allowed
2. **Wave-Particle Duality**: Particles exhibit wave-like behavior
3. **Probability Interpretation**: |Ψ|² gives probability density
4. **Superposition**: Quantum systems can exist in multiple states simultaneously
5. **Zero-Point Energy**: Confined particles always have non-zero minimum energy
6. **Nodes**: Higher energy states have more zeros in the wave function

---

## Technical Details

### Built With

- **HTML5**: Semantic structure
- **CSS3**: Custom properties, animations, responsive design
- **Vanilla JavaScript**: No frameworks or libraries required
- **Canvas API**: Real-time physics simulations

### Browser Compatibility

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

### Performance

- Lightweight single-file application (~45KB)
- 60 FPS animations using requestAnimationFrame
- Responsive design works on desktop and mobile devices

### Physics Engine

The simulations use accurate quantum mechanical calculations:

```javascript
// Energy eigenvalues
E_n = n²π²ℏ² / (2mL²)

// Normalized wave functions  
ψ_n(x) = √(2/L) sin(nπx/L)

// Time evolution
Ψ_n(x,t) = ψ_n(x) · exp(-iE_n·t/ℏ)
```

Constants used:
- ℏ = 1.054571817 × 10⁻³⁴ J·s
- m_e = 9.10938 × 10⁻³¹ kg (electron mass)
- 1 eV = 1.602176634 × 10⁻¹⁹ J

---

## Educational Applications

This app is suitable for:

- **High School Physics**: Introduction to quantum concepts
- **Undergraduate Courses**: Quantum mechanics, modern physics, physical chemistry
- **Self-Study**: Anyone curious about quantum mechanics
- **Teaching Demonstrations**: Classroom visualization tool
- **Science Communication**: Public outreach and education

### Suggested Learning Path

1. Start at the hero section to see the equation in its full form
2. Read through the beginner explanations of each term
3. Experiment with the particle-in-a-box simulation
4. Follow the step-by-step derivation to understand where the solutions come from
5. Explore superposition to see quantum weirdness in action
6. Review the historical timeline for context
7. Return to advanced explanations for deeper understanding

---

## File Structure

```
schrodinger-app/
├── schrodinger-equation-explorer.html    # Complete application (single file)
└── README.md                              # This documentation
```

---

## Credits

### Physics References

- Griffiths, D.J. *Introduction to Quantum Mechanics* (2018)
- Feynman, R.P. *The Feynman Lectures on Physics, Vol. III* (1965)
- Shankar, R. *Principles of Quantum Mechanics* (1994)

### Historical Sources

- Kumar, M. *Quantum: Einstein, Bohr, and the Great Debate* (2008)
- Isaacson, W. *Einstein: His Life and Universe* (2007)
- Moore, W. *Schrödinger: Life and Thought* (1989)

---

## License

© 2026 Accelerate Solutions, LLC. All rights reserved.

---

## Version History

- **v1.0.0** (2026): Initial release
  - Complete educational content
  - Two interactive simulations
  - Historical timeline
  - Responsive design
