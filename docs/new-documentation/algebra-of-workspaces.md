# Algebra of Workspaces

Version 1.0.0 — 2026-11-07

Built on *Workspace Theory: Axioms and Consequences* (A1–A10, C1–C9), v1.0.0.
## Introduction

The Algebra of Workspaces is an abstract language for reasoning about workspaces in general, and for making statements about them that hold beyond any single case. It was first conceived as a kind of algebraic topology of the workspace: the workspace has a topology — neighborhoods, enclosures, deformations that preserve an invariant — and it has operations that compose, and the algebra is the joint account of the two. It is an abstract algebra, though not rigorous in the mathematical sense; it keeps the level of rigor and comprehensiveness of a formal theory without claiming its formalism.

The algebra treats one workspace at a time. A workspace may contain several workspaces — two collaborators' workspaces, the terminals and archives of a room, the rooms of a house — and in that case they form one united workspace, which is what the algebra describes.

The algebra is not a schema, and it is not a methodology. (ALX is the methodology — a rigorous design workflow management methodology, a separate body of work; the two may connect and share vocabulary, but they are separate.) The algebra is built on Workspace Theory: its terms are the axioms and consequences of that theory (A1–A10, C1–C9), and its subject is what those axioms leave open — the space the workspace lives in, the operations performed in it, and the laws the operations obey.

## 1. Space and its axes

### The space

The workspace is fundamentally a space. Not a container it sits in, but space itself, in the quantum sense: a relational field — felt from inside, by the operator who inhabits it, as a continuous field (le continu), in which every intervention alters the tension of the whole. Its structure is given by **adjacency**: a station, a terminal, a Refcard, a stack has no place except the links it stands in — which other stations, cards, and volumes it is next to. Touching constructs the structure of the space; a neighborhood (**voisinage**) is what stands adjacent, and enclosure (**enveloppement**) is containment within the field — a workspace inside a workspace, a room inside the Historiotheque. The field is **elastic**: its arrangements can be stretched, deformed, and re-clustered without tearing, and what survives every such deformation is the invariant of the topology — **succession, the order of the delta chain**.

**The space is granular.** Underneath the felt continuity, its grains are its discrete units — a configuration, a step, a Refcard, a stack layer, a session — and its nodes are its quanta in this sense: they do not sit inside the space, they constitute it. Working is traversing the resulting graph: always something adjacent to something else, moving between areas of exposed surface and across the volumes of the subsurface — the stacks and strata beneath each surface.

The nodes of this network are **boundary markers**: they delimit the workspace's areas, points, lines, and surfaces — the dimensions of the **human scale** (the term is from architectural theory; the theory measures nothing finer or larger, and its grains are human-scale grains). A link between two adjacent volumes carries an **area**: the surface the two volumes share — the exposed surface between the workspace's air and a stack's depth (A3), the working surface one station presents to its neighbor. The volumes are the workspace's subsurface: the stacks, the archives, the nested workspaces. And every area has a **history**: traced through the delta chain, an area stays constant, grows, shrinks, or meets other areas, and that traced surface — the area's course through the workspace's time — is the history of the area. A boundary marker that persists traces a line through the history; where workspaces split or merge (nesting, coupling), the histories branch and join. A snapshot is one frame of the workspace — the network at an instant; the workspace's **history** is the whole traced structure, and the log is its record. (The conception of space here — place constituted by adjacency, space granular — is the conception contemporary physics also holds for space itself; this algebra is not a formal application of that physics, and the workspace conception was developed in large part independently of it.)

### The axes

A workspace is described by a tuple of values on seven axes (facets). Each axis varies independently of the others; together, the values define a unique workspace state — an expression of the workspace at a moment. The tuple gives the workspace's **coordinates**: they define the workspace in actual space and in actual time, and a path through successive tuples is the workspace's topological development — its evolution over time — which is central to this formulation: the algebra describes a workspace that evolves, state by state, along its coordinates.

