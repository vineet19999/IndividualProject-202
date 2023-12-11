# IndividualProject-202
CMPE202-Individual Project
# Part 1: Design

## Primary Objective:
The primary challenge is to devise a system for processing a CSV file containing credit card records. The system must extract the card number, validate its authenticity, and instantiate the appropriate credit card class based on the card issuer.

## Secondary Challenges:
- Dynamic creation of instances for the relevant credit card class.
- Identification of the credit card type (Visa, MasterCard, etc.) from the CSV record.

## Design Patterns:

-  Strategy Pattern: 
  - Employed for credit card validation.
  - Establish the CreditCardValidator interface with distinct implementations for various card types.

-  Factory Method Pattern: 
  - Employed to generate instances of credit card classes corresponding to the card issuer.
  - Each credit card type (Visa, MasterCard, etc.) possesses its own factory method.

## Implications:

1.  Flexibility and Extensibility: 
   - The Factory Method Pattern enhances flexibility, facilitating the seamless addition of new credit card types.

2.  Encapsulation: 
   - Encapsulation of the object creation process within factories improves maintainability and readability.

3.  Consistency: 
   - Ensures uniformity in object creation, as each factory produces instances adhering to specific rules.

4.  Testability: 
   - Bolsters testability by allowing the straightforward substitution of mock or test implementations.

# Part 2: Extension

## Design Overview:

-  Template Method Pattern: 
  - Defines a template method for processing credit card records from diverse file formats.
  - Subclasses contribute implementations for specific steps.

-  Factory Method Pattern: 
  - Utilized for generating instances of file format processors (CSV, JSON, XML).
  - Each factory is dedicated to a specific file format.

-  Strategy Pattern: 
  - Applied for credit card validation.

## Consequences of Template Method Pattern:

1.  Limited Code Reusability: 
   - Concrete steps in subclasses may lack independent reusability.

2.  Inflexibility: 
   - Subclasses must conform to the overall structure, restricting flexibility.

3.  Tight Coupling: 
   - Modifications to the template method may impact all subclasses.

4.  Difficulty in Refactoring: 
   - Refactoring may pose challenges, necessitating synchronized changes across subclasses.
