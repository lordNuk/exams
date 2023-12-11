# Big picture
one of the hallmarks of intelligence is the ability to reason

reasoning allows us to solve problems

if we want to build intelligent machines, we must be able to *automate reasoning*.

*logic* is the study of how we reason correctly.
goals of logic:
  - to represent knowledge of the world
  - reason with that knowledge

## Knowledge
ongoing debate among philosophers (definition of knowledge)

for now, lets define it as:
  - statements: *facts, info, descriptions*
  - regarded as *true/correct* or at least highly probable to be true.

knowledge is acquired through experience or education
  - precieving, discovering, or learning

simple enought, but:
  - communication?
  - manipulating it to draw conclusions and derive new knowledge.

## Inference
conclusion reached on the basis of evidence and reasoning, for eg: statistical inferrence.

## Reasoning
the drawing of conclusions(inferences) from known or assumed knowledge.

there are many ways to reason. for eg: logical deductive reasoning (i.e. syllogism)

## Knowledge representation
### reasoning with 'natural language'
problematic:
- for eg: 
  - knowledge: 
    - a penny is better than nothing.
    - nothing is better than world peace.
  - conclusion:
    - therefore, a penny is better than world peace.
- natural language is tricky (often ambiguous)!
  - an impractically huge knowledge base may be needed to understand context.

#### formal representation:
solving problems in a particular domain often requires knowledge of the objects and how to reason in that domain.

formal representation:
  - standardizes objects and reasoning
  - ex:
    - logic
    - programming languages
    - ontologies

mapping is needed to realte natural to formal.

consequence:
  - less flexible

*"the intended role of knowledge rep. in AI is to reduce problems of intelligent action to search problems."* -ginsberg (93)

### representation and mapping
inital facts(NL)--------------mapping based on sematics------>formally represented facts(formal lang)

formally represented facts----formal reasoining ------------->formally represented facts(formal lang)  

formally represented facts----mapping based on sematics------>conclusions(natural lang)

### symbol structures
knowledge must be represented:
  - effectively, consistently and in a meaningful way
  
symbol structures represent bits of knowledge:
  - for eg:
    - symbol 'blue' denotes a particular color
    - symbol structure blue(car) to denote the fact that car is of blue color.
  - can be any physical medium, like punchcards sym. str.
  - computers make it even easier:
    - Facts: data structres (array, lists, dict, dataframes, etc)
    - Reasoning: program code.

### requirements of good formal knowledge rep. schemes
- representational adequacy:
  - i.e ablility to represent all knowledge to reason with.
- infrential adequacy:
  - allow new knowledge to be inferred from basic set of facts.
  - don't innumerate -ves that could be covered by one +ve.
- infrential efficiency:
  - ability to make inferences efficiently and easily.
- clear syntax and semantics:
  - know allowed symbols/expressions and what they mean.
- naturalness:
  - reasonably natural and easy to use.

#### natural representation
use names for symbols that are meaningfull.

ex: 
  - natural fact: "if someone has a headache they should take aspirin."
  - rep. 1: if(x, h, a)
  - rep. 2: if symptom(x, headache) then medication(x, aspirin)

latter is more readable and easier to deal with.

## Knowledge representation techniques in AI
four major ones are:
1. Logical rep
2. Semantic networks
3. Production rules
4. Frames rep




