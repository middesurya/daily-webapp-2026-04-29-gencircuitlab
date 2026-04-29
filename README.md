# GenCircuitLab — Interactive Synthetic Biology & Genetic Circuit Design Laboratory

An interactive web laboratory for designing, simulating, and analyzing genetic circuits. Built as a zero-dependency single HTML application.

## 6 Interactive Modules

1. **Genetic Toggle Switch** — Gardner et al. (2000) bistable switch with two mutually repressing genes. ODE simulation (RK4), phase portrait with nullclines, bifurcation diagram showing bistability threshold.

2. **Repressilator** — Elowitz & Leibler (2000) three-gene oscillatory network. Real-time oscillation dynamics, 3D rotating phase space, period/amplitude analysis with peak detection.

3. **CRISPR Logic Gates** — Design Boolean logic gates (NOT, AND, OR, NAND, NOR, XOR, XNOR, IMPLIES, Half Adder) using dCas9/gRNA transcriptional regulation. Truth tables, sigmoidal transfer functions, biological implementation descriptions.

4. **Gene Regulatory Network Builder** — Drag-and-drop circuit designer. Place genes, connect with activation/repression edges, auto-generate ODE system, simulate in real-time. Presets: toggle switch, repressilator, feed-forward loop.

5. **Stochastic Gene Expression (Gillespie SSA)** — Full implementation of the Gillespie Stochastic Simulation Algorithm. Intrinsic vs extrinsic noise decomposition, Fano factor analysis, ensemble statistics, comparison with deterministic ODE.

6. **Metabolic Flux Analysis (FBA)** — Stoichiometric modeling with simplified flux balance analysis. Three metabolic models (core E.coli, fermentation, amino acid biosynthesis). Phenotype phase plane analysis.

## Key References

- Gardner, Cantor & Collins (2000) *Nature* 403:339-342
- Elowitz & Leibler (2000) *Nature* 403:335-338
- Gillespie (1977) *J Phys Chem* 81:2340
- Elowitz et al. (2002) *Science* 297:1183
- Orth, Thiele & Palsson (2010) *Nature Biotechnology* 28:245-248
- Nielsen et al. (2016) *Science* 352:aac7341

## Tech Stack

- Pure HTML/CSS/JavaScript — zero dependencies
- Canvas-based visualizations
- RK4 ODE integration
- Gillespie SSA stochastic simulation
- Responsive design

## License

MIT
