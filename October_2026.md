# October 2026

**2026-10-20**
* **Hours:** 4
* **Project Work (SnipToolKit — Online Compiler: Bug Fixes, Edge Cases, TypeScript):**
  * Active development session on the SnipToolKit online compiler feature. Work split across three areas:
    1. *Edge Case Identification:* Systematically triggered boundary conditions in the compiler interface — empty input, malformed code, extremely long inputs, rapid sequential submissions, and browser tab switching mid-execution. Documented each failure mode before patching.
    2. *TypeScript Debugging:* Traced and resolved type errors surfaced during testing; tightened type definitions to eliminate implicit `any` usage; ensured function signatures correctly reflect nullable and optional return states where compiler output can be undefined or an error object.
    3. *Bug Fixing & Regression Testing:* Fixed identified bugs and re-ran the full test suite after each patch to confirm no regressions. Verified compiler output rendering, error message display, and execution state management across fixed cases.

---

**2026-10-19**
* **Hours:** 3
* **AI Prompt Engineering (Structure, Techniques, and Use Cases):**
  * Studied the principles and mechanics of effective prompt design for large language models in sequential order from fundamentals to applied patterns:
    1. *Core Prompt Anatomy:* Five structural elements every high-quality prompt should contain: (i) Persona/Role — assign a specific professional identity to specialise model behaviour; (ii) Task/Action — use direct action verbs (write, compare, classify, summarise) rather than open-ended questions; (iii) Context and Background — supply relevant data, audience details, or situational framing upfront; (iv) Constraints and Boundaries — hard limits on length, tone, format, and explicit exclusions; (v) Output Format — specify the exact delivery shape (bullet list, markdown table, numbered steps, word-capped paragraph).
    2. *Zero-Shot Prompting:* Issuing a direct task with no examples; relies entirely on the model's pre-trained knowledge. Best suited for well-defined, unambiguous tasks where format flexibility is acceptable.
    3. *Few-Shot Prompting:* Providing 2-3 concrete input-output demonstration pairs inside the prompt; the model infers the desired style, tone, and structure from the pattern and applies it to the new input. Effective for enforcing custom formats the model would not adopt zero-shot.
    4. *Chain-of-Thought (CoT) Prompting:* Instructing the model to reason step-by-step before producing a final answer (trigger phrase: think step by step or walk through your reasoning). Measurably improves accuracy on multi-step arithmetic, logic, and causal inference tasks by externalising intermediate reasoning into the token stream.
    5. *Role-Based Prompting:* Framing the entire query around a domain persona (e.g., You are a senior systems architect reviewing this design for failure modes) to shift the model into specialised vocabulary, critical posture, and depth of analysis appropriate to that role.
    6. *Prompt Chaining:* Decomposing a complex, multi-stage goal into a linear sequence of smaller, dependent prompts where each output feeds as context into the next. Avoids context overload and keeps intermediate outputs reviewable and correctable before the chain progresses.
    7. *Applied Use Cases by Domain:* Content and copywriting (blog posts, email hooks, video scripts); coding and technical work (code generation, debugging, unit test generation, algorithm explanation); data analysis (report summarisation, document extraction, structured table formatting); business strategy (brainstorming, agenda drafting, marketing outlines).

---

