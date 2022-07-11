# Stylt

A programming language built to enable its creator to code what they wanted in the way they wanted.

###Primary Design Criteria (**PDC**):
  
  - All language constructs and concepts are to be as minimal and orthogonal as possible, while maintaining maximal expressivity
  - Language Primitives (syntax, type theoretic, and semantically) are designed to be as low-level (in the sense of Perlis) as possible
  - Expansive and Expandable Type Theory
  - Categorical Semantics
  - Syntax that enables the above considerations to be maximally expressive

###Design Decisions reached pursuing **PDC**:

  - Language Primitives motivated by a Curry-Howard Correspondence between a novel Process Calculus and Classical Linear Logic
  - Multi-Mode Multi-Modal Dependent Type Theory
  - Semantics are expressed in a Static/Dynamic split presentation, inspired by the work of Robert Harper as laid out in "Practical Foundations for Programming Languages"
  - Syntax is inspired and informed by the underlying composition-based semantics 