## Welcome to SDRule-DSL Web Site

Thanks for your interest in SDRule-DSL.

Let me introduce the language and our research... The SDRUle-DSL is a small language to represent software development rules and the language is part of a comprehensive research that is pursuing the construction of a platform for **Compliance Checking and Monitoring of Software Projects**.

As experienced developers who have witnessed many approaches for software development process (since Waterfall, RUP, Scrum, XP and other agile methods) we know that developing a software is a very complex mission and any attempt to make rigid processes will not succeed. Instead, we believe that software projects should be flexible and developers must have autonomy to make their own decisions. However, we also believe that a non-intrusive platform to observe what is going on during the process and alert the team of potential non-conformities could be a good idea.

As start point, the SDRule-DSL is tool that enables formal representation of software development rules. Our previous experience with general purpose languages for rule representation (such as OCL, JBoss Drools and SWRL) revealed that to be fully adopted by the industry a language must be, above all, simple. So, our aim is providing a simple, powerful and easy-to-learn DSL for rule representation (that is a tough challenge).

Our approach for software development representation is composed by a metamodel and the DSL.

METAMODEL FIGURE ENTERS HERE....

### Software Development Metamodel and Basic Syntax

The DSL reasons over the concepts presented in the metamodel. A simple example is showed bellow:

```
Id: MyFirstRule
Name: A started Project should have at least one Iteration
Description: A started project without an iteration doesn't make sense. May be someone forget to define an interation.
Target: PROJECT
When: $project.isStarted
Then: $project.interations.size > 0
```

For more details see [SDRule-DSL Wiki](https://github.com/utelemaco/sdrule-dsl/wiki).