**2026-10-18**
* **Hours:** 5
* **AI Ethics & Responsible AI (6-Module Survey):**
  * Covered the foundations, dilemmas, technical safeguards, legal frameworks, corporate governance, and frontier risks of ethical AI in sequential dependency order:

  * **Module 1 — Foundations & Why Ethics Matters:**
    1. *The AI Stack:* Situated ML, Deep Learning, Generative AI, and Agentic AI on a capability ladder; defined where human oversight currently fails at each layer.
    2. *The Black Box Problem:* Why deep networks (especially transformers) produce decisions that cannot be mechanistically traced by their own builders; distinguished opacity from unpredictability.
    3. *Intent vs. Impact Gap:* How formally correct, well-intentioned systems produce discriminatory or harmful real-world outcomes when deployed outside their training distribution.
    4. *Ethics vs. Law:* Regulatory lag — why legislation operates on decade timescales while model capabilities compound annually; ethics as the interim operating constraint for practitioners.

  * **Module 2 — Core Ethical Dilemmas:**
    5. *Algorithmic Bias & Fairness:* Historical data encodes past discrimination; trained models inherit and automate it at scale. Studied COMPAS recidivism predictor and hiring-filter case studies.
    6. *Privacy & Mass Surveillance:* Data scraping pipelines, facial recognition accuracy disparities across demographic groups (NIST FRVT findings), and the erosion of contextual integrity in personal data.
    7. *Autonomy & Deepfakes/Synthetic Media:* Generative media as an attack surface on public epistemic trust; non-consensual synthetic imagery; disinformation at scale and detection limitations.
    8. *Future of Work:* Displacement vs. augmentation debate; algorithmic management systems (Uber, Amazon warehouse) that set pace, evaluate performance, and terminate without human review.
    9. *Environmental Cost:* Training compute footprint (GPT-3 = ~552 tCO2e); inference-at-scale water consumption for cooling; carbon cost vs. capability gain as a governance variable.

  * **Module 3 — Technical Pillars of Trustworthy AI:**
    10. *Explainability & Interpretability (XAI):* Local explanations (LIME, SHAP) vs. global interpretability (attention maps, saliency); distinction between post-hoc explanation and inherently interpretable models.
    11. *Robustness & Security:* Adversarial examples (FGSM, PGD attacks), data poisoning (backdoor triggers in training sets), model inversion (reconstructing training data from outputs), membership inference attacks.
    12. *Transparency & Provenance:* Model Cards (Mitchell et al.) for documenting intended use, performance metrics, and limitations; Data Nutrition Labels for dataset lineage, collection method, and known biases.
    13. *Human-in-the-Loop (HITL):* Design patterns for meaningful human oversight — override mechanisms, audit trails, confidence thresholds for deferral, and avoiding automation bias where humans rubber-stamp AI outputs.

  * **Module 4 — Global Legal Landscape:**
    14. *EU AI Act (2024):* World''s first risk-based AI regulation. Four tiers: Prohibited (social scoring, real-time biometric surveillance in public), High-Risk (credit, hiring, critical infrastructure), Limited-Risk (disclosure obligations for chatbots), Minimal-Risk (spam filters, AI games).
    15. *US Regulatory Approach:* Executive Order 14110 (Oct 2023) on AI safety; NIST AI RMF as voluntary industry standard; Blueprint for an AI Bill of Rights (OSTP); fragmented state-level laws (Illinois BIPA, California CPRA).
    16. *Global South & UNESCO Framework:* UNESCO Recommendation on the Ethics of AI (2021) — 193 member states; digital colonialism critique (data extracted from Global South, value captured in Global North); equity and data sovereignty provisions.
    17. *Intellectual Property & Copyright:* Training data scraping legality (ongoing US litigation — NYT v. OpenAI, Getty v. Stability AI); output ownership ambiguity; fair use doctrine applied to model training.

  * **Module 5 — Corporate AI Governance:**
    18. *Governance Lifecycle:* Standardised AI system lifecycle: Design (requirements + ethics review) → Develop (bias auditing during training) → Deploy (staged rollout, monitoring hooks) → Monitor (drift detection, incident response).
    19. *Organizational Roles:* AI Ethics Officer mandate and authority; Cross-Functional AI Review Boards (legal, engineering, product, affected-communities representation); Risk Committees with escalation triggers.
    20. *NIST AI RMF:* Four core functions — Govern (culture, accountability), Map (context and risk identification), Measure (quantify risk with metrics), Manage (prioritize, respond, monitor). Framework profiles for sector-specific deployment.
    21. *Auditing & Red-Teaming:* Independent adversarial evaluation before release; structured red team roles (attacker, monitor, scribe); pre-deployment bias audits vs. post-deployment monitoring; responsible disclosure pipelines.

  * **Module 6 — Frontier & Future Risks:**
    22. *Frontier Risk Management:* Emergent capabilities in large models that appear discontinuously and were not present at smaller scale; evaluating dangerous capability thresholds (CBRN uplift, cyberoffense, deception).
    23. *Agentic AI Ethics:* The ethical shift when AI moves from generation to autonomous action — executing code, calling APIs, making purchases; minimal footprint principle, reversibility requirements, and sandboxing.
    24. *Alignment Theory:* The technical challenge of specifying and maintaining human-compatible objectives in increasingly capable systems; reward hacking, goal misgeneralization, and the inner/outer alignment distinction.

---

