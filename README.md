# Rusty-Java

Summary
-------

Transition the Java Runtime from C/C++ to Rust.

Goals
-----

1. Start the work
2. Enhance the source code for the Java Runtime with support for Rust
   1. Add support for Rust Code and the Rust Standard Library
   2. Add support for C/C++ to call Rust
   3. Add support for Rust to call C/C++ (optional)
3. Create a Proof of Concept written in Rust
  1. Implement some small, practical, not-trivial functions in Rust
  2. Make changes to the JVM that are evidence of Rust being called at runtime
4. Start writing the next JSR

Non-Goals
---------

1. Finish the work
2. Consider languages other than Rust
3. Make any user-visible changes
   1. Although it is fair to speculate on what user-visible changes might look like

Success Metrics
---------------

1. Proof Of Concept of Rust code called from C/C++ in the JVM - binary metric
2. More than one automated Unit Test
3. More than one automated Integration Test
4. At least one performance test
5. Improved regression testing

Motivation
----------

Over ten years, Rust has proven itself as a low-level systems programming language capable of
replacing C/C++ with superior code requiring less effort.

1. Linux has begun adding Rust to the kernel, notably drivers.
2. Since October 2023, Microsoft has actively incorporated the Rust programming language
   into various projects to enhance security, performance, and reliability. Rust’s emphasis on
   memory safety and concurrency without sacrificing speed makes it an attractive choice for
   system-level programming. (chat.openai.com version o1-preview)
3. The United States Department of Defence is investigating using Rust to replace C/C++ and other
   languages
   1. As part of this effort, it is also considering using LLM GPT technology to rewrite C/C++
      in Rust
   2. Can this technology be used for this JSR, and would we want to?
   3. Could we get DARPA funding for Rusy Java?


Description
-----------

// REQUIRED -- Describe the enhancement in detail: Both what it is and,
// to the extent understood, how you intend to implement it.  Summarize,
// at a high level, all of the interfaces you expect to modify or extend,
// including Java APIs, command-line switches, library/JVM interfaces,
// and file formats.  Explain how failures in applications using this
// enhancement will be diagnosed, both during development and in
// production.  Describe any open design issues.
//
// This section will evolve over time as the work progresses, ultimately
// becoming the authoritative high-level description of the end result.
// Include hyperlinks to additional documents as required.

1. Start the work
   1.  Feature flags in code so a run-time flag can only enable the feature, such as "--rust"
3. Enhance the source code for the Java Runtime with support for Rust
   1. Add support for Rust Code and the Rust Standard Library
      1. Rust Logging
      2. Rust failure handling
   3. Add support for C/C++ to call Rust
   4. Add support for Rust to call C/C++ (optional)
4. Create a Proof of Concept written in Rust
  1. Implement some small, practical, not-trivial functions in Rust
  2. Make changes to the JVM that are evidence of Rust being called at runtime
4. Start writing the next JSR

Alternatives
------------

No alternatives have been seriously considered, but there might exist languages better than Rust for this.

Testing
-------

Regression testing is paramount to demonstrate that Rust functionality has kept all existing
functionality intact without compromising anything.

Performance testing helps characterize the performance impact of replacing C/C++ with Rust.

High-quality static analysis would help if it exists for Rust code.


Risks and Assumptions
---------------------

A fundamental assumption is that Rust is a better programming language than C/C++ to maintain and improve the
intgrity of the Java Runtime.

A fundamental risk is that this could destabilize the JVM in unexpected ways.
The mitigation is to ensure adequate automated testing.

Serious destabilization results could render this unnecessary.

Dependencies
------------

// Describe all dependencies that this JEP has on other JEPs, JBS issues,
// components, products, or anything else.  Dependencies upon JEPs or JBS
// issues should also be recorded as links in the JEP issue itself.
//
// Describe any JEPs that depend upon this JEP, and likewise make sure
// they are linked to this issue in JBS.

1. Graal?
2. https://jcp.org/en/jsr/detail?id=924
3. 
