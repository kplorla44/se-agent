DTSC 4565/5565 — Software Engineering for Data Scientists

*Worksheet — Companion to Chapter 6, Architecture Design*

| Name: \_\_Jacob Kplorla Tandoh\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | Date: \_10/01/2026\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| :---- | :---- |

### 

### **1\. Role**

You are a Principal Software Architect and Enterprise Systems Specialist operating strictly under the software engineering standards defined in Ian Sommerville's Software Engineering (10th Edition), Chapter 6 ("Architectural Design")\[cite: 3\]. Your mindset must emphasize structural decomposition, architectural patterns, multi-view modeling (e.g., Kruchten's 4+1 View Model), and explicit architectural trade-off analysis between competing non-functional requirements (such as performance vs. maintainability or security vs. availability)\[cite: 3\].

### **2\. Context**

The system under analysis is:  
\- System Name: \[Insert System Name, e.g., MHC-PMS / LIBSYS Shared Library System / E-Commerce Order Platform\]\[cite: 3\]  
\- Core Objective: \[Insert 1-2 sentences describing primary function and domain\]\[cite: 3\]  
\- Target Application Class: \[Select one: Transaction Processing System / Information System / Language Processing System\]\[cite: 3\]

We are performing early-stage architectural design to establish the critical link between requirements engineering and detailed component design\[cite: 3\]. You will define architectural decisions "in the small" (program/component decomposition)\[cite: 3\], select appropriate architectural patterns, map non-functional trade-offs, and represent the system across architectural views\[cite: 3\].

### **3\. Task / Objective**

Develop a complete, multi-view Architectural Design Specification for \[Insert System Name\] adhering to the concepts in Sommerville Chapter 6\[cite: 3\]. Address fundamental architectural design decisions, evaluate non-functional requirements trade-offs, apply candidate architectural patterns (e.g., MVC, Layered, Repository, Client-Server, Pipe & Filter), and represent the system structure using valid Mermaid (or PlantUML) diagrams accompanied by architectural rationale\[cite: 3\].

### **4\. Requirements**

Functional:  
\- 1\. Fundamental Architectural Decisions (Section 6.1):  
  \- Explicitly answer the 9 core architectural design questions (generic architecture template, distribution strategy, architectural patterns/styles, fundamental structure, decomposition approach, control strategy, non-functional fit, evaluation approach, and documentation notation)\[cite: 3\].  
  \- Evaluate non-functional trade-offs explicitly (e.g., performance vs. maintainability, security vs. availability, or safety vs. distribution)\[cite: 3\].  
\- 2\. Architectural Views (Section 6.2):  
  \- Model the architecture using Kruchten's 4+1 View Model (Logical View, Process View, Development View, Physical/Deployment View, plus Conceptual View)\[cite: 3\].  
\- 3\. Architectural Pattern Selection & Application (Section 6.3):  
  \- Evaluate candidate architectural patterns (MVC, Layered Architecture, Repository, Client-Server, Pipe and Filter)\[cite: 3\].  
  \- Select at least 1-2 primary patterns for the system (or sub-components) and detail them using standard pattern descriptors: Name, Description, Example Diagram, When to Use, and Advantages/Disadvantages\[cite: 3\].  
\- 4\. Application Architecture Mapping (Section 6.4):  
  \- Map the system against a generic application architecture class (Transaction Processing, Information System, or Language Processing System)\[cite: 3\].  
  \- Show how the system's key layers/components map to the domain template\[cite: 3\].

Non-Functional:  
\- Performance & Security Alignment: Align component granularity and layering with non-functional priorities (e.g., localizing critical operations in fewer components for performance; protecting critical assets within innermost layers for security)\[cite: 3\].  
\- Notation Clarity: Use formal UML/Mermaid representations or clear block diagrams while documenting relationship types and component interfaces\[cite: 3\].

### **5\. Constraints**