**2026-10-17**
* **Hours:** 9
* **Computer Architecture (Full Curriculum — 24-Part Deep Dive):**
  * Covered computer architecture from binary fundamentals through GPU/VLIW execution, cache mathematics, multicore coherence, DRAM internals, and Networks-on-Chip in six sequential phases:

  * **Phase 1 — Foundations (Parts 1–4):**
    1. *Bits, Bytes & Number Systems:* Binary, decimal, hexadecimal conversions; two's complement; powers of 2 as design constants (2^10=1K, 2^20=1M, 2^30=1G); logarithm rules for bit-width estimation.
    2. *How Computers Work:* CPU, memory, registers, ALU; the fetch–decode–execute cycle; data path vs control path; why registers exist instead of operating directly on RAM.
    3. *Instruction Formats:* Opcode fields, register fields, immediate fields; R/I/J format comparison; addressing modes (immediate, register, direct, indirect, base+offset); stack machines and push/pop semantics; big-endian vs little-endian byte ordering.
    4. *Performance Mathematics:* Clock rate (Hz), cycle time (1/f), CPI (cycles per instruction), IPC (instructions per cycle), CPU execution time = Instruction Count × CPI × Cycle Time; Amdahl's Law for speedup; latency vs throughput distinction.

  * **Phase 2 — Processor Execution (Parts 5–8):**
    5. *RISC vs CISC & Pipelining:* RISC philosophy (fixed-length instructions, load/store architecture, large uniform register file); five-stage pipeline: IF → ID → EX → MEM → WB.
    6. *Pipeline Timing & Metrics:* Single-cycle vs pipelined execution time; pipeline speedup = number of stages (ideal); cycle time limited by slowest stage; stalls (bubbles) and their CPI cost; throughput = 1 instruction/cycle at steady state.
    7. *Hazards:* Data hazards (RAW — true dependency, WAR — anti-dependency, WAW — output dependency); structural hazards (shared hardware resource conflicts); control hazards (branch decision delay); forwarding/bypassing paths to eliminate RAW stalls without flushing.
    8. *Branch Prediction:* Branch penalty calculation; Branch Prediction Buffers (BPB) indexed by PC; Branch Target Buffers (BTB) for target address caching; 1-bit predictor (state flips on misprediction); 2-bit saturating counter (requires two consecutive mispredictions to change prediction); floating-point pipeline latency and structural hazard patterns.

  * **Phase 3 — Advanced Execution (Parts 9–12):**
    9. *Instruction-Level Parallelism (ILP):* Loop unrolling to expose independent instructions; static scheduling to fill delay slots; true vs name dependencies; anti-dependency and output dependency elimination via renaming.
    10. *Dynamic Scheduling — Tomasulo's Algorithm:* Reservation stations per functional unit; operand capture from Common Data Bus (CDB) on result broadcast; issue, execute, write-result stages; out-of-order execution with in-order issue.
    11. *Reorder Buffer (ROB) & Speculation:* ROB entries track instruction state (issue → execute → write → commit); in-order commit preserves precise exceptions; register renaming via ROB tags eliminates WAR/WAW hazards; branch misprediction causes ROB flush and re-fetch from correct path.
    12. *Parallelism Variants:* Coarse-grained vs fine-grained vs simultaneous multithreading (SMT/Hyper-Threading); superscalar (multiple issue slots, hardware detects parallelism); VLIW (compiler-scheduled multiple operations per instruction word); SIMD (single instruction, multiple data lanes); GPU architecture: thousands of lightweight SIMD cores, thread blocks, warps, and global/shared memory indexing.

  * **Phase 4 — Memory Hierarchy & Caches (Parts 13–16):**
    13. *Memory Hierarchy Basics:* Registers → L1 → L2 → L3 → DRAM → SSD; SRAM (fast, expensive, 6T cell, used in caches) vs DRAM (slow, dense, capacitor cell, refreshed); temporal and spatial locality as the justification for cache existence; average memory access time (AMAT) formula.
    14. *Cache Address Decomposition:* Block offset bits = log2(block size); index bits = log2(number of sets); tag bits = address bits − index − offset; direct-mapped, n-way set-associative, and fully-associative organizations; worked address decomposition problems.
    15. *Cache Miss Classification & Policies:* Compulsory (cold start), capacity (working set too large), conflict (set thrashing) misses; replacement policies: LRU, FIFO, pseudo-LRU (tree-based); write-through + write-allocate vs write-back + write-allocate tradeoffs; dirty bit, valid bit, tag.
    16. *Cache Optimization:* Victim caches (catch conflict evictions); multilevel cache inclusion/exclusion; hardware prefetching; early restart (supply partial cache line before fill completes); critical word first; miss penalty = L2 access time + L3 access time × miss rate; AMAT minimization strategies.

  * **Phase 5 — Multicore Memory & I/O (Parts 17–20):**
    17. *Cache Coherence & Consistency:* Why per-core private caches create stale-data problems; write-propagate (update) vs write-invalidate (invalidate on write) protocols; bus snooping (all caches observe every transaction); directory-based coherence for scalable multiprocessors; sequential consistency model.
    18. *MESI Protocol:* Four stable states — Modified (dirty, exclusive), Exclusive (clean, exclusive), Shared (clean, multiple readers), Invalid; full state-transition diagram on read/write hits and misses; false sharing (two threads access different variables in the same cache line, causing ping-pong invalidations); directory entry storage cost = 2 bits × number of processors per cache line.
    19. *DRAM Internals & Disk Scheduling:* Row/column address multiplexing; CAS (Column Address Strobe) latency; refresh cycles and tRFC timing; channels, ranks, banks, and interleaving for parallelism; disk scheduling algorithms — FCFS, SSTF, SCAN (elevator), C-SCAN; seek time + rotational latency + transfer time = total access time.
    20. *Networks-on-Chip (NoC):* Why off-chip buses bottleneck at many cores; mesh topology (k×k grid, bisection bandwidth = 2k links); router micro-architecture: route computation, virtual channel allocation, switch allocation, switch traversal, link traversal (5 pipeline stages); flits (flow control units) vs phits vs packets; virtual channels for deadlock freedom; wormhole vs store-and-forward flow control.

  * **Phase 6 — Advanced NoC & Revision (Parts 21–24):**
    21. *Adaptive Routing & Arbitration:* Oblivious (deterministic) vs adaptive routing; counting minimal paths in mesh; arbitration schemes — round-robin, age-based (oldest packet first); output port selection; avoiding livelock in adaptive routing.
    22. *Advanced NoC Architectures:* CHIPPER (bufferless deflection router); DeBAR, BLESS, MinBD (bufferless designs); SLIDER (stochastic latency); PDN (priority deflection network); BEU (bypass express unit); central buffer pool designs and their area/power tradeoffs vs distributed buffering.
    23. *Advanced Topics:* Network slack (latency tolerance for traffic shaping); memory-level parallelism (MLP) and its interaction with NoC latency; network sensitivity analysis; core-to-cache mapping strategies in tiled architectures; advanced L2 cache indexing (XOR-based, skewed).
    24. *Full Revision & Mock Test:* Integrated problem set spanning all six phases — binary conversion, pipeline timing diagrams, Tomasulo issue/execute/write tables, cache address decomposition, MESI state transitions, and NoC routing hop-count calculations.

