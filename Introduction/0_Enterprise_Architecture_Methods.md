# Enterprise Architecture Methods Introduction

## Outline

- [Enterprise Architecture Methods Introduction](#enterprise-architecture-methods-introduction)
  - [Outline](#outline)
  - [Enterprise Architecture Methods](#enterprise-architecture-methods)
    - [Definitions](#definitions)
      - [Architecture methods](#architecture-methods)
      - [Framework](#framework)
    - [Rational Unified Process (RUP)](#rational-unified-process-rup)
    - [UN/CEFACT's Modeling Methodology (UMM)](#uncefacts-modeling-methodology-umm)
    - [IEEE 1471-2000](#ieee-1471-2000)
    - [IEEE 42010](#ieee-42010)
  - [Enterprise Architecture Frameworks](#enterprise-architecture-frameworks)
    - [Zachman Framework](#zachman-framework)
    - [The Open Group Architecture Framework (TOGAF)](#the-open-group-architecture-framework-togaf)
      - [TOGAF Architecture development method](#togaf-architecture-development-method)
    - [OMG's Model-Driven Architecture (MDA)](#omgs-model-driven-architecture-mda)

## Enterprise Architecture Methods

### Definitions

#### Architecture methods

An **[architecture method](../Glossary/Architecture_method.md)** is a structured collection of techniques and process steps for creating and maintaining an enterprise architecture. For example, TOGAF's Architecture Development Method (ADM) is a well-known [architecture method](../Glossary/Architecture_method.md).

[Architecture methods](../Glossary/Architecture_method.md) typically **display the various phases of the architecture lifecycle**. They **specify what deliverables** should be produced at each stage and how these **deliverables are verified or tested**. Essentially, [architecture methods](../Glossary/Architecture_method.md) are tools designed to manage the architecture lifecycle and develop the enterprise architecture framework.

#### Framework

A **[framework](../Glossary/Architecture_framework.md)** is a real or conceptual structure that serves as a support or guide for building something useful. In computer systems, a [framework](../Glossary/Architecture_framework.md) often represents a layered structure. This structure indicates what kinds of programs can or should be built and how they interrelate. For instance, the Zachman [Framework](../Glossary/Architecture_framework.md) provides a structured approach to designing and managing enterprise architectures.

### Rational Unified Process (RUP)

The Rational Unified Process (RUP) is an iterative software development process [framework](../Glossary/Architecture_framework.md). Unlike the classical waterfall process, RUP defines an iterative process. This process realizes software by adding functionality to the architecture at each increment.

![RUP_phases_and_disciplines](./Resources/RUP_phases_and_disciplines.png)

In the image above, the RUP phases are shown as columns and disciplines as rows. Each discipline's activity is displayed as the thickness of the lines. For instance, there is little effort put into tests during the Inception phase. However, between the Construction and Transition phases, a significant amount of work is involved.

> [!NOTE] Example
> For example, in a software development project, the Inception phase might involve defining the project scope and identifying key stakeholders. During the Construction phase, the development team would focus on building the core functionality, while the Transition phase would involve deploying the software and training end-users.

### UN/CEFACT's Modeling Methodology (UMM)

UN/CEFACT's Modeling Methodology (UMM) is a UML modeling approach. It designs the business services that each business partner must provide to collaborate. UMM provides the business justification for the service to be implemented in a service-oriented architecture (SOA).

> [!NOTE] Example
> For instance, in a supply chain management system, UMM can be used to model the business services required for collaboration between suppliers, manufacturers, and retailers. This ensures that each partner understands their role and the services they need to provide.

### IEEE 1471-2000

The IEEE 1471 is a standard for system, software, and enterprise architectures. It has been replaced by the ISO/IEC/IEEE 42010 standard, which will be described later on. IEEE 1471 is a base of the **Zachman [Framework](../Glossary/Architecture_framework.md)**.

![IEEE 1471 description image](Resources/IEEE_1471_Description_image.png)

Let's discuss the diagram shown above. When describing a system, the system needs to have (at least) a mission. This system will be deployed in an environment (e.g., software deployed on a server/machine) and will influence it. The system has an architecture and one or multiple stakeholders. This architecture must be described by one or multiple views. These views allow the creation of viewpoints that are addressed to the stakeholders depending on the concerns. These views, viewpoints, and architecture description are related to models, which are the data of the architectural description.

> [!NOTE] Example
> For example, in a healthcare system, the mission might be to improve patient outcomes. The system would be deployed in a hospital environment and would influence patient care processes. The architecture would be described by views such as the clinical workflow view and the patient data view.

### IEEE 42010

ISO/IEC/IEEE 42010 addresses the creation, analysis, and sustainment of architectures of systems through the use of semantically rigorous architecture descriptions.

> [!IMPORTANT]
> This standard is the base of TOGAF and other current [frameworks](../Glossary/Architecture_framework.md). **You might need to understand ISO-42010 before learning TOGAF.**

For more detail please refer to : [Github - Nicolas Goyon - ISO 42010](https://github.com/nicolas-goyon/ISO-42010)

## Enterprise Architecture Frameworks

### Zachman Framework

John Zachman introduced the first and best-known enterprise [architecture framework](../Glossary/Architecture_framework.md) (Zachman 1987). It depicts the design artifacts that constitute the intersection between roles in the design process (**Owner, Designer, Builder**) and the product abstractions (**What, How, Where, Who, When, Why**).

![Zachman](Resources/Zachman.png)

For instance :

|                                     | What                                                          | How                                                            |                              Where                               | Who                                                              | When                                                    | Why                                                  |                         |
|-------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------|:----------------------------------------------------------------:|------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------|-------------------------|
| **Executive perspective**           | Inventory identification *(list: inventory types)*            | Process identification *(list: processes types)*               |     Distribution identification *(list: distribution types)*     | Responsibility identification *(list: responsibility types)*     | Timing identification *(list: Timing types)*            | Motivation identification *(list: motivation types)* | **Scope context**       |
| **Business Mgmt perspective**           | Inventory definition *(Business entity & relations)*          | Process definition *(business transform & input/output)*       |   Distribution definition *(business location & Connections)*    | Responsibility definition *(Business Role & Work products)*      | Timing Definition *(Business Interval & moments)*       | Motivation definition *(Busines End & means)*        | **business concept**    |
| **Architect perspective**           | Inventory representation *(System entity & relationship)*     | Process representation *(System transform & input/output)*     |   Distribution representation *(System location & connection)*   | Responsibility representation *(System Role & Work product)*     | Timing Representation *(System interval & moments)*     | Motivation representation *(System end & means)*     | **System Logic**        |
| **Engineer perspective**            | Inventory specification *(Technology entity & relationship)*  | Process specification *(Technology transform & input/output)*  | Distribution specification *(Technology location & connection)*  | Responsibility specification *(Technology Role & Work product)*  | Timing specification *(Technology interval & moments)*  | Motivation specification *(Technology end & means)*  | **Technology Physics**  |
| **technician perspective**          | Inventory Configuration *(Tool entity & relationship)*        | Process Configuration *(Tool transform & input/output)*        |    Distribution Configuration *(Tool location & connection)*     | Responsibility Configuration *(Tool Role & Work product)*        | Timing Configuration *(Tool interval & moments)*        | Motivation Configuration *(Tool end & means)*        | **Tool components**     |
| **Enterprsise perspective (users)** | Inventory Instantiations *(Operations entity & relationship)* | Process Instantiations *(Operations transform & input/output)* | Distribution Instantiations *(Operations location & connection)* | Responsibility Instantiations *(Operations Role & Work product)* | Timing Instantiations *(Operations interval & moments)* | Motivation Instantiations *(Operations end & means)* | **Operation instances** |
|                                     | **Inventory Sets**                                            | **Process flows**                                              |                    **Distribution networks**                     | **Responsibility assignments**                                   | **Timing cycles**                                       | **Motivation intentions**                            |                         |

> [!NOTE] Example
> For example, in an e-commerce platform, the Executive perspective might identify the inventory types (What), process types (How), and distribution types (Where). The Business Management perspective would define business entities and their relationships, while the Architect perspective would represent the system entities and their relationships.

### The Open Group Architecture Framework (TOGAF)

TOGAF has the following main components :

1) **Architecture Capability [Framework](../Glossary/Architecture_framework.md)**: Addresses the organization, processes, skills, roles, and responsibilities.
2) **Architecture Development Method (ADM)**: Provides a 'way of working' for architects.
3) **Architecture Content [Framework](../Glossary/Architecture_framework.md)**: Composed of four closely interrelated architectures :
   1) Business Architecture
   2) Data Architecture
   3) Application Architecture
   4) Technology (IT) Architecture
4) **Enterprise Continuum**: Comprises various reference models, such as:
   1) Technical Reference Model
   2) The Open Group's Stardards Information Base (SIB)
   3) The Building Blocks Information Base (BBIB)

Here is a basic illustration of TOGAF :
![TOGAF Illustration](Resources/TOGAF_Illustration.png)

#### TOGAF Architecture development method

TOGAF's ADM is iterative, over the whole process, between phases, and within phases. For each iteration of the ADM, a fresh decision must be taken as to :

- The **breadth (width)** of coveration of the enterprise to be defined.
- The **level (depth)** of detail to be defined.
- The **extend of the time horizon** aimed at, including the number and extend of any intermediate horizons.
- The **architectural assets** to be leveraged in the organisation's Enterprise Continuum. This includes assets created in previous iterations of the ADM cycle within the enterprise and the assets avaliable elsewhere in the industry.

![ADM](Resources/ADM.png)

> [!NOTE] Example
> For instance, in an enterprise-wide IT transformation project, the ADM might start with a broad coverage of the entire organization. The level of detail would be high for critical systems, and the time horizon might extend over several years with intermediate milestones for key deliverables.

### OMG's Model-Driven Architecture (MDA)

The OMG has extended the focus of MDA to the Computation-Independent Model (CIM) layer, which covers the business aspects of a company. Thus, MDA comprises three abstraction levels with mappings between them :

1. **Computation-Independent Model (CIM)**: The requirements for the system are modeled in a CIM describing the situation in which the system will be used.
2. **Platform-Independent Model (PIM)**: Describes the operation of a system while hiding the details necessary for a particular platform, from one platform to another.
3. **Platform-Specific Model (PSM)**: Combines the specifications in the PIM with the details that specify how that system uses a particular type of platform.
