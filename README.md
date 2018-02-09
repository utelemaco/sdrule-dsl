## Welcome to SDRule-DSL Web Site

#### [About SDRule-DSL](about.md)
#### [Documentation](doc/index.md)
#### [Examples](examples/index.md)
#### Sandbox Environment (Soon)
#### [FAQs](faqs.md)

SDRule-DSL is a language that enables the representation of rules for software development. A simple example is showed bellow:

```
Id: MyFirstRule
Name: A started Project should have at least one Iteration
Description: A started project without an iteration doesn't make sense. May be someone forget to define an interation.
Target: PROJECT
When: $project.isStarted
Then: $project.interations.size > 0
```