---

**2026-10-16**
* **Hours:** 4
* **Academic Engineering (DBMS — Relational Algebra):**
  * Covered the complete formal query language underlying SQL, in dependency order from primitive to derived operators:
    1. *Primitive Unary Operators:* Selection (sigma) for horizontal filtering by condition, Projection (pi) for vertical filtering by attribute columns, and Rename (rho) for schema aliasing.
    2. *Primitive Set Operators:* Union, Intersection, and Set Difference applied to union-compatible relations. Studied cardinality behavior for each operation.
    3. *Relational Comparison & Conditions:* Compound predicates using AND, OR, NOT. Comparison operators across attribute domains and their mapping to SQL WHERE clauses.
    4. *Join Operators:* Cartesian Product (base), Theta Join (generalised condition), Equi-Join (equality-only condition), Natural Join (automatic attribute matching), Semi-Join, and Anti-Join. Studied output schema and tuple count for each.
    5. *Division Operator:* Relational division for queries of the form find tuples related to ALL values in another relation. Mapped to its SQL equivalent using NOT EXISTS / EXCEPT.
    6. *Extended Operators:* Grouping (gamma) with aggregate functions and Ungrouping. How these map to GROUP BY and ROLLUP/CUBE in SQL.

---

**2026-10-15**
* **Hours:** 6
* **Code & Data Science (Data Visualization Stack + NumPy Deep Dive):**
  * Covered the complete Python visualization ecosystem in structured order from foundational charts to statistical distributions:
    1. *Core Chart Types (Matplotlib):* Bar charts, pie charts, scatter plots, and histograms. Practised axis labeling, text alignment, title placement, and custom tick formatting.
    2. *Statistical Distribution Plots (Matplotlib + Seaborn):* Box plots (IQR, whiskers, outlier detection), violin plots (kernel density estimation mirrored around a center axis), and swarm plots (non-overlapping jittered points showing full data distribution).
    3. *Seaborn Integration:* Layering Seaborn statistical plots on Matplotlib Axes objects. Understood how Seaborn is a high-level wrapper around Matplotlib using the same Figure/Axes architecture under the hood.
    4. *Text Annotation & Layout:* Word clouds for frequency-weighted text visualization. Axis text alignment controls, annotation placement, and multi-subplot layout management.
    5. *NumPy (Mathematical & Statistical Functions):* Revisited and deepened understanding of array attributes (shape, dtype, ndim, size, strides). Practiced mathematical ufuncs (np.sqrt, np.log, np.exp, np.power) and statistical aggregations (np.mean, np.median, np.std, np.var, np.percentile, np.corrcoef).

