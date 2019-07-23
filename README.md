# Provably Awesome.    [![](img/badge.svg)](http://awesome.re)

This is a curated list of links and resources related to mathematical proofs
about the properties of computer programs.

#### Table of Contents

* [Languages](#languages) - Languages with good ability to use formal type
safety
* [Proof Assistants](#proof-assistants) - Interactive theorem provers used to
prove properties of programs.
* [Projects](#projects) - Projects involving provably correct code.
* [Books](#books) - Textbooks commonly referred to 
* [Courses](#courses) - Online courses (youtube, university courses)
* [More Links](#more) - Video presentations about formal proof of code topics

## Languages

* [Idris](https://www.idris-lang.org/) : Idris is a general purpose pure 
functional programming language with dependent types. Dependent types allow 
types to be predicated on values, meaning that some aspects of a program’s 
behaviour can be specified precisely in the type. It is compiled, with eager 
evaluation. Its features are influenced by Haskell and ML.
  * [Idris docs](http://docs.idris-lang.org/en/latest/)
  * [Idris tutorial](http://docs.idris-lang.org/en/latest/tutorial/index.html#tutorial-index)
  * [Theorem proving with Idris tutorial](http://docs.idris-lang.org/en/latest/proofs/index.html)
* [Agda](http://wiki.portal.chalmers.se/agda/pmwiki.php) : Dependently
 typed functional programming language. It has inductive families, i.e., data 
 types which depend on values, such as the type of vectors of a given length. 
 It also has parametrised modules, mixfix operators, Unicode characters, and an
  interactive Emacs interface which can assist the programmer in writing the 
  program.
  * [Agda Github](https://github.com/agda/agda)
  * [Agda User Manual](http://agda.readthedocs.io/en/v2.5.2/)

* [UR/Web](http://www.impredicative.com/ur/) : Ur/Web is Ur plus a special 
standard library and associated rules for parsing and optimization. Ur/Web 
supports construction of dynamic web applications backed by SQL databases. 
The signature of the standard library is such that well-typed Ur/Web programs 
"don't go wrong" in a very broad sense. Not only do they not crash during 
particular page generations, but they also may not:
  * Suffer from any kinds of code-injection attacks
  * Return invalid HTML
  * Contain dead intra-application links
  * Have mismatches between HTML forms and the fields expected by their handlers
  * Include client-side code that makes incorrect assumptions about the 
    "AJAX"-style services that the remote web server provides
  * Attempt invalid SQL queries
  * Use improper marshaling or unmarshaling in communication with SQL databases
    or between browsers and web servers
* [Haskell](https://www.haskell.org/) : An advanced, purely functional 
programming language. 

* [Liquid Haskell](https://ucsd-progsys.github.io/liquidhaskell-blog/) :
LiquidHaskell (LH) refines Haskell's types with logical predicates that let 
you enforce critical properties at compile time. (Guarantee functions are total,
keep pointers within bounds, avoid infinite loops, enforce correctness 
properties, prove laws by writing code)

* [Elm](http://elm-lang.org/) : A type-safe functional programming language for 
declaratively creating web browser-based graphical user interfaces. 
Implemented in Haskell. It generates JavaScript with great performance and 
*no runtime exceptions*.

## Proof Assistants

* [Coq](https://coq.inria.fr/) : Coq is a formal proof management system. It 
provides a formal language to write mathematical definitions, executable 
algorithms and theorems together with an environment for semi-interactive 
development of machine-checked proofs. 
[[current stable version](https://coq.inria.fr/download)]
[[reference manual](https://coq.inria.fr/distrib/current/refman)]
    * https://github.com/Ptival/PeaCoq
    * https://math-comp.github.io/mcb/
* [Isabelle](https://isabelle.in.tum.de/) : Isabelle is a generic proof assistant.
 It allows mathematical formulas to be expressed in a formal language and 
 provides tools for proving those formulas in a logical calculus.
 [[overview](https://isabelle.in.tum.de/overview.html)]
* [HOL](https://hol-theorem-prover.org/) : The HOL interactive theorem prover is
 a proof assistant for higher-order logic: a programming environment in which 
 theorems can be proved and proof tools implemented. Built-in decision 
 procedures and theorem provers can automatically establish many simple 
 theorems (users may have to prove the hard theorems themselves!) An oracle 
 mechanism gives access to external programs such as SMT and BDD engines. 
 HOL is particularly suitable as a platform for implementing combinations of 
 deduction, execution and property checking. 
 [[Other HOLS](https://hol-theorem-prover.org/other-hols.html)]
* [LEAN](https://leanprover.github.io/) : Lean is a new open source theorem 
 prover being developed at Microsoft Research, and its standard library at 
 Carnegie Mellon University. Lean aims to bridge the gap between interactive and 
 automated theorem proving, by situating automated tools and methods in a framework 
 that supports user interaction and the construction of fully specified axiomatic 
 proofs. The goal is to support both mathematical reasoning and reasoning about 
 complex systems, and to verify claims in both domains.
   [Online version](https://leanprover.github.io/live/latest/)
* [K Framework](http://www.kframework.org/index.php/Main_Page) : The K framework
 is a rewrite-based executable semantic framework in which programming languages, 
 type systems and formal analysis tools can be defined using configurations, 
 computations and rules. Configurations organize the state in units called cells, 
 which are labeled and can be nested. Computations carry computational meaning as 
 special nested list structures sequentializing computational tasks, such as fragments 
 of program. Computations extend the original language abstract syntax. K (rewrite) 
 rules make it explicit which parts of the term they read-only, write-only, read-write, 
 or do not care about. This makes K suitable for defining truly concurrent languages 
 even in the presence of sharing. Computations are like any other terms in a rewriting 
 environment: they can be matched, moved from one place to another, modified, or 
 deleted. This makes K suitable for defining control-intensive features such as 
 abrupt termination, exceptions or call/cc.
   * [K Tutorial](http://www.kframework.org/index.php/K_Tutorial) by [Grigore Rosu](https://github.com/grosu), [video playlist](https://www.youtube.com/watch?v=eSaIKHQOo4c&list=PLx_U8qR-tMtLQEDPvVk1y9gTIdUIWGaQd)
   * (https://runtimeverification.com/) : Company formed from K Framework people. 
     Runtime Verification Inc. is currently developing three core products: 
     * RV-Predict is a predictive runtime analysis tool focused on automatically 
       detecting concurrency errors in your programs. 
     * RV-Monitor is a development methodology and library generation tool allowing 
       for the monitoring and enforcement of user-selected properties at runtime. 
     * RV-Match is a tool allowing for exhaustive runtime verification to be performed 
       symbolically on all possible program paths, proving certain properties correct 
       for all possible executions of a given program.

## Projects

* [seL4](https://sel4.systems/) : The world's first operating-system kernel with 
an end-to-end proof of implementation correctness and security enforcement 
is available as open source. 
[[brochure](https://sel4.systems/Info/Docs/seL4-brochure.pdf)]
[[white paper](https://sel4.systems/Info/Docs/GD-NICTA-whitepaper.pdf)]
* [Certikos](http://flint.cs.yale.edu/certikos/) : Certified Kit Operating 
System.
  * **Certified OS Kernels**: Clean-slate design with end-to-end guarantees on 
    extensibility, security, and resilience.
    Without Zero-Day Kernel Vulnerabilities.
  * **Layered Approach**: Divides a complex
     system into multiple certified abstraction layers, which are deep 
     specifications of their underlying implementations.
  * **Languages and Tools**: New formal methods, languages, compilers and other 
  tools for developing, checking, and automating specs and proofs.

* [Compcert](http://compcert.inria.fr/) : The CompCert project investigates the 
formal verification of realistic compilers usable for critical embedded 
software. Such verified compilers come with a mathematical, machine-checked 
proof that the generated executable code behaves exactly as prescribed by the 
semantics of the source program. 
[[C compiler](http://compcert.inria.fr/download.html)]
* [Bedrock](http://plv.csail.mit.edu/bedrock/) 
[[tutorial pdf](http://plv.csail.mit.edu/bedrock/tutorial.pdf)] :
Bedrock is a library that turns Coq into a tool much like classical 
verification systems (e.g., ESC, Boogie), but niftier. In particular, 
Bedrock is:
  * **Low-level**: You can verify programs that, for performance reasons or 
  otherwise, can't tolerate any abstraction beyond that associated with 
  assembly language.
  * **Foundational**: The output of a Bedrock verification is a theorem whose 
  statement depends only on the predicates you choose to use in the key 
  specifications and on the operational semantics of a simple cross-platform 
  machine language. That is, you don't need to trust that the verification 
  framework is bug-free; rather, you need to trust the usual Coq proof-checker
  and the formalization of the machine language semantics.
  * **Higher-order**: Bedrock facilitates quite pleasant reasoning about code 
  pointers as data.
  * **Computational**: Many useful functions are specified most effectively by 
  comparing with "reference implementations" in a pure functional language. 
  Bedrock supports that model, backed by the full expressive power of Coq's 
  usual programming language.
  * **Structured**: Bedrock is an extensible programming language: any client 
  program may add new control flow constructs by providing their proof rules. 
  For example, adding high-level syntax for your own calling convention or 
  exception handling construct is relatively straightforward and does not 
  require tweaking the core library code.
  * **Mostly automated**: Tactics automate verification condition generation 
  (in a form inspired by separation logic) and most of the process of 
  discharging those conditions. Many interesting programs can be verified with 
  zero manual proof effort, in stark contrast to most Coq developments.

* [HACMS](https://www.darpa.mil/program/high-assurance-cyber-military-systems)
: High-Assurance Cyber Military Systems (HACMS)
. Dr. Raymond Richards. Technology for cyber-physical systems,
functionally correct and satisfying appropriate safety and security properties. 
Clean-slate, formal methods, semi-automated code synthesis from executable, 
formal specifications. HACMS seeks a synthesizer capable of producing a 
machine-checkable proof that generated code satisfies functional 
specs as well as security and safety policies, and development to ensure 
proofs are composable, allowing  components.
  [[more Darpa "formal" tagged links](https://www.darpa.mil/tag-list?tt=78)]
  [[verigames-crowdsourced formal verification](https://www.darpa.mil/news-events/2013-12-04a)]

* [Genode](http://genode.org/) : Genode is a novel OS architecture that is 
able to master complexity by applying a strict organizational structure to all
 software components including device drivers, system services, and applications. 

## Books
* [The Little Prover](https://mitpress.mit.edu/books/little-prover)
The Little Prover introduces inductive proofs as a way to determine facts about
 computer programs.

* [Certified Programming with Dependent Types](http://adam.chlipala.net/cpdt/) by
Adam Chlipala. Textbook about practical engineering with the Coq proof assistant.
The focus is on building programs with proofs of correctness, using dependent 
types and scripted proof automation.
[[Latest draft](http://adam.chlipala.net/cpdt/cpdt.pdf)]

* [Software Foundations](https://softwarefoundations.cis.upenn.edu/) by
Benjamin Pierce and others. The Software Foundations series is a broad 
introduction to the mathematical underpinnings of reliable software.

  * [Vol. 1:](https://softwarefoundations.cis.upenn.edu/lf-current/index.html)
[[read](https://softwarefoundations.cis.upenn.edu/lf-current/toc.html)]
[[download](https://softwarefoundations.cis.upenn.edu/lf-current/lf.tgz)]
Logical Foundations, serves as the entry-point to the series. It covers 
functional programming, basic concepts of logic, computer-assisted theorem 
proving,and Coq.

  * [Vol. 2:](https://softwarefoundations.cis.upenn.edu/plf-current/index.html)
[[read](https://softwarefoundations.cis.upenn.edu/plf-current/toc.html)]
[[download](https://softwarefoundations.cis.upenn.edu/plf-current/plf.tgz)]
Programming Language Foundations, surveys the theory of programming languages, 
including operational semantics, Hoare logic, and static type systems.

  * [Vol. 3: Verified Functional Algorithms](https://softwarefoundations.cis.upenn.edu/vfa-current/index.html)
[[read](https://softwarefoundations.cis.upenn.edu/vfa-current/index.html)]
[[download](https://softwarefoundations.cis.upenn.edu/vfa-current/vfa.tgz)]
Learn how to specify and verify (prove the correctness of) sorting algorithms, 
binary search trees, balanced binary search trees, and priority queues.

* HoTT : [Homotopy Type Theory: Univalent Foundations of Mathematics](https://homotopytypetheory.org/book/)
[[pdf](http://saunders.phil.cmu.edu/book/hott-online.pdfUnivalent)] 
Foundations of Mathematics is Vladimir Voevodsky’s new program for a 
comprehensive, computational foundation for mathematics based on the homotopical
interpretation of type theory. The type theoretic univalence axiom relates 
propositional equality on the universe with homotopy equivalence of small types. 
The program is currently being implemented with the help of the automated proof 
assistant Coq.

* https://math-comp.github.io/mcb/

## Courses

* [DeepSpec Summer School](https://www.youtube.com/channel/UC5yB0ZRgc4A99ttkwer-dDw)
41 Videos about deep specification. Coq videos, examples, tutorials.

* Adam Chlipala Videos:

  * 2017-12-29 CCC Presentation: [Coming Soon Machine-Checked Mathematical Proofs in Everyday Software and Hardware Development](https://media.ccc.de/v/34c3-9105-coming_soon_machine-checked_mathematical_proofs_in_everyday_software_and_hardware_development)

  * [Adam Chlipala Lecture 1, OPLSS 2015](https://www.youtube.com/watch?v=ORKAy_CHDYM)
  * [Bedrock: A Software Development Ecosystem Inside a Proof Assistant](https://www.youtube.com/watch?v=BSyrp-iYBMo)
  * [CACM August 2016 - Ur/Web: A Simple Model for Programming the Web](https://www.youtube.com/watch?v=J3XI6-aZZXk)
  * [Proof engineering Adam Chlipala](https://www.youtube.com/watch?v=yXLeyANzAC4)
  * [2015 Coq Proof Assistant and Its Applications to Programming-Language Semantics](https://www.youtube.com/playlist?list=PLt7hcIEdZLAnO7AawDQkHwE7RtwPDOFEc)
* [Type-Drive Development in Idris - Edwin Brady](https://www.youtube.com/watch?v=X36ye-1x_HQ)

* [Benjamin Pierce - Software Foundations Course](https://www.youtube.com/playlist?list=PLGCr8P_YncjUT7gXUVJWSoefQ40gTOz89)

* [Learning Automated Theorem Proving](https://cs.stackexchange.com/questions/820/learning-automated-theorem-proving) : Stackexchange post about learning


## More

* [Curry-Howard](https://en.wikipedia.org/wiki/Curry%E2%80%93Howard_correspondence) :
Curry–Howard correspondence refers to the direct relationship between computer
programs and mathematical proofs. This is also the idea of "proofs as programs",
and "propositions (formulas)-as-types".

* [Hoare logic](https://en.wikipedia.org/wiki/Hoare_logic)
Hoare logic (also known as Floyd–Hoare logic or Hoare rules) is a formal system 
with a set of logical rules for reasoning rigorously about the correctness of 
computer programs. 

* [Designing A Theorem Prover (Paulson, Cambridge, 1990)](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-192.pdf)

* [Rolf Rolles Program Synthesis in Reverse Engineering](https://www.youtube.com/watch?v=mFjSbxV_1vw)
...Assume you generate all possible programs...

* [The Open-Source seL4 Kernel. Military-Grade Security Through Mathematics - SFO17-417](https://www.youtube.com/watch?v=heSmrHzHcuM)
* [DARPA Hack Proof Drones](https://www.defensetech.org/2014/05/21/darpa-unveils-hack-proof-drone/)
  Uses SEL4, other RTOS
* [Pentagon Wants Unhackable Helicopters](https://www.engadget.com/2015/03/16/pentagon-wants-unhackable-helicopters/)
* [Hacker-Proof Code Confirmed](https://www.quantamagazine.org/formal-verification-creates-hacker-proof-code-20160920/) : 
Computer scientists can prove certain programs to be error-free with the same certainty that mathematicians prove theorems. The advances are being used to secure everything from unmanned drones to the internet.

* [CertiKOS enables creation of secure system kernels](http://www.zdnet.com/article/certikos-a-hacker-proof-os/) [[certikos project](http://flint.cs.yale.edu/certikos/)]
Computer system security stinks, because our 
software is buggy and untestable in full. Great for cyber criminals, but not 
for us. So why doesn't someone build a mathematically verified, secure, 
concurrent kernel that can run on x86 and ARM? A team at Yale has.

* [seL4 Is Free – What Does This Mean For You?](https://www.youtube.com/watch?v=lRndE7rSXiI)
* [From L3 to seL4 what have we learnt in 20 years of L4 microkernels?](https://www.youtube.com/watch?v=RdoaFc5-1Rk)
* [seL4 introduction: Capability--based Access Model](https://www.youtube.com/watch?v=x3P6Y6VO0UI) <- Chinese, translation?
* [seL4 playlist](https://www.youtube.com/playlist?list=PL8UO9ZG39Nx43YCAKGCtj9Rb6p2_3utdc)
* [Creating drones that can't be hacked](https://www.youtube.com/watch?v=4oONdV5RYp8)
* [HACMS: Protecting Military Systems from Hackers](https://www.youtube.com/watch?v=OyqNpn6JpBk)

* [Formal Methods for Avionics Software Verification pt1](https://www.youtube.com/watch?v=tRtK4xOK-8o
)

* TODO: find Heartbleed Example with Agda Showing Proofs
