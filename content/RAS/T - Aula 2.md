19 Setembro 2023 - #RAS

## Contents
1. [[RAS/T - Aula 2#Definition of Requirement|Definition of requirement]]
2. [[RAS/T - Aula 2#Functional requirements|Functional requirements]]
3. [[RAS/T - Aula 2#Non-functional requirements|Non-functional requirements]]
4. [[RAS/T - Aula 2#4. User and system requirements|User and system requirements]]
5. [[RAS/T - Aula 2#Recap|Recap]]

## 1. Definition of Requirement
The requirements express the users necessities and restrictions that are
placed on the system.

A **requirement** is a capacity that a system must possess, to satisfy the
users necessities.

The IEEE 610.12-1990 standard definition divides requirements into
two alternatives:
1. user needs
2. system capacities

Requirements can be divided into:
1. functional requirements
2. non-functional requirements

A r**equirement that for a stakeholder** can be perceived
as being **functional**, can be considered as **non-functional**
for **a different one**.

> [!info] A candidate requirement is a requirement that was identified by some elicitation technique.


## 2. Functional requirements

> [!tip] Definition
> A functional requirement describes a functionality to be made
available to the users of the system.

- This type of requirements should not mention any technological issue.
- Ideally, functional requirements must be independent of design and
implementation aspects.

> [!note]- Note: Cohesion and Completion
> Collectively, the set of functional requirements must be complete and
coherent. The set is:
> - *coherent*, if there are no contradictions among its elements;
> - *complete*, if it considers all the necessities that the client wishes to see
satisfied.
>
> Defining complete requirements is the most difficult attribute to
achieve or evaluate.

> [!note]- Note: Implicit and Explicit Requirements
> Implicit requirements are referred like that because the client may not be aware about these requirements.
> 
> An **implicit requirement** is a requirement included by the development team, based on the domain knowledge that it possesses, in spite of not having been explicitly requested by the stakeholders.
> 
> An **explicit requirement** refers to a requirement that was requested by the clients and that is represented in the documentation.


## 3. Non-functional requirements

> [!tip] Definition
> A non-functional requirement corresponds to a set of restrictions
imposed on the system to be developed.

- Alternative terms: quality requirement or quality attribute
- It establishes how attractive, fast, or reliable the system is.
- It includes time constraints, restrictions in the development process, or
adoption of standards.

> [!example]- Example: Technological restriction
> The product must be developed in C++.

> [!info] **A non-functional requirement does not change the essence of the system functionalities.**


- Non-functional requirements are applicable to the system as a whole
and not just to some of its parts, as, generally, non-functional requirements **cannot be modularized**.

- The non-functional requirements are frequently **emergent properties** of the system at hand. *An emergent property of a system is a property that can be associated with the system as a whole, but not individually to each of its components.*
	- *Reliability* is a good example of an emergent property.


> [!info] **Non-functional requirements are crucial to decide the system architecture.**



### 3.1 Classification of non-functional requirements

> [!tip]- Classification: Sommerville (2010)
> - **product requirements**: characterise aspects of the behaviour of the system itself (*reliability, performance, efficiency, portability, usability, testability, and readability*).
> -  **organisational requirements**: come from strategies and procedures established in the context of the manufacturing process of the system or the client organisation (process standards and implementation requirements).
> - **external requirements**: have origin in external factors to the system and the development process (interoperability, legal, and ethical requirements).

> [!tip]- Classification: Roberson and Roberson (2006)
> - **appearance**: the aspect and the aesthetics of the system;
> -  **usability**: the easiness of utilization of the system and everything that permits a more friendly user experience;
> - **performance**: aspects of speed, real-time, storage capacity, and execution correction;
> - **operational**: characteristics about what the system must do to work correctly in the environment where it is inserted;
> - **maintenance and support**: attributes that allow the system to be repaired or improved and new functionalities to be added;
> - **security**: issues related to access, confidentiality, protection, and integrity of the data;
> - **cultural and political**: factors related to the stakeholders culture and habits;
> - **legal**: laws that apply to the system so that it can operate.

#### 3.1.1 Usability
 - **Ease of use** is related to the efficiency of utilizing a system and with the mechanisms that reduce the errors made by the users.
 - **Personalization** is associated with the capacity of adapting the system to the tastes of the users.
 - **Ease of learning** is concerned with the way users are trained to use the system.
 - **Accessibility** indicates how easy it is to use the system, for people who
are somehow physically or mentally disabled.

> [!example]- Example: Usability requirements
> 1. The product shall be easy to use for illiterate persons.
> 2. The product shall be intuitive to use for children with 4 years old.
> 3. The product shall be usable by visually impaired persons.

#### 3.1.2 Maintenance and support
- System maintenance is divided into four types: preventive, corrective, perfective, and adaptive.
- **Modifiability** is related to maintenance and is dependent on how easy it is to locate the components that must be changed.

> [!example]- Example: Maintenance and support requirements
> 1. The source code of the product programs should contain comments.
> 2. The product must be prepared to be translated to any language.

#### 3.1.3 Legal
> [!example]- Example: Legal requirements
> 1. The product shall be aligned with the PMBoK guide.
> 2. The product shall be certified by the Taxing Authority.
> 3. The product shall fulfil with the copyright.



## 4. User and system requirements

A **user requirement** represents:
1. a functionality that the system is expected to provide to its users;
2. a restriction that is applicable to the operation of that system.

- These requirements are related to the problem domain.
- They are normally expressed without great mathematical rigour, using natural language and informal diagrams.


A **system requirement** constitutes a more detailed specification of a requirement, being generally a formal model of the system. These requirements are oriented towards the solution domain, and are documented in a more technical language than the one
adopted for the user requirements.

### 4.1 Problem domain
- The requirements result from necessities that exist in the problem domain to be addressed.
- User requirements should be described with the problem domain terminology.





# Recap
1. Requirements represent the necessities of the users and the constraints that are applied to a system and that must be considered throughout the development.
2. The requirements can be classified, according to a first criterion, as either functional or non-functional.
3. Non-functional requirements are divided in 8 different types: appearance, usability, performance, operational, maintenance and support, security, cultural and political, and legal.
4. The requirements can be designated as either user or system requirements.
5. User requirements are related to the problem domain and are usually expressed in a natural language.
6. A system requirement is oriented towards the solution domain and is a detailed specification of a requirement, generally in the form of a formal model of the system.

[[Próxima aula]]
[[RAS/PL - Aula 1|Aula prática]]