# Stylt

A programming language built to enable its creator to code what they wanted in the way they wanted.

### Primary Design Criteria (**PDC**):
  
  - All language constructs and concepts should be as minimal and orthogonal as possible
  - The base language should Maximize Expressivity and the Abilities of Computational Constructs
  - The Language should have Well Defined and Foramlly Specified Semantics:
    - The Language should enable the specification of Categorical Semantics and the more traditional Denotational Semantics should be able to be discussed
    - Operational Semantics should be presentable for both the level of 'program' execution and for compilation (which are ultimately the same)
  - Language Primitives, syntactically, type theoretically, and semantically, should be situated at the lowest possible level of abstraction
  - The core design and implementation of any language primitive, feature, or construct is explicitly targeted at the efficient creation of opinionated, composable abstractions rather than providing those abstractions at the language level
  - The Syntax of the language should enable all the above criteria to be Maximally Expressive and Maximally Powerful

### Design Decisions reached pursuing **PDC** and Inspirations for those Decisions:
  
  - Language Primitives motivated by Category Theory, Classical Linear Logic, and a novel Process Calculus
  - Many common computational systems (i.e. lambda calculus) and type systems (i.e. session types) can be and SHOULD BE encoded in the language merely as distinct modes, types/Universes, or encoded abstractions not as privileged sublanguages or type theories
  - Several common extentions to simple type theory (i.e. parametric and ad-hoc polymorphism, subtyping, type refinement, etc) are subsumed into the orthoganal basic constructs of the language and the interactions between those constructs
    - Parametric Polymorphism (what little there may be) is achieved by combining dependent types and multi-stage programming
    - Ad-Hoc Polymorphism is achieved almost soley by multi-phase programming
    - Subtyping and Type Refinement are derivative achievements of the adjoint modal type theory
    - examples can continue...
  - The 'Type' System draws heavily from prior work in dependent types, modal logic, and *-Autonomous Categories
    - The work of Benton, Reed, Pfenning, et al on Modal Logic and Modal Type Theories and the subsequent work on Adjoint logic is a primary influence on the languages design
    - The continuing academic work on Multi-Mode Multi-Modal Dependent Type Theory influence several key aspects of the design
    - The work on Contextual Modal Logic and Types
    - Type is used in scare quotes because, as Robert Constable said, Type Theory, and particulary the Function type  'is the most comprehensive theory of effective computability in the sense of deterministic sequential computation'; however, the basis for computation in the language is explicitly non-sequential (i.e. concurrent) and inherently non-deterministic (determinism must be forced on the system via 'types' and program design)
      - There seem to be several good reasons for differintiating the language's 'type' system and the traditional (and very well developed) usage and meaning of the term 'type theory'
        1) Explicitly avoid confusion where similar terminology is used to take advantage of similar semantics
        2) Explicitly disclaim those positions and uses which are contrary or wildly divergent to the tradition of type theoretical study
        3) The language attempts to explicitly be capable of encoding traditional type theory and then, when discussing the encoding or terms within that encoding, the differentiation between the underlying 'type' theory and the encoded type theory must remain seperable
  - Semantics are expressed in a Static/Dynamic split presentation in the informal and formal definition and specification of the language
    - The presentation is most clearly inspired by the work of Robert Harper as laid out in "Practical Foundations for Programming Languages"
    - However, there are several departures and significant alteration to accomodate the Modality Enforced Multi-Phase Semantics
  - Syntax is inspired and informed by the underlying composition-based semantics



### A List of Anti-Features:
  
  - 'Developer Experience', at the expense of any PDC
    - An example would be having type inference at the expense of restrictions on expressivity
    - Another example would be having implicit arguments, types, modes where such would require a restriction on orthoganality
  - Simplification of base language to appeal to inexperienced users
    - Any 'simplification' would be implemented as a '#lang' style abstraction layer/mode
  - Adherence to conventions, prior languages, or alledged concensus where such adherence would cut against any PDC
  - Removal or Restriction of capabilities, either computationaly or syntactically, to satisfy the needs of large scale development
    - There will be methods to allow large scale and distributed development to enforce requirements and specifications as needed and such will have no effect of the base language
  - Sacrifice of PDC or specified development goals to satisfy or appeal to any external group of developers or commercial interests