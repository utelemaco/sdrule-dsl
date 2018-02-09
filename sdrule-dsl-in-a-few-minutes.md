## SDRule-DSL in a few minutes

The solution for software representation is composed by a *metamodel* and a *dsl*. The metamodel contains concepts necessary to mapping a software development environment and was inspired in agile methods. Thus, concepts such as _Iteration_ and _Case_ appear as main concepts. To learn more about the metamodel see the [metamodel section](doc/metamodel.md).

Regarding the dsl, it has the following structure: 

```
{
  id:
  name:
  description:
  target:
  when:
  then:
```

The _id_, _name_ and _description_ are self-explanatory. 

The _target_ element can assume the values: Project, Iteration, Case, Task, Delivery and Delivery Interval. It indicates the target of the rule. You can reach more details of target element in the section [Target Element](doc/target-element.md).

The _when_ and _then_ elements are used to control the evaluation of the rule. The first (_when_) is a trigger that indicates whether the rule should be evaluated. The second (_then_) indicates if the rule is compliant or non-compliant.

You should use SDRule-DSL-Expression in the elements _when_ and _then_. Those expression offers many features to make coding rules easier. Among the features there are:
1. Simple mechanism for collection filtering
1. Mechanism for selecting elements from collection based on maximum and minimum values
1. Mechanism for grouping collections 
1. Basic logical and math operators

Let's see some examples:
```
{
  id: my-fisrt-rule
  name: My first rule
  description: The first rule states that a Project should have at least 1 Iteration
  target: Project
  when: ALWAYS
  then: $project.iterations.size() > 0
```

Note that _my-first-rule_ uses a constant *ALWAYS* and a expression *$project.iterations.size() > 0*


```
{
  id:
  name:
  description:
  target:
  when:
  then:
```

```
{
  id:
  name:
  description:
  target:
  when:
  then:
```
