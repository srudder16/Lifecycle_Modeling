# Lifecycle Modeling Language (LML) v2.0 — Certification Exam

50 multiple-choice questions based on the LML Specification, Version 2.0 (April 23, 2025). Each question has one (1) correct answer. 
<!-- Any update to this needs to be validated against the answer key -->
---

## Section 1: ERA Fundamentals & Documentation Conventions (Q1–10)

**1.** In LML's ERA model, what does an "attribute" describe?
A) A distinct class of information
B) An element defined using an entity class
C) A property of an entity class or a relationship
D) A possible link between two or more classes

**2.** Which documentation convention is used when referencing an LML entity class in running text?
A) Italics, first letter lowercase
B) Bold, first letter capitalized
C) Underlined, first letter lowercase
D) Bold italics, first letter capitalized

**3.** How is a relationship name formatted when referenced outside of a specification heading?
A) Bold, first letter capitalized
B) Italics, first letter lowercase
C) Bold italics, first letter lowercase
D) Underlined, first letter lowercase

**4.** How is an attribute on a relationship formatted in running text?
A) Bold
B) Italics
C) Underlined, first letter lowercase
D) ALL CAPS

**5.** What is the standard parent-child relationship used by all LML classes?
A) traced from / traced to
B) decomposed by / decomposes
C) related to / relates
D) specified by / specifies

**6.** What three attributes does every LML entity class possess?
A) name, type, and value
B) name, number, and description
C) number, units, and description
D) name, description, and status

**7.** What is required for every LML entity instance to be properly identified?
A) A UUID must be assigned
B) A name or a number must be populated
C) A description must be populated
D) Both name and number are mandatory

**8.** What key addition does LML make to the classic Entity-Relationship-Attribute (ERA) model?
A) Attributes on entity classes only
B) Multiple inheritance between entity classes
C) Attributes on relationships
D) Mandatory UUIDs for all instances

**9.** In LML, how must relationships be defined?
A) Only in the forward direction
B) In both directions, with unique names using the same verb
C) In both directions, with different verbs for each direction
D) Only as reflexive relationships

**10.** Which statement about child class inheritance is correct?
A) A child class inherits attributes and relationships from its parent, except the class designation
B) A child class inherits only the relationships, not the attributes, of its parent
C) A child class must redefine all inherited attributes
D) Types are inherited by subclasses from the parent entity class

---

## Section 2: Attribute Data Types (Q11–20)

**11.** What is the maximum character length of a Big_Text attribute?
A) 256 characters
B) 1,024 characters
C) 4,096 characters
D) 65,536 characters

**12.** What is the maximum character length of a Text attribute?
A) 64 characters
B) 256 characters
C) 1,024 characters
D) 65,536 characters

**13.** Which data type is a special case of Number restricted to values between zero and one hundred?
A) Multiplicity
B) Duration
C) Percent
D) Quality

**14.** Which data type represents a mathematical formula using a language such as LaTeX and can both visualize AND calculate values?
A) Equation
B) Computable
C) Formula
D) Big_Text

**15.** How does the Equation data type differ from the Computable data type?
A) Equation can calculate values; Computable can only visualize
B) Equation can only visualize the formula; Computable can visualize and calculate
C) They are functionally identical
D) Equation is deprecated in v2.0

**16.** What is the minimum number of options required to define an Enumeration?
A) One
B) Two
C) Three
D) There is no minimum

**17.** Which rule applies to both Enumeration and Multiselect data types?
A) Options may mix Text and Number data types
B) Repeated options within a set are not permitted
C) A minimum of five options is required
D) Selections must always be numeric

**18.** What distinguishes Multiselect from Enumeration?
A) Multiselect allows selection of one or more options; Enumeration allows only one
B) Multiselect is Text only; Enumeration is Number only
C) Multiselect requires a minimum of five options
D) There is no functional difference

**19.** Which data type represents a longitude/latitude pair on the surface of a body?
A) Physical
B) GeoPoint
C) Coordinates
D) URI

**20.** Which data type is described as representing the "goodness" of an entity, such as whether a requirement is Appropriate, Complete, or Correct?
A) Characteristic
B) Measure
C) Quality
D) Verification Requirement

---

## Section 3: LML Classes Overview (Q21–30)

**21.** How many parent classes does LML v2.0 define?
A) 8
B) 10
C) 12
D) 15

**22.** Which of the following is NOT one of the 12 LML parent classes?
A) Decision
B) Requirement
C) Risk
D) Time

**23.** According to Table 3-2, which entity class has the description "specifies an effort, operation, or a process by which inputs are transformed into outputs"?
A) Asset
B) Action
C) Input/Output
D) Task

**24.** Which class is described as an abstract class with no direct instances, having subclasses Conduit, Dependency, and Logical?
A) Location
B) Connection
C) Asset
D) Statement

