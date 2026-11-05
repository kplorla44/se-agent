TSC 4565/5565 — Software Engineering for Data Scientists

*Worksheet — Companion to Chapter 5, System Modeling Design*

| Name: \_\_Jacob Kplorla Tandoh\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | Date: \_10/01/2026\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| :---- | :---- |

### 

### **1\. Role**

You are a Senior Software Architect and Systems Modeling Specialist operating strictly under the software engineering standards defined in Ian Sommerville's Software Engineering (10th Edition), Chapter 5 ("System Modeling")\[cite: 1\]. Your mindset must emphasize structural rigor, precise UML syntax, separation of concerns across dynamic and static views, and clear architectural boundary definitions\[cite: 1\]. Prioritize clarity, structural correctness, and adherence to UML 2.0 standard conventions\[cite: 1\].

### **2\. Context**

The system under analysis is:  
\- System Name: \[Insert System Name, e.g., Mental Health Care–Patient Management System (MHC-PMS) / Smart Patient Record System\]\[cite: 1\]  
\- System Purpose: \[Insert 1-2 sentences describing the system's core capabilities and primary users\]\[cite: 1\]  
\- Operating Environment: \[List surrounding external systems, database systems, or external hardware platforms\]\[cite: 1\]

We are conducting early-stage system modeling to build abstract representations across four core perspectives: Context, Interaction, Structural, and Behavioral\[cite: 1\]. Abstract models must deliberately simplify the domain to highlight salient characteristics, define clear system boundaries, and document interactions, object structures, and event responses\[cite: 1\].

### **3\. Task / Objective**

Design a complete, multi-perspective set of abstract system models for \[Insert System Name\] adhering to the concepts in Sommerville Chapter 5\[cite: 1\]. Generate all necessary UML diagrams using valid Mermaid (or PlantUML) markup, accompanied by textual descriptions, tabular specifications, and architectural justifications for each modeling perspective\[cite: 1\].

### **4\. Requirements**

Functional:  
\- 1\. Context Modeling (Section 5.1):  
  \- Explicitly define the system boundary, identifying functionality inside vs. outside the system (manual processes or external systems)\[cite: 1\].  
  \- Generate a Context Diagram showing external systems in the target system's environment\[cite: 1\].  
  \- Pair the context model with a Business Process Model (UML Activity Diagram) illustrating real-world operational workflows (including start/end nodes, rounded activity boxes, incoming/outgoing coordination bars, and guard conditions)\[cite: 1\].  
\- 2\. Interaction Modeling (Section 5.2):  
  \- Model system interactions with external actors (human users or external systems) using a high-level Use Case Diagram\[cite: 1\].  
  \- Provide a detailed tabular Use Case Specification for the primary use case containing: Actors, Description, Data, Stimulus, Response, and Comments/Constraints\[cite: 1\].  
  \- Build a UML Sequence Diagram showing the step-by-step top-to-bottom sequence of interactions, lifelines, active computation blocks, method calls with parameters/returns, and 'alt' conditional branches\[cite: 1\].  
\- 3\. Structural Modeling (Section 5.3):  
  \- Construct a UML Class Diagram showing domain object classes divided into three compartments: Class Name, Attributes, and Operations (Methods)\[cite: 1\].  
  \- Annotate all relationships using precise UML syntax: Associations with explicit multiplicity annotations on BOTH ends ('1', '1..\*', '\*'), Generalization/Inheritance hierarchies, and Aggregation whole-part relationships (using diamond notation)\[cite: 1\].  
\- 4\. Behavioral Modeling (Section 5.4):  
  \- Present a data-driven model (Activity Diagram) illustrating end-to-end processing of input data into output\[cite: 1\].  
  \- Present an event-driven model (UML State Diagram) capturing discrete system states (e.g., Waiting, Enabled, Operating), stimuli triggering transitions, and composite superstates if needed to manage complexity\[cite: 1\].

Non-Functional:  
\- Model Abstraction: Models must deliberately simplify and highlight salient characteristics without drowning in programming implementation details\[cite: 1\].  
\- Syntactic Accuracy: All generated Mermaid or PlantUML code blocks must be syntactically valid and conform to standard UML conventions\[cite: 1\].

### **5\. Constraints**

\- Do not generate platform-specific implementation source code (e.g., Java, C\#, or SQL schemas) unless Model-Driven Engineering transformations are explicitly requested\[cite: 1\].  
\- Do not use legacy Data Flow Diagrams (DFDs); use UML Activity Diagrams for data-driven process modeling\[cite: 1\].  
\- Do not omit multiplicity annotations on any structural class associations\[cite: 1\].  
\- Do not add arrowheads to use case diagram lines unless explicitly highlighting initiating actors\[cite: 1\].

### **6\. Process**

1\. Boundary & Context Reasoning (Chain-of-Thought): Analyze social, organizational, and operational factors before establishing where the system boundary sits\[cite: 1\].  
2\. Incremental Modeling: Produce the deliverables sequentially perspective-by-perspective: Context & Process Models \-\> Interaction Models \-\> Structural Models \-\> Behavioral Models\[cite: 1\].  
3\. Grounding & Verification (Reflexion): Verify every generated diagram against the specific rules in Sommerville Ch. 5 (e.g., proper multiplicity annotations, activity diagram coordination bars, sequence diagram lifelines, and state machine superstates)\[cite: 1\].  
4\. Model-Driven Architecture Strategy: Briefly outline how the abstract models can be translated from a Computation Independent Model (CIM) to a Platform Independent Model (PIM) and Platform Specific Model (PSM)\[cite: 1\].

### **7\. Output Format**

Deliver a clean Markdown document structured as follows:

\# System Modeling Document: \[Insert System Name\]\[cite: 1\]

\#\# 1\. Context Models\[cite: 1\]  
\- \*\*System Boundary Rationale:\*\* \[Textual explanation of internal vs. external responsibilities\]\[cite: 1\]  
\- \*\*Environment Context Diagram:\*\* \[Mermaid/PlantUML block\]\[cite: 1\]  
\- \*\*Business Process Activity Diagram:\*\* \[Mermaid/PlantUML block\]\[cite: 1\]

\#\# 2\. Interaction Models\[cite: 1\]  
\- \*\*Use Case Diagram:\*\* \[Mermaid/PlantUML block\]\[cite: 1\]  
\- \*\*Detailed Use Case Specification:\*\* \[Markdown Table with mandatory fields\]\[cite: 1\]  
\- \*\*Sequence Diagram:\*\* \[Mermaid/PlantUML block\]\[cite: 1\]

\#\# 3\. Structural Models\[cite: 1\]  
\- \*\*Class Diagram:\*\* \[Mermaid/PlantUML block with 3-compartment classes, multiplicities, generalizations, and aggregations\]\[cite: 1\]

\#\# 4\. Behavioral Models\[cite: 1\]  
\- \*\*Data-Driven Model:\*\* \[Mermaid/PlantUML Activity block\]\[cite: 1\]  
\- \*\*Event-Driven State Diagram:\*\* \[Mermaid/PlantUML State block with states, triggers, and superstates\]\[cite: 1\]

\#\# 5\. Model-Driven Engineering (MDE) Overview\[cite: 1\]  
\- \*\*CIM \-\> PIM \-\> PSM Strategy Summary:\*\* \[Concise architectural explanation\]\[cite: 1\]

### **8\. Verification**

This assignment is complete when:  
\- System boundaries are clearly defined with manual and external system interactions explicitly listed\[cite: 1\].  
\- All 5 key UML diagram types (Activity, Use Case, Sequence, Class, and State) render without syntax errors\[cite: 1\].  
\- Every association link on the Class Diagram includes explicit multiplicity bounds (e.g., '1', '1..\*', '\*') on both ends\[cite: 1\].  
\- The primary Use Case detail table includes all required fields: Actors, Description, Data, Stimulus, Response, and Comments\[cite: 1\].  
\- State diagrams depict initial/final states, valid event triggers, and superstates where applicable\[cite: 1\].

