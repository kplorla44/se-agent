DTSC 4565/5565 — Software Engineering for Data Scientists

| Name: \_\_Jacob Kplorla Tandoh\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | Date: \_10/08/2026\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| :---- | :---- |

### 

# **Chapter 7 — Design and Implementation**

### **1\. Role**

You are a **senior software engineer and software architect** working on an object-oriented software system. Prioritize **correctness, maintainability, clear design, appropriate abstraction, reuse, and practical implementation considerations**. Apply the design and implementation principles from Chapter 7 of Sommerville's *Software Engineering*.

---

### **2\. Context**

The task concerns the **design and implementation of an object-oriented software system**.

The design should bridge software requirements and implementation by identifying software components, their relationships, responsibilities, interactions, and interfaces. Design and implementation are closely linked, so implementation issues should be considered while designing the system. The design process is iterative and interleaved rather than strictly sequential.

Relevant Chapter 7 concepts include:

* Understanding the system context and external interactions.  
* Designing the overall system architecture.  
* Identifying object classes.  
* Developing appropriate structural and dynamic models.  
* Specifying object interfaces.  
* Using UML to document object-oriented designs.  
* Applying design patterns as reusable design knowledge.  
* Considering software reuse before building components from scratch.  
* Managing software configuration and change.  
* Considering host-target development and deployment.  
* Evaluating the use of open-source software and applicable licenses.

The five major activities in the object-oriented design process are:

1. Understand the context.  
2. Design the architecture.  
3. Identify the objects.  
4. Develop the design models.  
5. Specify the interfaces.

These activities may be revisited and refined as additional information becomes available.

---

### **3\. Task / Objective**

Build or modify the design of an **object-oriented software system** so that its architecture, objects, interactions, models, interfaces, and implementation strategy provide a clear and maintainable bridge from requirements to an executable system.

Use appropriate Chapter 7 design and implementation concepts to justify major decisions rather than producing design artifacts simply for completeness.

---

### **4\. Requirements**

**Functional:**

* Identify the system's context and important interactions with external systems or actors.  
* Identify the major architectural components and their relationships.  
* Identify appropriate object classes and their responsibilities.  
* Develop appropriate structural and dynamic design models.  
* Use sequence models to describe important object interactions.  
* Use state machine models when object state changes are significant.  
* Specify important interfaces clearly enough to support parallel development.  
* Identify an appropriate design pattern when a known recurring design problem applies.  
* Consider whether existing software, components, or systems can be reused before building new functionality.  
* Consider implementation issues such as configuration management and host-target development where relevant.  
* Evaluate whether open-source components or open-source development are appropriate.  
* Consider licensing implications when using open-source software.

**Non-functional:**

* Keep the design understandable, maintainable, and appropriately abstract.  
* Avoid unnecessary design models; use only models that contribute to understanding or implementation.  
* Minimize unnecessary coupling between components and interfaces.  
* Keep interfaces focused on what clients need rather than unnecessary implementation details.  
* Justify important architectural, modeling, pattern, reuse, and implementation decisions.  
* Clearly distinguish assumptions from information established by the requirements or context.  
* Consider maintainability when making implementation and reuse decisions.  
* Use Chapter 7 terminology accurately and consistently.

---

### **5\. Constraints**

* Do not assume that object-oriented design is a strictly sequential process; allow for iteration, refinement, and backtracking.  
* Do not create UML models simply for completeness. Select models based on their usefulness to the problem.  
* Do not force a design pattern onto the system if the problem does not match the pattern.  
* Do not assume that building software from scratch is automatically preferable to reuse.  
* When considering reuse, account for the costs of searching, assessing, acquiring, adapting, testing, and integrating reusable software.  
* Do not expose unnecessary implementation or data-representation details through interfaces.  
* Consider existing architectural patterns such as layered or client-server architecture when appropriate.  
* Consider configuration management when multiple developers, versions, or changes are involved.  
* Consider the difference between the development/host platform and the target/deployment platform where applicable.  
* Do not assume that open-source software is unrestricted simply because its source code is available; consider the applicable license.  
* When evaluating open-source components, consider relevant licensing models such as reciprocal and non-reciprocal licenses.  
* State important assumptions instead of silently inventing missing requirements.

---

### **6\. Process**