**25.** Which class is the parent of the Resource subclass?
A) Action
B) Characteristic
C) Asset
D) Connection

**26.** Which class is the parent of the Requirement and Verification Requirement subclasses?
A) Artifact
B) Statement
C) Decision
D) Characteristic

**27.** What are the two subclasses of Action listed in Table 3-2?
A) Requirement and Verification Requirement
B) Task and Test Case
C) Resource and Measure
D) Conduit and Logical

**28.** Which class specifies "where an entity resides" and is itself an abstract class?
A) Location
B) Connection
C) Asset
D) Time

**29.** Which class specifies "the combined probability and consequence in achieving objectives"?
A) Decision
B) Cost
C) Risk
D) Characteristic

**30.** Which class specifies "a choice, a resolution, a conclusion, or a selected option"?
A) Decision
B) Statement
C) Risk
D) Requirement

---

## Section 4: LML Relationships (Q31–38)

**31.** Using the Action–Statement example in the specification, what is the correct reading of the relationship?
A) An Action is traced to a Statement; the Statement is traced from the Action
B) An Action is traced from a Statement; the Statement is traced to the Action
C) A Statement decomposes an Action
D) An Action specifies a Statement

**32.** What relationship connects an Action to the Asset that executes it?
A) performed by / performs
B) enabled by / enables
C) located at / locates
D) generated by / generates

**33.** Which relationship identifies the Risk resulting from a given class entity?
A) mitigates / mitigated by
B) causes / caused by
C) resolves / resolved by
D) results in / result of

**34.** Which relationship identifies a Characteristic that provides further information about a class entity?
A) references / referenced by
B) related to / relates
C) specified by / specifies
D) traced from / traced to

**35.** Which common relationship is explicitly excluded from the Connection abstract class (except for its Conduit and Logical subclasses)?
A) located at / locates
B) causes / caused by
C) decomposes / decomposed by
D) incurs / incurred by

**36.** According to the common relationships list, which relationship identifies the Decision that is empowered by a class entity?
A) results in / result of
B) enables / enabled by
C) causes / caused by
D) resolves / resolved by

**37.** Which relationship on the Action class represents an Action using a Resource that is released after the Action completes (rather than permanently used up)?
A) consumes / consumed by
B) seizes / seized by
C) generates / generated by
D) receives / received by

**38.** What attribute on the receives/received by relationship represents an enabling requirement for the Action to begin execution?
A) amount
B) trigger
C) origin
D) multiplicity

---

## Section 5: Common Attributes & Relationships (Q39–42)

**39.** Which three attributes are common to all LML entities?
A) name, number, description
B) name, type, value
C) number, status, type
D) name, units, description

**40.** What does the "related to" relationship's optional attribute "context" represent?
A) The location of the relationship
B) A description of the relationship
C) The cost incurred by the relationship
D) The originating artifact

**41.** Which relationship is used to link a Class Entity to the Location where it exists?
A) locates / located at (located at identifies the Location)
B) specified by / specifies
C) traced from / traced to
D) incurs / incurred by

**42.** Which relationship identifies the Time entity in which a class entity happens?
A) date resolved by / date resolves
B) occurs / occurred by
C) scheduled by / schedules
D) tracked by / tracks

---

## Section 6: Action, Task, and Test Case (Q43–48)

**43.** Which two attributes did LML v1.x place on Action that have since moved to the Task subclass in v2.0?
A) duration and type
B) start and status
C) name and number
D) priority and finish

**44.** What data type is used for the Task attribute "priority"?
A) Text
B) Boolean
C) Enumeration
D) Percent

**45.** In the Task class, what relationship identifies the Dependency (a subclass of Connection) between two Tasks?
A) tracked by / tracks
B) scheduled by / schedules
C) depends on / has dependent
D) traced from / traced to

**46.** Which Test Case attribute captures "conditions and setup details to be used during the test," such as parameters that simulate scenarios?
A) Setup
B) Event Conditions
C) Event Constraints
D) Expected Result

**47.** What relationship identifies the Asset entity included in and evaluated by a verification event (Test Case)?
A) references / referenced by
B) evaluates / evaluated by
C) performed by / performs
D) satisfies / satisfied by

**48.** A Test Case is traced from which entity, per its class relationships?
A) Requirement
B) Test Suite
C) Verification Requirement
D) Decision

---

## Section 7: Artifact, Asset, and Resource (Q49–50)

**49.** What does the "date published" attribute of an Artifact represent?
A) The date the Artifact was created internally
B) The date the Artifact was accessed, published, or uploaded to the knowledgebase
C) The date the Artifact expires
D) The date the Artifact was last modified

**50.** A Resource entity is a subclass of which parent class?
A) Characteristic
B) Connection
C) Asset
D) Input/Output

---


---