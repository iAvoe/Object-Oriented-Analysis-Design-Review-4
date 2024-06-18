# Object-Oriented-Analysis-Design-Review-M4

## Problem Domain

A portion of area or domain that the users' business need we (analysts) care about
- In scope of the system we design
- Comprised of multiple collections of "things" (one actor per collection)

## "Things" Problem Domain Objects / Classes

A small set of problem domain for one actor, involving items an actor interacts with, objects in system possesses. They have little to do with programming knowledges, but must be fully understood before development

For embedded software for telecomms, they are:
  - Ethernet
  - VoIP
  - Video protocols
  - Video codecs
For the Ridge Mountain Olympics CSMS, they are:
  - Sales
  - Shippers
  - advertisement
  - Customers
  - Invoices
  - Payments
  - Products
For photography business, they are:
  - Camera
  - Filming equipments
  - eCommerce
  - advertisement
  - Shippers (ship physical photo copies)
  - Clothing
  - Customers
  - Invoices
  - Payments
  - Products

Modeled as domain classes or data entities

## Identify "Things" (Problem Domain Objects / Classes)

### Brainstorming technique

Identify in which developers work with users in an open group setting

1. Identify a user and a set of use cases.
2. Brainstorm with the user to identify problem domain objects / classes involved, when carrying out the use case
3. Use "types of things" / categories to systematically question potential things, such as:
  - Any tangible things you store information?
  - Any locations involved?
  - Any other people / partners / firms you have to meet or talk to?
  - Any other people playing a role in your job?
4. Continue to work with all types of users and stakeholders to expand the brainstorming list
5. Merge the results, eliminate any duplicates, and compile an initial list

### Noun technique

Identify by finding & classifying the nouns in a dialog or description

1. Study use cases, actors, other information (e.g., input & outputs) about the system
2. Study other info from existing systems, current procedures, current reports / forms
  - Goal: identify all nouns
3. Refine the gathered list of nouns:
  - Is it important
  - Is it in scope
  - Is it really a thing (e.g., a report or an arribute is not)
  - Is it still unclear? (requiring further research)
4. Write a master list of all nouns identified, add note on items that should be included
5. Review the list with users, stakeholders, and team members and then refine the list of things in the problem domain

### Attributes of "Things" (Problem Domain Objects / Classes)

The noun technique involves listing all the nouns that come up in discussions or requirements, but many of these nouns are actually attributes, not things.
- e.g., "Ethernet" is not an attribute, "password", "date" or "color" is an attribute

### Associations Among "Things" (Problem Domain Objects / Classes)

**Cardinality**
- The possible amount of association
- e.g., "1 ----> 3" means 1 left can associate with 3 right

**Multiplicity**
- The min and max possible amount of association
- e.g., "0..1 ----> 1..3" means 0 to 1 left can associate with 1 to 3 right
- UML avoids the term cardinality and only uses multiplicity

**C-M Mixed Representation**
- e.g., "0..1 ----> 3" has left multiplicity, and right cardinality

**Binary associations**
- Associations between exactly two distinct types of things

**Unary association**
- Association between two instances of the same type of thing

**Ternary association**
- Association between exactly three distinct types of things

**N-ary association**
- Association between n distinct types of thing

## Entity Relationship Diagram (ERD)

A diagram consisting of data entities (i.e., sets of things) and their relationships

**Data entities**
- The term used in an ER diagram to describe sets of things or individual things

**Crow's feet notation**
- "1, 0, multiple" represented by "|, ○, >, <" on the association line

**Semantic net**
- A graphical representation of an individual data entity and its relationship with other individual data entities
- Helps to understand and design an ERD model
  - e.g., Join places order:
    - Actor entity: Join
    - Order entity: id 1, feb 4
    - Item entity: microphone

**Attributes**
- descriptive pieces of information about things or objects

**Identifier or key**
- an attribute the value of which uniquely identifies an individual thing or object

**Compound attribute**
- an attribute that consists of multiple pieces of information but is best treated in the aggregate

## Generalization / Specialization

**Abstract class**
- Allow subclasses to inherit characteristics but cannot have instances. In Italics

**Concrete class**
- Standard class, can have instances

**Inheritance**
- Inherit from a parent class's variables and methods
- e.g., SavingAccount class can inherit from Account class

## State Machine Diagram

A diagram which shows the life of an object in states and transitions

**Origin state**
- the original state of an object before it begins a transition

**Destination state**
- Represented as boxes with rounded corners
- the state to which an object moves after completing a transition

**Pseudostate ●**
- the starting point in a state machine diagram. Noted by a black circle

**Action-expression**
- some activity that must be completed as part of a transition

**Concurrent paths**
- Represented as a cross-off line, parallel paths arrive at this line at the same time
- When multiple paths are being followed concurrently

**Trigger →**
- The cause of the transition (signal, event, temperature, datetime)
- "(state)—— Trigger cond. [Guard cond.] / Effect cond. ——>(state)"

**Guard →**
- True/False test to see whether a transition can fire
- "(state)—— Trigger cond. [Guard cond.] / Effect cond. ——>(state)"

**Effect**
- An action which will be invoked directly on the object that owns the state machine as a result of the transition.
- "(state)—— Trigger cond. [Guard cond.] / Effect cond. ——>(state)"

