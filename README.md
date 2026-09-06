# Arman Bijari

Computer Engineering undergraduate at **Ferdowsi University of Mashhad** (B.Sc. expected 2027),
and a research intern in the Lise Meitner group *Neurobiosocial* at the
**Max Planck Institute for Human Cognitive and Brain Sciences**, Leipzig.

I work on computational models of the brain and on the numerical and GPU machinery that makes
them tractable. I am drawn to one kind of problem in particular: a modelling assumption that
applied work relies on routinely, but that has never been tested in the regime where it is
actually applied.

---

## Research

**Does an excitation–inhibition shift move the Hurst exponent uniformly across cortex?**
The Hurst exponent is widely used as a regional proxy for E:I balance, but that relationship was
established in a single circuit with no connectome. I am testing whether it survives inside a
connected whole-brain model — 100 coupled reduced Wong–Wang nodes on HCP-YA connectomes,
integrated on GPU with [cuBNM](https://github.com/amnsbr/cuBNM). Two confounds turned out to
matter: the solver's default reuse of a 30-second noise segment corrupts exactly the
low-frequency structure the estimator depends on, and the perturbation parameter is coupled to
mean firing rate.
*MPI CBS Leipzig, Aug 2025 – present. Supervisors: Dr. Sofie Valk, Dr. Amin Saberi.
Repository private pending publication.*

**How much of a memory bank can you discard before anomaly detection degrades?**
A comparative evaluation of five coreset selection methods — submodular Facility Location,
k-means++ medoid, k-medoids, Determinantal Point Processes, and leverage-score sampling — on
PatchCore embeddings for industrial surface-defect detection, at 1/2/5/10% subset sizes, scored
on fidelity, coverage, diversity and stability.
*With Dr. Hamidreza Pourreza, Machine Vision Lab, FUM. Manuscript in preparation.*

**Where should the beacons go?**
A self-directed indoor-positioning pipeline: DXF architectural floor plans → a georeferenced
semantic 3D building model → a continuous Riemannian RF field solved once per beacon by Fast
Marching → BLE beacon placement posed as D-optimal lazy-greedy submodular maximisation over the
Fisher information field, which buys a (1−1/e) approximation guarantee in place of a heuristic.
Extended to coupled multi-floor placement with a concave-truncated Bhattacharyya separability
term that preserves submodularity. Zero-shot, no training corpus, CPU-only inference.

---

## Selected software

- **[JflapTester](https://github.com/ArmanBjr/JflapTester)** — automated judge for JFLAP automata
  assignments. Handles every JFLAP machine type, grades a whole class straight from Moodle
  submissions, exports to Excel. Written to remove the manual grading bottleneck in a course I
  TA; 106 tests under CI.
- **[computer-architecture-lab](https://github.com/ArmanBjr/computer-architecture-lab)** —
  single-cycle RV32I processor in Verilog with a self-checking testbench, a matching Python
  assembler, and a DE2 FPGA port.
- **[ipfs-simple](https://github.com/ArmanBjr/ipfs-simple)** — content-addressed store in C11.
  Blake3 content-defined chunking, so edits deduplicate against earlier versions; thread-pool
  engine behind a UNIX-socket binary API, with a FastAPI gateway.
- **[universities-atlas-europe](https://github.com/ArmanBjr/universities-atlas-europe)** —
  interactive globe of European universities filtered by tuition, living costs, visa rules and
  post-study work rights. Built because the data existed but nowhere in one place.

Most other repositories here are university coursework. They are documented and reproducible,
and their descriptions say plainly what they are.

---

## Teaching

Teaching assistant for **12 courses** in the Department of Computer Engineering at FUM —
programming, data structures, algorithms, AI, operating systems, discrete mathematics, linear
algebra, logic and electrical circuits, signals & systems, automata theory.

Invited to deliver all three official training workshops of the second edition of *CodeStorm*,
a national ICPC-style contest — [greedy algorithms](https://www.aparat.com/v/wqj6fnj),
[dynamic programming and divide-and-conquer](https://www.aparat.com/v/ljiuwq0),
[graph algorithms](https://www.aparat.com/v/rhumhe9) — roughly 6.5 hours to 200+ participants.
Also a [lecture in English on SchemDraw](https://youtu.be/gnwauqgZ_n8) for the Electrical &
Electronic Circuits course, and co-author of the open-access textbook
[*Mastering Electronics with PySpice & SchemDraw*](https://www.researchgate.net/publication/396700586_Mastering_Electronics_with_PySpice_SchemDraw).

---

## Tools

Python, C, C++, Java, Verilog. PyTorch and scikit-learn for modelling; NumPy/SciPy and CUDA
workflows for simulation; pytest, Docker and CMake for keeping results reproducible — config
hashing, run manifests, seed control, and figures that regenerate from a single command.

---

Applying for MSc study in computational neuroscience and simulation science, Fall 2027.
Open to research collaboration.

[Email](mailto:armanbijari5@gmail.com) · [LinkedIn](https://www.linkedin.com/in/armanbijari/) · [Telegram](https://t.me/Arman_Bjr)