- **Workspace** (place): lab, field, studio, terminal 1, terminal 2, main desk, front desk, study, balcony… — open vocabulary, per the log spec. A terminal may be multi-purpose — research, image work, and sound design at one station — without ceasing to be one workspace on this axis.
- **Session type** (verb): the Work Schema's Facet A modes — intake (reading), generative, structural (archiving, admin), output (publishing), meta-cognitive (discourse, research), somatic…
- **Time**: the window, the arc.
- **Operator**: who or what works.
- **Substrate / medium**: text, image, sound, code, paper…
- **Project / Work**: which work the segment serves. A project is itself a workspace, nested in the containing one (§2); the coordinate states which nested workspace, at the current level, the work runs in.
- **ΔW temp**: the segment's temperature, given as a triple of qualia — a point in qualia space.

A **configuration** is the workspace in one total state (A2) — one value on every axis, all at once. A **session** is a path segment: configurations changing underneath while the segment's coordinates hold steady. A **log** is a composed path: segments joined end to end, its frontmatter stating the path's bounding arc.

**Derived quantities.** Not every coordinate is dialed in directly. ΔW temp is *derived* — read off a window of deltas, as C2 defines it — and velocity likewise. A derived coordinate still figures in the description and definition of a workspace: the tuple reports it because a workspace is not fully described without its temperature, any more than without its place. Derivation is a fact about where a value comes from, not a reason to strike it from the description.

## 2. The operations

- **Δ — difference.** A′ − A = ΔW. *Test: state what appreciably changed; if nothing did, the delta is null.*
- **; — composition (sequencing).** s₁ ; s₂ = s₁ then s₂. A log's arc is a composition of its segments.
- **Interleave (the Switchboard operation).** Sessions woven into one path — station to station, project to project — segments alternating at regular or irregular intervals and varying rates (A8).
- **The switch.** The switch is not dead time between sessions; in essence it is the most important part of the algebra's dynamics. The switch is where the deltas are created: the operator experiences the work as switches, and the delta chain is the trail those switches leave — a non-linear trail (the genetic trail of the work), marked by lateral jumps, forward loops, and self-interruptions, whose lived texture is the **switch texture**. Variants along the trail are not errors or hesitations; they are the trail's positive structure. The texture itself is treated at length in §7.
- **⊂ — nesting (enveloppement).** A workspace inside a workspace: a project-workspace inside the operation's workspace; this terminal inside the room that also holds a second terminal and the archives; the room inside the greater Historiotheque, with its front desk and its art studio. The nested workspace keeps its own configuration and record while sharing the containing field (A1: fields within fields).
- **+ — coupling.** Two workspaces sharing a surface or a record-stream function as one workspace at a larger scale (A10).
- **π — projection.** π keeps only the named coordinates and renders the rest away. π(time × density) = the hourly heat map; π(days × hours) = the two-dimensional chart.
- **| — restriction (slice).** Path | workspace = lab: the part of the path in the lab.
- **Push / pop — the stack operations** (A3). Set aside = push: the layer gains depth. Retrieve = pop, at A5's price: raising a layer.
- **Snapshot.** Freeze the path's current coordinates into the record (A9). A snapshot changes what the operator knows, not the workspace (§5) — and it is one frame of the workspace; the log is the history the frames belong to (§1).

## 3. The laws