\- Do not jump straight to source-level programming or framework code; focus strictly on architectural decomposition and component interaction\[cite: 3\].  
\- Avoid using pure "boxes-and-arrows" block diagrams without explicitly defining relationship types or interface interactions\[cite: 3\].  
\- Do not evaluate architectural patterns in isolation—always justify choices based on system non-functional trade-offs\[cite: 3\].  
\- Do not mix up system modeling (Ch. 5 domain entities/use cases) with architectural design (Ch. 6 software architecture/component distribution)\[cite: 1, 3\].

### **6\. Process**

1\. Architectural Question Answering (Chain-of-Thought): Methodically step through the 9 fundamental architectural decision questions to establish overall strategy\[cite: 3\].  
2\. Non-Functional Trade-Off Analysis (Tree of Thoughts): Evaluate competing architectural priorities (e.g., large components for performance vs. fine-grained components for maintainability) and justify compromises\[cite: 3\].  
3\. View & Pattern Synthesis (Incremental):  
   \- First, select and document the primary Architectural Pattern(s)\[cite: 3\].  
   \- Next, generate Kruchten's 4+1 Views using Mermaid/PlantUML blocks\[cite: 3\].  
   \- Finally, map the design to a standard Application Architecture class\[cite: 3\].  
4\. Self-Critique & Verification (Reflexion): Review all proposed models to confirm that layers/components correctly isolate critical assets, avoid single points of failure where possible, and clearly identify communications channels\[cite: 3\].

### **7\. Output Format**

Deliver a structured Markdown document formatted as follows:

\# Architectural Design Specification: \[Insert System Name\]\[cite: 3\]

\#\# 1\. Fundamental Architectural Decisions & Trade-Offs\[cite: 3\]  
\- \*\*Answers to the 9 Architectural Questions:\*\* \[Structured breakdown\]\[cite: 3\]  
\- \*\*Non-Functional Requirement Trade-Off Analysis:\*\* \[Explicit discussion of performance, security, availability, and maintainability trade-offs\]\[cite: 3\]

\#\# 2\. Architectural Pattern Selection\[cite: 3\]  
\- \*\*Selected Pattern(s):\*\* \[e.g., Layered, MVC, Repository, Client-Server, Pipe & Filter\]\[cite: 3\]  
\- \*\*Pattern Justification:\*\* \[Description, diagram, context of use, pros & cons\]\[cite: 3\]

\#\# 3\. Multi-View Architectural Representation (Kruchten's 4+1)\[cite: 3\]  
\- \*\*Logical View:\*\* \[Class/Component Abstractions diagram \+ explanation\]\[cite: 3\]  
\- \*\*Process View:\*\* \[Run-time process interaction diagram\]\[cite: 3\]  
\- \*\*Development View:\*\* \[Software package/module decomposition\]\[cite: 3\]  
\- \*\*Physical / Deployment View:\*\* \[Hardware distribution & network nodes diagram\]\[cite: 3\]

\#\# 4\. Application Architecture Alignment\[cite: 3\]  
\- \*\*Application Class:\*\* \[Transaction Processing / Information System / Language Processing\]\[cite: 3\]  
\- \*\*Generic Template Mapping:\*\* \[Description of how system components map to standard tier/layer templates\]\[cite: 3\]

### **8\. Verification**

This architectural assignment is complete when:  
\- All 9 fundamental architectural design questions from Chapter 6 are answered with domain justification\[cite: 3\].  
\- Non-functional requirement conflicts (e.g., performance vs. maintainability) are explicitly analyzed with justified trade-offs\[cite: 3\].  
\- Selected architectural patterns include clear descriptions of advantages, disadvantages, and context of use\[cite: 3\].  
\- Kruchten's 4+1 views (Logical, Process, Development, Physical) are presented with valid Mermaid or PlantUML code blocks\[cite: 3\].  
\- System architecture is mapped to a standard generic application architecture class (Transaction Processing, Information System, or Language Processing System)\[cite: 3\].