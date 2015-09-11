# jbehave4-empty-example-scenario

`PerformableTree` is adding `PerformableScenario` instances that do not contain any `ExamplePerformableScenario` instance, causing later a NPE when trying to perform them, since they are handled like a `NormalPerformableScenario`

This regression was introduced by JBEHAVE-1117.

## Run using JBehave 4.0.4

From a terminal, just execute:

`mvn clean test`

Maven Build will fail because of NPE thrown in `PerformableTree:876`

## Run using JBehave 4.0.3

From a terminal, just execute:

`mvn clean test -Pjbehave403`

Maven Build will success
