# Rusty-Java

//
// JDK Enhancement Proposal ("JEP") body template, v2.0
//
// ==> Delete all lines starting with "//"
//     before entering a proposal into JBS
//
// Instances of this template are meant to be evolving documents.  When
// you initially draft a JEP you don't need to fill out every section of
// the template, and in fact at that point you probably won't be able to
// do so.  As you get feedback and build consensus around your proposal
// you'll revise the JEP accordingly.  If your JEP is accepted and targeted
// then you'll continue to revise it as the work progresses so that, once
// it's complete, the JEP can serve as an authoritative record of what
// was actually done.
//
// The body of a JEP uses the Markdown markup language
// (http://daringfireball.net/projects/markdown/basics).
//
// All sections are optional except those marked REQUIRED.  Keep sections
// in the order shown below.  If an optional section is not needed then
// simply omit it rather than write something like "None".  Do not add
// sections beyond those defined in the template.
//
// Use lines of dashes ("----") under section titles, not equals signs
// ("====").  If you need subsections then use the "###" prefix before
// subsection headings and "####" before sub-subsection headings.  Do not
// use HTML markup (`<h2>`, etc.) for section headings.  In general, avoid
// HTML markup unless it's absolutely necessary.

Summary
-------

Transition the Java Runtime from C/C++ to Rust.

Goals
-----

// What are the goals of this proposal?  Omit this section if you have
// nothing to say beyond what's already in the summary.
1. Enhance the source code for the Java Runtime with support for Rust
   1. Add support for Rust Code and the Rust Standard Library
   2. Add support for C/C++ to call Rust
   3. Add support for Rust to call C/C++
2. Create a Proof of Concept written in Rust
  1. Implement some small, useful, not-trivial function

Non-Goals
---------

1. Consider languages other than Rust
2. Make any user-visible changes
   1. Although it is fair to speculate on what user-visible changes might look like

Success Metrics
---------------

// If the success of this work can be gauged by specific numerical
// metrics and associated goals then describe them here.

Motivation
----------

// Why should this work be done?  What are its benefits?  Who's asking
// for it?  How does it compare to the competition, if any?
Rust has proven itself as a low-level systems programming language capable of replacing C/C++
with superior code requiring less effort.

1. Linux has begun adding Rust to the kernel, notably drivers.
2. As of October 2023, Microsoft has been actively incorporating the Rust programming language
   into various projects to enhance security, performance, and reliability. Rust’s emphasis on
   memory safety and concurrency without sacrificing speed makes it an attractive choice for
   system-level programming. (chat.openai.com version o1-preview)
3. The United States Department of Defence is investigating using Rust to replace C/C++ and other
   languages
   1. As part of this effort, it is also considering using LLM GPT technology to rewrite C/C++
      in Rust


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

Alternatives
------------

// Did you consider any alternative approaches or technologies?  If so
// then please describe them here and explain why they were not chosen.

Testing
-------

// What kinds of test development and execution will be required in order
// to validate this enhancement, beyond the usual mandatory unit tests?
// Be sure to list any special platform or hardware requirements.

Risks and Assumptions
---------------------

// Describe any risks or assumptions that must be considered along with
// this proposal.  Could any plausible events derail this work, or even
// render it unnecessary?  If you have mitigation plans for the known
// risks then please describe them.

Dependencies
------------

// Describe all dependencies that this JEP has on other JEPs, JBS issues,
// components, products, or anything else.  Dependencies upon JEPs or JBS
// issues should also be recorded as links in the JEP issue itself.
//
// Describe any JEPs that depend upon this JEP, and likewise make sure
// they are linked to this issue in JBS.