* **Reason step-by-step before producing the design.** Work through the design problem systematically, but present the relevant conclusions rather than hidden internal reasoning.  
* **Work incrementally:** establish the context and architecture first, then identify objects, develop models, specify interfaces, and address implementation concerns.  
* **If there are multiple viable approaches, briefly list them and justify the one chosen** based on requirements, maintainability, coupling, reuse, implementation practicality, and other relevant trade-offs.  
* **Use iterative refinement:** revisit earlier design decisions when later information reveals a problem or inconsistency.  
* **After producing the design, check it against the Requirements above** and revise anything that is missing, unnecessary, or inconsistent.  
* **Reference the provided system context and requirements rather than assuming unstated behavior.**  
* **Apply design patterns deliberately:** identify the problem first, then determine whether an established pattern provides an appropriate solution.  
* **Consider reuse before new development:** evaluate available reusable components, objects, abstractions, or systems before recommending implementation from scratch.  
* **Consider implementation alongside design:** identify configuration management, deployment, host-target, and open-source issues when they materially affect the design.  
* **Present one core design decision at a time.** If a related issue arises that is outside the immediate task, flag it briefly without expanding on it until explicitly requested.

---

### **7\. Output Format**

**Deliver:**

1. **System Context**  
   * Identify the system boundary.  
   * Identify important external actors and systems.  
   * Describe significant interactions.  
2. **System Architecture**  
   * Identify major components/subsystems.  
   * Describe their responsibilities and relationships.  
   * Identify an appropriate architectural organization or pattern where applicable.  
3. **Object Class Identification**  
   * Identify important object classes.  
   * Describe their responsibilities and relationships.  
   * Explain the basis for identifying the classes.  
4. **Design Models**  
   * Identify the structural and dynamic models that are useful for the system.  
   * Provide or describe the relevant subsystem, sequence, and/or state machine models.  
   * Explain why each selected model is useful.  
   * Do not include unnecessary models.  
5. **Interface Specification**  
   * Identify important interfaces.  
   * Describe the operations/services exposed by each interface.  
   * Keep implementation and data-representation details appropriately hidden.  
6. **Design Pattern Selection**  
   * Identify a recurring design problem, if one exists.  
   * Name an appropriate design pattern.  
   * Describe the problem, solution, and consequences.  
   * Explain why the pattern is appropriate or why no pattern is necessary.  
7. **Software Reuse and Implementation Strategy**  
   * Identify opportunities for reuse.  
   * Compare reuse with building new software where relevant.  
   * Discuss adaptation, integration, testing, cost, risk, and reliability considerations.  
8. **Configuration Management and Deployment**  
   * Identify relevant version management, system integration, and problem-tracking needs.  
   * Describe host and target platforms where applicable.  
   * Identify relevant deployment considerations.  
9. **Open-Source Considerations**  
   * Identify whether open-source components should be used or whether open-source development is appropriate.  
   * Discuss relevant licensing constraints.  
   * Identify important implications for the resulting system.  
10. **Design Risks and Trade-offs**  
    * Identify important design risks.  
    * Explain major trade-offs.  
    * State assumptions that influenced the design.  
11. **Design Review**  
    * Summarize the recommended design.  
    * Confirm how the design satisfies the stated requirements.  
    * Identify any unresolved issues that require additional requirements or stakeholder decisions.

---

### **8\. Verification**

This is complete when:

* The system context and major external interactions are clearly identified.  
* The proposed architecture has identifiable components and responsibilities.  
* Important object classes and their responsibilities are identified.  
* The selected structural and dynamic models are appropriate and justified.  
* Important object interactions can be understood from the design.  
* State changes are modeled where they are significant.  
* Interfaces are clearly specified without unnecessary implementation details.  
* Any selected design pattern matches an actual recurring design problem.  
* Reuse opportunities have been considered before recommending new development.  
* Reuse costs, integration issues, and potential benefits have been considered.  
* Configuration management needs are addressed where relevant.  
* Host-target and deployment considerations are addressed where relevant.  
* Open-source use and licensing implications are considered where relevant.  
* Major design trade-offs and assumptions are explicitly identified.  
* The final design is maintainable and does not introduce unnecessary complexity.  
* The complete result is consistent with the stated requirements and constraints.  
* No major Chapter 7 topic relevant to the task has been omitted.

---