- **L1 — Associativity.** (s₁ ; s₂) ; s₃ = s₁ ; (s₂ ; s₃). Regrouping a path does not change the path.
- **L2 — Identity.** The null delta composes away: s ; null = s. A stretch in which nothing appreciably changed adds nothing to the path.
- **L3 — No inverse.** There is no −s. Work cannot be subtracted; a return is a new delta forward, never an undo (patina; A4's stepwise chain). The operations form a **monoid, not a group**. (Operational shadow of L3: the no-backfill doctrine.)
- **L4 — Partial order (precedence).** The relation ≺ is **precedence**: w₁ ≺ w₂ states that the work state w₂ is **adiabatically accessible** from w₁ — reachable from it by work done within the workspace, step by step, no step skipping (the Lieb–Yngvason theory behind the 2015 formalism). Precedence is reflexive and transitive but not total: incomparable states exist, reachable from one another only by going around — by traversing intermediate grains — and A5 prices the going-around.
- **L5 — Fixed point and quotient.** Collabrium (C6) is the fixed point of the dynamics: the state the flow maps to itself, unchanged. Collapse (C7) is a quotient: many configurations map down onto the core; the core is what persists through the quotient.
- **L6 — Neighborhoods and the invariant.** Proximity (A6) is adjacency (§1): the neighborhood of a node is what stands linked to it, and of a configuration, what is reachable from it within a price. Rearrangements that preserve the record and the chain's order deform the field without tearing it (the elastic taxonomy); the invariant under such deformation is **succession — the order of the delta chain**.

## 4. Precedence and accessibility — the physics of the workspace

The relation at the center of the algebra is ≺, **precedence**. Precedence states what is adiabatically accessible from what: w₁ ≺ w₂ means the work state w₂ can be reached from w₁ by the workspace's own work, step by step. Every step is grain-to-grain: a state is reachable only through its adjacents (§1), so a precedence chain is a path across the grains of the space, and each step is a delta — the quantum of change in this algebra. There is no continuous slide between states (A4).

Proximology (A6) is where accessibility is truly spoken of: from one work state to another, as the operator meets it — nearness as adjacency, distance as the priced length of the path (A5). This is the physics aspect of the algebra: precedence, adjacency, and price, without the formalism of physics.

Two modal readings complete the algebra as a language for statements about workspaces. **◇p** — p holds at some state reachable from here, some successor under precedence. **□p** — p holds at every reachable successor. A5 grades both: reachable *within this price*. Most practical claims about a workspace ("we can get there from here") are ◇-claims; most disagreements about them are about the price attached, not the ◇. Precedence, that is, ranges over every history the workspace could take from here; the record (§5) preserves the single history it actually took.

## 5. The epistemic layer — knowledge in the workspace

The operator's knowledge state is K = surface + record: what is present without work, plus what the record holds. A **snapshot is an epistemic action**: K changes, the configuration does not. An ordinary delta changes both at once.

The record, with the workspace that holds it, is the operator's **extended cognitive organ**: memory offloaded onto the workspace itself — a physical, three-dimensional memory with its very own coordinates. To remember, in a workspace, is to traverse to coordinates: the remembered thing has a place in the graph, and retrieval is the priced path to it (A5). This offloading is the workspace's efficiency as a work system — what is carried by the space does not have to be carried in the head. A delta posted to a shared record is an announcement: it updates the knowledge state of every operator coupled through that record. In a shared workspace, what stands on the shared record is common knowledge.

## 6. Complexity and pull

Keeping track of a workspace's states costs time and space, and the bill grows with the state-load (C8). Interdependence compounds the cost: choices among many interdependent projects form a search whose cost grows combinatorially (the Switchboard decision-cost model: each choice changes the state the next is judged from), which is why proximity — the constant-time greedy read, following what is adjacent — is the operator's viable strategy. Bounded computation is not a defect of the operator; it is the condition A5 prices.

Projects are workspaces (nesting, §2), and nested workspaces behave as quasi-agents — as character-agents do: a project holds a state, demands maintenance, and **grows in complexity**, as workspaces do. Projects exert a **pull** — on the operator, and on neighboring projects. The medium they pull in is the elastic field of §1: a heavy project, many deltas at a high temperature, deforms the voisinage around it and draws what is near into its orbit. The operator's zero-memory Switchboard selection is movement in this pull field: follow the strongest pull, at no search cost (A6).

Because complexity grows at every level of nesting, the ceiling (C7) applies recursively: a workspace collapses when the time, space, and energy spent tracking and maintaining its states outruns what flows in across its membrane (A10) — and a project can collapse inside a healthy containing workspace, its collapse registering in the container as disorder (C8). The core (C7) is the minimal structure whose overhead any budget can carry.

## 7. The switch texture

I have used the Switchboard Method for decades. What I want to say about it now is that it is really all about the deltas — and it is about the switch texture.

A delta is what the record keeps: A′ − A, one grain of change, countable. A chain of deltas is the genetic trail of a workspace. But no operator experiences a chain. I experience switching: the leaving, the crossing, the arriving, hundreds of times a day, for decades. The switch texture is what the Operator actually experiences. A theory built only on deltas would describe a workspace nobody inhabits — like a music theory built only on notes, with no account of rhythm or touch.

A delta is a subtraction, and a subtraction needs two states. While I stay inside one piece of work there are not yet two states — there is flow: the painting changing under the hand, continuously, nothing yet divided into a before and an after. The switch is the cut. Leaving closes the work as a state — and the leaving itself changes it, from being worked on to drying, cooling, incubating. Arriving reconfigures the work entered before a single mark is made, because I arrive carrying what the last work put in my head. Only then do two definite states exist, with a boundary between them, and only then is there a delta to record. No switch, no cut; no cut, no pair of states; no pair, no delta. The chain in the record is the trail of those cuts.

The switch creates the deltas, rather than merely tracking them. The switch creates deltas at three levels at once — in the work left, where the leaving is itself a state change (the piece goes from available to proximate or occurrent; paint dries, a paragraph cools, a stalled problem starts incubating); in the work entered, where arrival reconfigures that workspace's surface before a single mark is made; and in the containing workspace, where the traversal links the two projects, so that a cross-connection — a noise-field idea surfacing inside a novel session because I passed through both in one morning — is a delta that belongs to neither project alone. The most valuable deltas in an interdisciplinary operation are switch-born, and a serial, one-project-at-a-time practice structurally cannot produce them.

Texture is describable. It has dimensions, not just a frequency: grain — the interval distribution, rapid and irregular, no fixed cadence, because a metronome would be a schedule and a schedule reintroduces the decision problem; span — how far a switch jumps, station to station, medium to medium, project to project, occasionally workspace to workspace; return shape — forward loops and re-entries, an occurrent project pulled back up after months having a different texture than the next item on a surface; friction — proximity keeps the switch nearly decisionless and cheap, and texture is rough precisely when the next thing is not at hand and the context-reload is heavy, so roughness is diagnostic of a badly arranged surface, not a badly behaving operator; temperature — ΔW temp is derived from a window of deltas, but texture is how that temperature is felt from inside.

The decades are the dataset. I developed the Switchboard Method in 2001–2004, under the name the 15-Minute Work Week, and formalized it fully more recently. And the logs raise the theory's honest problem: a studio log segment coarse-grains the texture — the macro session gets the header and one ΔW temp, while the real switching happened underneath, sub-segment. The texture is always partly below the resolution of its own record. Naming that limit is part of the theory, not an embarrassment to it.

The Cahiers are the same phenomenon at the opposite grain. Valéry's morning notebook IS the operation — essentially one great switch a day, into the notebook and back out, sustained fifty years. The notebook is the surface, each morning's entry a delta, recurrence and self-interruption the switch texture. Thinking IS an operation, and IS an art operation, especially when an artist is doing the thinking — performed in a workspace, on a surface, with tools, refmats, constraints, and a record that accumulates deltas. If that scale-invariance holds — texture at very low frequency, but texture still — it is a strong claim for the theory.

Why it matters for 'solving the workspace': an agentic system that tracks state-diffs alone knows what changed; it knows nothing about when to switch, what a switch costs, or that leaving a problem is often the operation that solves it. Texture is the missing variable: stall detection, incubation returns, friction as a surface-design signal. If agents are ever to work IN human workspaces rather than merely on their contents, switch texture is one of the main things they will have to learn to read — and my practice is the worked example.
