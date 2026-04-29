# Build Report: GenCircuitLab
**Date:** 2026-04-29
**Live URL:** https://gencircuitlab.vercel.app
**GitHub:** https://github.com/middesurya/daily-webapp-2026-04-29-gencircuitlab

## Idea Selection

### Why Synthetic Biology?
- Synthetic biology is a massive 2026 trend: precision fermentation, CRISPR biosensors, genetic logic gates
- April 2026 publications in Advanced Science (Wiley) on next-gen synthetic biosensors
- Frontiers in Synthetic Biology published on broadening the toolbox of regulatory devices
- No interactive genetic circuit design tools exist as standalone zero-dependency web apps
- Deeply scientific, not covered in any previous daily webapp

### Scoring
- Novelty: 9/10 (3x) = 27
- Feasibility: 8/10 (3x) = 24
- Wow Factor: 9/10 (2x) = 18
- Learning Value: 10/10 (2x) = 20
- Utility: 8/10 (1x) = 8
- **Total: 97/110**

## Architecture

### Single HTML file (74KB, 1728 lines)
- Pure HTML/CSS/JS, zero dependencies
- Canvas-based rendering for all visualizations
- RK4 ODE solver for deterministic simulation
- Gillespie SSA for stochastic simulation
- Responsive CSS Grid layout

### 6 Modules Built
1. **Genetic Toggle Switch** — Gardner et al. (2000), bistable circuit, phase portrait with nullclines, bifurcation diagram
2. **Repressilator** — Elowitz & Leibler (2000), 3-gene oscillator, 3D phase space with rotation, period detection
3. **CRISPR Logic Gates** — 9 gate types (NOT, AND, OR, NAND, NOR, XOR, XNOR, IMPLIES, Half Adder), truth tables, transfer functions
4. **GRN Builder** — Interactive drag-and-drop network canvas, auto-ODE generation, 3 presets
5. **Stochastic Gene Expression** — Full Gillespie SSA, ensemble statistics, Fano factor, noise decomposition
6. **Metabolic Flux Analysis** — 3 metabolic models, heuristic FBA solver, phenotype phase plane

## Lessons Learned
- Canvas API is efficient for scientific visualizations — no need for D3.js or Chart.js
- RK4 integrator handles stiff systems well enough for these biological models
- Gillespie SSA performance is acceptable for ~500 time units with 4 reactions
- Simplified FBA solver (heuristic, not full LP) is sufficient for educational purposes
- 3D phase space rotation with simple perspective projection works well

## Tech Decisions
- Single HTML over React: faster load, zero build, perfect for educational tool
- Canvas over SVG: better performance for real-time animations (toggle switch, repressilator run continuously)
- Inline data over fetch: follows lesson #1 from CRITICAL BUILD LESSONS