---

**2026-10-14**
* **Hours:** 6
* **Academic Engineering (DBMS — Foundations to Indexing for University Exams):**
  * Covered the full DBMS stack in sequential order from relational theory to physical storage structures:
    1. *Relational Model Foundations:* Relations, attributes, degree (number of attributes), cardinality (number of tuples), and static vs. dynamic relations.
    2. *Keys & Constraints:* Super key, candidate key, primary key, foreign key, and composite key. Enforcing referential integrity and constraint propagation across tables.
    3. *SQL Command Architecture:* DDL (CREATE, ALTER, DROP), DML (INSERT, UPDATE, DELETE), TCL (COMMIT, ROLLBACK), and DCL (GRANT, REVOKE) — reviewed their execution context within transaction boundaries.
    4. *Storage & Indexing — B-Trees and B+ Trees:* Structural differences between B-Trees (data stored at all nodes) and B+ Trees (data only at leaf nodes, linked list at leaves). Insertion, deletion, and search time complexity. Why RDBMS engines (MySQL InnoDB, PostgreSQL) exclusively use B+ Trees for secondary indexing.
    5. *Hashing & Collision Resolution:*
       * Static Hashing: Open addressing (linear probing, quadratic probing, double hashing) vs. Separate chaining.
       * Dynamic/Extensible Hashing: Global depth, local depth, bucket splitting, and directory doubling mechanics. All associated formulas and bit-manipulation concepts for bucket address calculation.
  * Studied all standard formulas for hashing, tree height, and space utilization across indexing methods.

---

**2026-10-13**
* **Hours:** 3
* **Code & Data Science Foundations (NumPy & Matplotlib Deep Dive):** 
  * *NumPy (Array Manipulation & Vectorization):*
    * Practiced multi-dimensional slicing and advanced boolean masking (filtering arrays via conditional indexing).
    * Experimented with array broadcasting rules across mismatched shapes to understand memory layout and dimension expansion.
    * Implemented axis-specific aggregations (\xis=0\ vs \xis=1\) and basic matrix operations (p.dot\, matrix transpositions).
  * *Matplotlib (Visualization & Object-Oriented API):*
    * Transitioned from standard stateful plotting to the Object-Oriented API using \plt.subplots()\, manipulating \Figure\ and \Axes\ objects directly.
    * Built multi-panel plots, distribution histograms, and scatter plots mapped to synthetic datasets.
    * Configured plot aesthetics: custom markers, gridlines, axis scaling, legends, and layout padding via \plt.tight_layout()\.
  * *Key Takeaway:* Practiced feeding vectorized NumPy transformations directly into visualization pipelines without relying on inefficient Python loops.

---

