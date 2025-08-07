# The Therac-25 Investigation: Software Safety in Medical Devices

## High-Level Summary

**Authors:** Nancy G. Leveson and Clark S. Turner  
**Publication:** IEEE Computer, July 1993  
**Type:** Investigation Report and Case Study  

**📄 Original Document:** [An Investigation of the Therac-25 Accidents - IEEE Computer, July 1993](https://ieeexplore.ieee.org/document/274940)

**Additional Resources:**
- [Wikipedia: Therac-25](https://en.wikipedia.org/wiki/Therac-25)
- [Stanford PDF Mirror](https://web.stanford.edu/class/cs240/old/sp2014/readings/therac-25.pdf)

This landmark investigation documents the worst series of radiation accidents in the 35-year history of medical accelerators, where software bugs in the Therac-25 linear accelerator led to massive radiation overdoses, deaths, and serious injuries between June 1985 and January 1987.

### The Therac-25 System

The Therac-25 was a medical linear accelerator developed by Atomic Energy of Canada Limited (AECL) for radiation therapy. Unlike its predecessors, the Therac-25 relied heavily on software for safety controls, with minimal hardware safety interlocks. This design philosophy proved catastrophically flawed.

### The Accidents

Six known accidents occurred involving massive overdoses:
- **East Texas Cancer Center (1985-1986)**: Multiple patients received overdoses 100 times the intended dose
- **Yakima Valley Memorial Hospital (1985)**: Patient died from radiation burns
- **Hamilton Clinic, Georgia (1985)**: Patient suffered severe radiation burns
- **Other incidents**: Additional cases documented across different facilities

### Root Causes Identified

The investigation revealed multiple systemic failures:

#### Software Design Flaws
- **Race Conditions**: Timing-dependent bugs that occurred when operators made rapid corrections
- **Poor Error Handling**: Cryptic error messages like "MALFUNCTION 54" provided no useful information
- **Inadequate Testing**: Software was never tested in all possible operating modes
- **Concurrent Programming Errors**: The software had critical timing vulnerabilities

#### Organizational Failures
- **No Independent Code Review**: AECL relied entirely on in-house software development
- **Inadequate Safety Analysis**: Failed to consider software failure modes in hazard analysis
- **Poor Documentation**: Insufficient technical documentation of safety-critical systems
- **Overconfidence in Software**: Assumed software would be inherently more reliable than hardware

#### Regulatory Shortcomings
- **Insufficient Oversight**: FDA approval process didn't adequately evaluate software safety
- **Delayed Response**: Slow recognition and response to emerging accident patterns
- **Industry Standards**: Lack of established standards for medical software safety

### Technical Details

#### The Software Architecture
The Therac-25 used a PDP-11 computer running a custom real-time operating system. The software controlled:
- Beam intensity and energy levels
- Patient positioning systems  
- Safety interlocks and monitoring
- User interface and data entry

#### Critical Bug Examples
- **Data Entry Race Condition**: Rapid operator corrections could cause the system to deliver treatment doses while in electron beam mode instead of X-ray mode
- **Flag Variable Overflow**: A counter overflow could disable safety checking under specific conditions
- **Concurrent Access Problems**: Multiple processes accessing shared variables without proper synchronization

### Impact and Legacy

#### Immediate Consequences
- Multiple patient deaths and severe injuries
- Legal liability for AECL
- Industry-wide examination of medical device software safety
- Enhanced FDA regulations for medical devices

#### Long-term Influence
- **Software Engineering Education**: Became a standard case study in computer science curricula
- **Safety-Critical Systems**: Influenced development of formal methods for safety verification
- **Medical Device Regulation**: Led to more stringent software validation requirements
- **Professional Standards**: Contributed to software engineering codes of ethics and responsibility

### Key Lessons Learned

#### Technical Lessons
1. **Defense in Depth**: Never rely solely on software for safety-critical functions
2. **Formal Verification**: Safety-critical systems require mathematical verification methods  
3. **Comprehensive Testing**: Must test all possible failure modes and edge cases
4. **Clear Error Messages**: User interfaces must provide actionable error information

#### Organizational Lessons
1. **Independent Review**: Safety-critical software requires external audit and verification
2. **Safety Culture**: Organizations must prioritize safety over schedule and cost pressures
3. **Transparent Reporting**: Incident reporting and sharing is essential for industry safety
4. **Continuous Monitoring**: Post-deployment surveillance is crucial for complex systems

#### Regulatory Lessons
1. **Software-Specific Standards**: Traditional hardware safety standards inadequate for software
2. **Process Regulation**: Need to regulate development processes, not just end products
3. **Ongoing Oversight**: Continuous monitoring required throughout product lifecycle
4. **International Coordination**: Global standards needed for medical device safety

### Contemporary Relevance

The Therac-25 case remains highly relevant to modern software development:

- **Autonomous Systems**: Similar issues arise in self-driving cars, drones, and AI systems
- **Medical Devices**: Modern devices face similar software complexity challenges
- **Critical Infrastructure**: Power grids, financial systems, and transportation networks face analogous risks
- **IoT and Connected Devices**: Proliferation of software-controlled devices increases risk surface

### Conclusion

The Therac-25 accidents represent a watershed moment in understanding software's role in safety-critical systems. Leveson and Turner's investigation revealed how seemingly minor software bugs, combined with organizational and regulatory failures, could lead to catastrophic consequences.

The case demonstrates that software safety cannot be achieved through testing alone but requires:
- Rigorous safety analysis during design
- Independent verification and validation
- Robust organizational safety culture
- Appropriate regulatory oversight
- Continuous learning from failures

This investigation established software safety as a distinct engineering discipline and remains essential reading for anyone developing systems where software failure could harm people. The lessons learned continue to influence safety engineering practices across industries, making this one of the most important documents in the history of software engineering.

## Related Documents in This Collection

### Foundational Computing Concepts
- **[On Computable Numbers](Turing_On_Computable_Numbers.md)** - Turing's foundational work established the theoretical limits of computation, relevant to understanding what software can and cannot reliably accomplish in safety-critical systems.

- **[First Draft of a Report on the EDVAC](Von_Neumann_EDVAC_Report.md)** - Von Neumann's stored-program architecture enabled the software-controlled systems like the Therac-25, highlighting how architectural decisions affect safety considerations.

### Programming and Software Engineering  
- **[Go To Statement Considered Harmful](Dijkstra_Go_To_Statement_Considered_Harmful.md)** - Dijkstra's advocacy for structured programming principles directly relates to the Therac-25's software design flaws, including race conditions and concurrent programming errors.

- **[Foundational Programming Languages](Foundational_Programming_Languages.md)** - The evolution of programming languages shows the ongoing challenge of creating reliable software, with the Therac-25 representing failures in real-time systems programming.

- **[The Art of Computer Programming](Knuth_Art_of_Computer_Programming.md)** - Knuth's rigorous approach to algorithm analysis and correctness represents the kind of mathematical verification that was lacking in the Therac-25 development.

### Systems and Architecture
- **[A Mathematical Theory of Communication](Shannon_Mathematical_Theory_Communication.md)** - Shannon's information theory provides the mathematical foundation for understanding how errors propagate through systems, relevant to the Therac-25's error handling failures.

### Connections and Contrasts
This investigation illustrates the critical importance of applying the theoretical foundations and rigorous methodologies documented in the other papers of this collection. The Therac-25 accidents resulted from failures to apply established computer science principles to safety-critical software development, making this document a cautionary tale about the consequences of ignoring fundamental computing concepts in real-world systems.

---

*This case study serves as a permanent reminder that with the power of software comes the responsibility to ensure it operates safely, especially when human lives depend on it.*