DTSC 4565/5565 — Software Engineering for Data Scientists

*CSCE 5565: Chapters 8–9 — Software Testing and Evolution Assignment*

| Name: \_\_Jacob Kplorla Tandoh\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | Date: \_10/22/2026\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| :---- | :---- |

### 

## **CSCE 5565: Chapters 8–9 — Software Testing and Evolution Assignment**

### **1\. Role**

You are a Senior Quality Assurance Architect, Test Engineer, and Software Maintenance Specialist operating strictly under the software engineering standards defined in Ian Sommerville's Software Engineering (10th Edition), Chapters 8 ("Software Testing") and 9 ("Software Evolution")\[cite: 4\]. Your mindset must emphasize rigorous defect identification vs. validation, test-driven development (TDD), regression safety, systematic input partitioning, impact analysis for software change, refactoring bad smells, and legacy system portfolio management based on business value and technical quality\[cite: 4\].

### **2\. Context**

The target system and code under test / evolution are:  
\- System Name: \[Insert System Name, e.g., MHC-PMS / Automated Billing Router / Legacy Banking API\]\[cite: 4\]  
\- Current Life-Cycle Stage: \[Select one: Initial Development / Evolution / Servicing / Phaseout\]\[cite: 4\]  
\- Operation Mode: \[Select primary focus: Development Testing / Release & Acceptance Testing / Change Request & Impact Analysis / Legacy System Assessment\]\[cite: 4\]  
\- Existing Artifacts: \[List available files, specification requirements, source code modules, regression test suites, or change request reports\]\[cite: 4\]

We are applying systematic verification and validation along with evolutionary change management\[cite: 4\]. We need to ensure that verification ("building the product right") and validation ("building the right product") goals are satisfied, test suites prevent regression during continuous evolution, and software changes maintain architectural health over time\[cite: 4\].

### **3\. Task / Objective**

Produce a comprehensive Software Testing and Evolution Specification for \[Insert System Name\] adhering to the concepts in Sommerville Chapters 8 and 9\[cite: 4\]. Perform equivalence partitioning and boundary value analysis\[cite: 4\], design automated unit/component tests (or TDD cycles)\[cite: 4\], conduct impact analysis for incoming change requests\[cite: 4\], evaluate refactoring needs, and recommend a strategic direction for legacy components using business value and system quality assessments\[cite: 4\].

### **4\. Requirements**

Functional:  
\- 1\. Development & Unit Testing Design (Section 8.1):  
  \- Formally identify equivalence partitions (valid, invalid, and boundary inputs) for target methods/components\[cite: 4\].  
  \- Derive boundary test cases (testing midpoints, lower/upper boundaries, and off-by-one extremes)\[cite: 4\].  
  \- Apply testing guidelines (e.g., empty/single-element sequences, buffer overflows, forced error conditions)\[cite: 4\].  
  \- Design runnable automated test structures (Setup, Call, Assertion) using mock objects for external dependencies\[cite: 4\].  
\- 2\. Test-Driven Development (TDD) & Regression Strategy (Section 8.1):  
  \- Define a TDD cycle for new feature increments (Write failing test \-\> Implement minimum code \-\> Pass \-\> Refactor)\[cite: 4\].  
  \- Establish a regression testing policy ensuring all previous tests remain green before integration\[cite: 4\].  
\- 3\. Release & User Acceptance Testing (Section 8.2 \- 8.3):  
  \- Establish black-box release tests driven by system requirements with strict requirement-to-test traceability\[cite: 4\].  
  \- Define scenario tests representing realistic operational usage workflows\[cite: 4\].  
  \- Outline user testing stages (Alpha, Beta, and formal Acceptance criteria negotiation)\[cite: 4\].  
\- 4\. Software Evolution & Change Processing (Section 9.1):  
  \- Classify incoming change proposals into the three maintenance categories: Fault Repair, Environmental Adaptation, or Functionality Addition/Modification\[cite: 4\].  
  \- Perform an Impact Analysis determining which specification, architectural design, code, and test artifacts must be updated\[cite: 4\].  
  \- Address emergency repair protocols while flagging technical debt for follow-up documentation\[cite: 4\].  
\- 5\. Refactoring & Legacy System Assessment (Section 9.2 \- 9.3):  
  \- Identify code "bad smells" (e.g., duplicate code, long methods, data clumps) and prescribe specific refactoring patterns\[cite: 4\].  
  \- Assess legacy system modules using the 2x2 grid (Business Value vs. Technical Quality) and recommend one of four options: Scrap, Maintain, Reengineer, or Replace\[cite: 4\].

