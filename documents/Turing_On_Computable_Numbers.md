# On Computable Numbers, with an Application to the Entscheidungsproblem

## High-Level Summary

**Author:** Alan Turing  
**Publication:** Proceedings of the London Mathematical Society, Series 2, Volume 42, Pages 230-265 (1936)  
**Correction:** Volume 43, Pages 544-546 (1937)  
**Type:** Foundational Mathematical Paper  

**📄 Original Document:** [On Computable Numbers, with an Application to the Entscheidungsproblem - Turing Digital Archive](https://turingarchive.kings.cam.ac.uk/publications-lectures-and-talks-amtb/amt-b-12)

**Alternative Sources:**
- [Proceedings of the London Mathematical Society (1936)](https://londmathsoc.onlinelibrary.wiley.com/doi/abs/10.1112/plms/s2-42.2.230)
- [Princeton University Archive](https://catalog.princeton.edu/catalog/4609321)  

## Historical Context

This groundbreaking 1936 paper by Alan Turing laid the theoretical foundation for modern computer science. Written when Turing was just 24 years old, it addressed David Hilbert's Entscheidungsproblem (decision problem) - whether there exists a definite method that could, in principle, be applied to any assertion and determine whether it is true or false.

## Key Contributions

### The Turing Machine
Turing introduced the concept of an abstract computing machine (now called a "Turing machine") consisting of:
- An infinite tape divided into squares
- A read/write head that can move left or right
- A finite set of states
- A table of instructions governing behavior

### Computable Numbers
Turing defined computable numbers as those whose decimal expansions can be calculated by a definite method - essentially what we now call algorithms. He proved that most real numbers are not computable.

### The Halting Problem
Turing demonstrated that there is no general algorithm that can determine whether a given program will halt or run forever - a fundamental limitation of computation known as the halting problem.

### Solution to the Entscheidungsproblem
By showing that the halting problem is undecidable, Turing proved that Hilbert's Entscheidungsproblem has no solution - there is no universal algorithmic method for determining the truth of mathematical statements.

## Impact on Computer Science

This paper established several foundational concepts:

1. **Theoretical Model of Computation**: The Turing machine became the standard model for studying computability
2. **Algorithm Definition**: Formalized what it means for a problem to be algorithmically solvable
3. **Computational Limits**: Identified fundamental limits to what can be computed
4. **Church-Turing Thesis**: Supported the thesis that any function computable by an algorithm is computable by a Turing machine

## Legacy

Turing's work preceded the development of electronic computers by over a decade, yet it remains relevant to modern computer science. The concepts introduced in this paper underpin:
- Programming language theory
- Computational complexity theory
- Artificial intelligence
- Modern computer architecture

## Related Work

This paper was developed independently but simultaneously with Alonzo Church's work on lambda calculus, leading to the Church-Turing thesis that these different approaches to computation are equivalent in power.

## Archival Information

**Original Publication**: Proceedings of the London Mathematical Society, Series 2, Volume 42 (1936)  
**Primary Archive**: Turing Digital Archive, King's College Cambridge  
**Reprints Available In**:
- "The Essential Turing" edited by B. Jack Copeland (2004)
- "The Undecidable" edited by Martin Davis (1965)

## Significance Statement

This paper represents one of the most important theoretical contributions to computer science, establishing the mathematical foundations for the digital age before electronic computers existed. Turing's insights into the nature of computation continue to influence how we understand the possibilities and limitations of algorithmic problem-solving.

## Related Documents in This Collection

### Building on Turing's Foundation
- **[First Draft of a Report on the EDVAC](Von_Neumann_EDVAC_Report.md)** - Von Neumann's stored-program architecture represents the practical implementation of Turing's theoretical universal computing machine, transforming the abstract Turing machine into concrete computer design.

- **[A Mathematical Theory of Communication](Shannon_Mathematical_Theory_Communication.md)** - Shannon's information theory provides the mathematical framework for understanding computation and communication that complements Turing's work on computability, together forming the theoretical foundation of computer science.

### Programming and Algorithms
- **[The Art of Computer Programming](Knuth_Art_of_Computer_Programming.md)** - Knuth's comprehensive treatment of algorithms represents the practical application of Turing's theoretical framework, showing how the concept of algorithmic computation translates into real-world programming.

- **[Go To Statement Considered Harmful](Dijkstra_Go_To_Statement_Considered_Harmful.md)** - Dijkstra's structured programming principles address the practical challenge of creating reliable programs that implement the algorithmic processes Turing proved theoretically possible.

- **[Foundational Programming Languages](Foundational_Programming_Languages.md)** - The development of high-level programming languages represents the evolution from Turing's abstract machine description to human-readable instructions that implement computable functions.

### Applied Computing
- **[A Relational Model of Data](Codd_Relational_Model.md)** - Codd's relational database model demonstrates how Turing's abstract concept of computation applies to practical data processing problems, using mathematical rigor similar to Turing's approach.

### Safety and Reliability
- **[The Therac-25 Investigation](Therac-25_Investigation.md)** - This case study illustrates the importance of understanding the limits of computation that Turing established, showing how failures to recognize computational limitations can have tragic consequences in safety-critical systems.

### Historical Significance
Turing's paper established the theoretical limits and possibilities of computation that all subsequent computer science work builds upon. Every document in this collection either directly implements concepts from Turing's work or represents applications of the computational paradigm he defined. His proof that some problems are fundamentally unsolvable remains relevant to modern discussions of AI, software verification, and the limits of algorithmic solutions.

---

*For the complete original text, consult the Turing Digital Archive at King's College Cambridge or academic reprints in major computer science collections.*