## Quiz

### Noun & Brainstorming Technique

When analyzing the list of nouns to determine whether to exclude a particular noun as an important "thing," which of the following questions should be asked about the noun?
- Is it a synonym of an existing thing?
- Is it an output from the system?

When making a list of nouns to determine what are the important "things" for the new system, there are three question that should be asked about each noun. Which of the following is one of those questions?​
- ​Should it be researched further?

The noun technique can be thought of as a variation of the brainstorming technique.​
- False, they are very different

One technique to find the "things" that need to be included in the new system begins by starting with a user and the use cases and then try to identify the necessary informational "things." This technique is called the _______.
- Brainstorming technique

One technique for finding "things" that need to be in the new system is done by the analyst starts making lists of "things." He may do this from information and even without talking to the users extensively. This technique is called the _______.
- noun technique

When using the brainstorming technique it is often helpful to think about each use case and talking to users.​
- True

-----

### Attributes

An attribute whose value uniquely identifies an object is called a(n) _______.​
- key attribute

Descriptive properties of things in the problem domain are often documented as what?
- Attributes

A piece of information about a particular object is called a(n) _______.
- Attribute

In the traditional approach to system development, the system stores information about ____.​
- Data entities

-----

### Problem Domain

The specific area of the user's business need that is within the scope of the new system is called the _______.​
- ​problem domain

When identifying things in the problem domain, an analyst should focus primarily on tangible things about which information is required.​
- False

-----

### UML Relationships

Which of the following relationships would NOT be an appropriate way to describe a relationship between an employee and his/her manager?
- Association

As association class is frequently required for what kind of relationship?
- Many to many

A superclass only exists as part of a generalization/specialization.
- True

A class of objects is equivalent to a set of objects.
- True

____ is used to describe the relationship between two things of the same type, such as one person being married to another person.​
- Unary

The association shown on the above image is a(n) ________ association. 0.. 0.. both on customer
- Unary

If we modeled a "sale" and the "sale items" with a whole-part relationship, it would best be described as a _______ relationship.​
- Composite

A relationship between a "sports team" and the players, coaches, and sponsor would be described as what kind of relationship?​
- Aggregation

A concept that allows subclasses to share the characteristics of their superclasses is called ____.​
- inheritance

This notation indicates what type of association?​ Upward arrow going to one box coming from three boxes
- Generalization/Specialization

_____ is based on the idea that people classify things in terms of similarities and differences.
- Generalization/Specialization

In a generalization/specialization relationship, it would not make sense for a class at the bottom of the hierarchy to be a(n) ______ class.​
- Abstract

If we modeled a "sale" and the "sale items" with a whole-part relationship, it would best be described as a _______ relationship.
- Composite

-----

### Entity Relationship Diagram

A synonym for cardinality (used with UML class diagrams) is ____.​
- multiplicity

The ERD crows feet cardinality constraint indicates a mandatory many relationship.​
- False

A measure of the number of links between one object and another object in a relationship is called the _______
- Cardinality

The number of associations that occur among specific things in an entity relationship diagram is called ____.
- Cardinality

The crows feet notation on an ERD is a type of _______ constraint.
- Cardinality

In UML the constraint denoted by "0..*" indicates what?
- An optional relationship

Which of the following is NOT true about a UML class.
- It has multiplicity.

A semantic net illustrates individual objects within a class diagram.
- True

Above cardinality constraint on the Order data entity indicates that there can be _____
- One or many orders

-----

### State Machine Diagram

For real-world objects the state of an object is the same as its _______
- Status condition

A state-machine diagram is usually developed for every class in the problem domain class diagram.​
- False

Every state-machine diagram must have both origin states and destination states.
- True

The guard-condition on a transition indicates what?​
- Whether the transition fires.

A state machine diagram is used to document the states and transitions of a(n) _______ .
- Object

One way to determine whether an occurrence is an event or part of the interaction before or after an event is by asking if any long pauses or intervals occur.
- False: a event can be milliseconds long

A fact finding user interview can usually be completed in one comprehensive session.
- False

Once a Scrum team has agreed on a goal and has selected items from the backlog list, the scope of the sprint is frozen.
- True

During analysis the analyst should be sure to identify system control events such as the user logging in or out.
- False

A state event is an event that occurs when something happens outside the system that triggers the need for processing.
- False

An activity diagram and the flow of activities in a fully developed use case description serve the same purpose.
- True

The final decision of project scope in an Agile project rests with the users.
- False

Activity diagrams are not helpful when the flow of activities is too complex.
- False

Since the Agile philosophy embraces change, project scope management is not important for Agile projects.
- False

In a state machine diagram, a state is represented by a(n) ____.
- Oval

To document ____, draw a composite state with the lower portion divided into multiple compartments for each concurrent path of behavior.
- Concurrent behavior of a single object

Which of the following documents information about classes that are part of the problem domain of the user?
- State machine diagram

Which of the following is NOT a step in the development of a state machine diagram?
- Expand the name of each state to identify concurrent activities

What is a trigger in state machine diagram?

Which of the following is NOT an element in a transition label?
- Trigger

A message event causes what to happen?
- Transition to fire

In a transition label in a state machine the syntax is A(B)[ C ]/D. The D stands for what?​
- action