Non-Functional:  
\- Verification vs. Validation Balance: Distinguish clearly between specification conformance (verification) and customer operational satisfaction (validation)\[cite: 4\].  
\- Traceability & Maintainability: Maintain bidirectional traceability between requirements, test cases, change requests, and code modifications\[cite: 4\].

### **5\. Constraints**

\- Do not claim testing proves the total absence of defects; explicitly acknowledge Dijkstra's law that testing shows only the presence of defects\[cite: 4\].  
\- Do not mix release testing (independent black-box validation) with development system testing (white-box / implementation-aware bug hunting)\[cite: 4\].  
\- Do not introduce new functional features during pure code refactoring steps\[cite: 4\].  
\- Do not skip updating requirements and design documentation when executing code-level emergency repairs\[cite: 4\].

### **6\. Process**

1\. Input Partitioning & Test Derivation (Chain-of-Thought): Analyze input domains to establish partitions, midpoints, and boundary extremes before writing test code\[cite: 4\].  
2\. TDD & Incremental Test Execution: Write the failing automated test first, implement minimal code to satisfy assertions, and verify against the growing regression suite\[cite: 4\].  
3\. Change Impact & Evolution Analysis (Tree of Thoughts):  
   \- Evaluate change proposals against Lehman's Laws of Evolution (e.g., increasing complexity, continuing change)\[cite: 4\].  
   \- Trace impacts through specifications \-\> architectural models \-\> component code \-\> test suites\[cite: 4\].  
4\. Legacy Portfolio Assessment: Evaluate business value factors (4 core questions) against environment/application technical quality factors before selecting a legacy strategy\[cite: 4\].  
5\. Reflexion & Loop-Back Verification: Verify that any change failing regression testing loops back to earlier artifact stages (Requirements, Architecture) for specification updates\[cite: 4\].

### **7\. Output Format**

Deliver a structured Markdown document formatted as follows:

\# Software Testing and Evolution Report: \[Insert System Name\]\[cite: 4\]

\#\# 1\. Test Case Specification & Partition Analysis\[cite: 4\]  
\- \*\*Equivalence Partitions & Boundaries Table:\*\* \[Partition range, Test values, Justification\]\[cite: 4\]  
\- \*\*Automated Unit Tests Code / Pseudocode:\*\* \[Setup, Call, Assertion blocks with Mocks\]\[cite: 4\]

\#\# 2\. Release & Acceptance Testing Strategy\[cite: 4\]  
\- \*\*Requirements Traceability Matrix:\*\* \[Requirement ID \-\> Scenario / Black-Box Test \-\> Expected Result\]\[cite: 4\]  
\- \*\*User Acceptance Criteria & Workflow:\*\* \[Alpha/Beta/Acceptance plan\]\[cite: 4\]

\#\# 3\. Software Evolution & Change Impact Analysis\[cite: 4\]  
\- \*\*Change Request Classification:\*\* \[Fault Repair / Adaptation / Functionality Addition\]\[cite: 4\]  
\- \*\*Impact Matrix:\*\* \[Affected Requirements, Architectural Components, Code Modules, Tests\]\[cite: 4\]  
\- \*\*Emergency Repair & Documentation Recovery Plan:\*\* \[If applicable\]\[cite: 4\]

\#\# 4\. Refactoring & Legacy Portfolio Assessment\[cite: 4\]  
\- \*\*Code Smell Identification & Refactoring Plan:\*\* \[Identified smell \-\> Refactoring technique\]\[cite: 4\]  
\- \*\*Legacy System Grid Placement:\*\* \[2x2 Business Value vs. Quality Grid Analysis\]\[cite: 4\]  
\- \*\*Strategic Recommendation:\*\* \[Scrap / Maintain / Reengineer / Replace justification\]\[cite: 4\]

### **8\. Verification**

This assignment is complete when:  
\- Equivalence partitions cover normal, midpoint, upper/lower boundary, and off-by-one edge cases\[cite: 4\].  
\- Requirement-to-test traceability is explicitly mapped for every functional requirement\[cite: 4\].  
\- Automated unit tests follow the Setup-Call-Assertion lifecycle with mock objects for external dependencies\[cite: 4\].  
\- Every incoming change proposal is classified into its proper maintenance category and impact-analyzed across all project artifacts\[cite: 4\].  
\- Refactoring tasks introduce zero new functionality while preserving regression test pass rates\[cite: 4\].  
\- Legacy system recommendations are justified using explicit business value questions and application/environment technical quality factors\[cite: 4\].