**2026-10-12**
* **Hours:** 7
* **Academic Engineering (OOP & C++ Deep Dive for University Exams):** 
  * Structured and revised Object-Oriented Programming concepts from foundational mechanics to runtime dispatch:
    1. *Object Mechanics & Lifecycle:* Member functions, friend functions, constructors (types, initialization lists), and destructors.
    2. *Inheritance Hierarchies:* Single, multiple, multilevel, hierarchical, and hybrid inheritance; member access control (public, protected, private).
    3. *Compile-Time (Static) Polymorphism:* Function overloading, unary operator overloading, and binary operator overloading.
    4. *Run-Time (Dynamic) Polymorphism:* Function overriding, virtual functions (vtable/vptr mechanics), and virtual base classes (resolving the diamond problem).
    5. *Robustness & Control Flow:* Exception handling fundamentals (	ry, catch, 	hrow) and defining custom user-defined exceptions.
  * Wrote and analyzed concrete code implementations exploring edge cases for each paradigm.

---

**2026-10-11**
* **Hours:** 6
* **Academic Engineering (Software Engineering Exam Prep):** 
  * Completed an intensive, structured revision of the Software Engineering lifecycle:
    1. *Requirements Engineering:* Requirements analysis, Software Requirements Specification (SRS), and Data Dictionaries.
    2. *System Design & Modeling:* Data Flow Diagrams (DFD), Entity-Relationship (ER) diagrams, and Unified Modeling Language (UML).
    3. *Estimation & Project Management:* Software Project Management (SPM), size estimation, effort/cost modeling via the COCOMO model, and project scheduling using Gantt charts.
    4. *Risk Management:* Risk identification, assessment, and mitigation planning.

---

**2026-10-10**
* **Hours:** 1
* **Code (NumPy):** 
  * Transitioned from theory to practical code execution (prep for upcoming university exams).
  * Practiced creating, reshaping, and manipulating 1D and 2D 
p.array structures.
  * Wrote scripts to test array slicing, vectorization concepts, and core mathematical/statistical functions.

---

**2026-10-09**
* **Hours:** 5
* **Code (Data Science Stack):** 
  * Studied the theoretical foundations of NumPy: explored 
darray attributes, data types, array creation methods, and core applications.
  * Reviewed Matplotlib fundamentals: understanding the hierarchy of figures, subplots, and basic charting/graphing capabilities.
  * *Note:* Heavy theory day. Need to ensure this is immediately followed up by practical coding implementation tomorrow so the concepts don\'t fade.

---

**2026-10-08**
* **Hours:** 1
* **Code (SQL):** 
  * Practiced the core SQL command categories: DDL (Definition), DML (Manipulation), TCL (Transaction Control), and DCL (Data Control).
* **Blocker / Status:** 
  * University exams, assignments, and projects are heavily starting to eat into my time and focus. 
  * *Note:* Experiencing the classic collision between the academic workload and actual engineering skill-building. Need to tightly manage my time so this doesn\'t derail my daily momentum.

---

**2026-10-07**
* **Hours:** 1
* **Code (SQL):** 
  * Studied fundamental SQL aggregate functions: COUNT(), SUM(), AVG(), and MIN().
  * Practiced using the GROUP BY clause to aggregate data across categories.
  * Reinforced basic database querying structures and syntax.

---

**2026-10-06**
* **Hours:** 1
* **Code (Python):** 
  * Practiced foundational coding questions centered on functions.
  * Reviewed the mechanics of function definitions, syntax, and execution flow.
  * *Blocker:* Still experiencing some confusion around function definitions—specifically how parameters map to arguments and how the code execution jumps when a function is called.

---

**2026-10-05**
* **Hours:** 2
* **Code (Python):** 
  * Continued practicing * pattern loops and studying the underlying mathematical logic. 
  * *Blocker:* Confused about how to dynamically handle user input for sizing the pattern grids.
  * Started learning functions: definitions, calling, default arguments, and parameters. 
  * Explored the concept of recursion and base cases, and how functions improve code reusability.

---

**2026-10-04**
* **Hours:** 6
* **Code (Python):** Practiced nested loops by building `*` pattern shapes. 
  * *Blocker:* Found it difficult to manage indentation, calculate exact spaces, and set the correct `range()` boundaries for inverted shapes. 
  * *Status:* Still working on fully grasping how the inner and outer loops interact with spaces.
* **Reading (Research):** Studied YOLO object detection models applied to weapon detection. Focused on understanding their performance metrics and current limitations. Also read up on global market insights.
* **Side Quest (Sniptoolkit):** 
  * Polished the UI for our team's website (`sniptoolkit`). 
  * Stress-tested the compiler using extreme AI-generated edge cases. 
  * Deployed the changes to a `workers.dev` preview environment.
