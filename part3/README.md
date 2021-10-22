# Theory
## Threats and Security
### Assignment
- Prepare a presentation on the key points of each paper, and also think about the "big picture":
  - How has security evolved over the last 30 years?
  - How can modern techniques and methods like DevOps and SOCs be applied to networked CPS?
  - What makes misconfigurations so dangerous?
  - How can we keep next-generation CPS/IoT systems safe and secure?

### Reading
- Video resources
  - [Module 1: What are threats and the four types of attack?](https://www.youtube.com/watch?v=5DNcj5NZIjo) 
  - [Basics of Intrusion Detection](https://www.youtube.com/watch?v=Kb4T2s2gdtM)
- Two sources per group member (more can be found). Each source should be covered by at least one person
  - OWASP Top 10: A5 Security Misconfiguration [https://www.youtube.com/watch?v=ouuXu9_UM0w] [Marcus]
  - Bidou, R. (2005). Security operation center concepts & implementation (29 pages). [Javier]
  - Ebert, C., Gallardo, G., Hernantes, J., & Serrano, N. (2016). DevOps. IEEE Software, 33(3), 94-100. [Kostas] [Muhammed]
  - Dang, Y., Lin, Q., & Huang, P. (2019, May). AIOps: real-world challenges and research innovations. In 2019 IEEE/ACM 41st International Conference on Software Engineering: Companion Proceedings (ICSE-Companion) (pp. 4-5). IEEE. [Shamoona] [Muhammed]
  - Ganame, A. K., Bourgeois, J., Bidou, R., & Spies, F. (2008). A global security architecture for intrusion detection on computer networks. computers & security, 27(1-2), 30-47. [Shamoona]
  - Ly, K., & Jin, Y. (2016, July). Security challenges in CPS and IoT: From end-node to the system. In 2016 IEEE Computer Society Annual Symposium on VLSI (ISVLSI) (pp. 63-68). IEEE. [Marcus] [Kostas]
  - Chlosta, M., Rupprecht, D., Holz, T., & Pöpper, C. (2019, May). LTE security disabled: misconfiguration in commercial networks. In Proceedings of the 12th conference on security and privacy in wireless and mobile networks (pp. 261-266). [Marcus]  [Javier]




# Project
## Modeling

Think of a concrete scenario that has (possibly conflicting) safety and security properties. Brainstorm a bit in your group about what interest you the most.

## Concrete scenarios:
 - Biolab => Espace ship
  -  Airlock in the espace ship
    - Different types of stafss, special access to go to certain rooms with access to airlockers
    - Requirements:
      - Only one door should be open in the airlock
      - The astrnaut needs to go in (Liveness property)   
    - Safety:
      - You need access to go outside
      - You dont need acces to come inside ? 
 - Submarine 
  - Torpedo(wathever) (1)
    - Two steps authentication (Security)
      - One in the room one outside 
    - Location component (Security + Safety)
    - External measurements (Safety)
      - For example, the tube should be full of water before turning on the torpedo (Safety)
      - The access from the tube to the submarine should be closed (Safety, the submarine sinks)


  - Go to surface (2) (Decided)(Security + Safety)
    - The final decision can be disregarded to the captain no matter the following security consequences
      - Submarine in Stockhollm
      - K19 (scifi)
      - Kursk
      - others...     

Create an informal model and description first, then choose some key components and model them formally in NuSMV.

## Modeling key features and properties

For some key functionality and properties for your scenario, create a model in NuSMV.

The model should have at least the following modules:

- Modules for each key component.
- A user module that models possible choices of a (benign or malicious) user.
- A main module that ties everything together.

**Write at least five properties, out of which at least one must be a liveness property.**

Verify your model with NuSMV and ensure that the properties are verified as correct.

Apply a validation technique to your model and assess whether you think the properties themselves are right.

## Deliverables

- Upload a short presentation (about 2–3 slides) giving an informal overview of your project.
Try to use a few diagrams to show the project and how you model it.
- Upload the resulting NuSMV model and description (either as a comment, or as a separate file or text input).
