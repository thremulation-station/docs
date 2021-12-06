# Overview
(Image below needs updated)
<br>
<p align="center">
<img src="/images/ts-topology2.png">
</p>
<br>

## The Problem to Solve

Not everyone has a blade server heating their home from a closet... and not everyone has the time or engineering skills that can stitch  complex systems together to create an environment to sharpen their skills. Whether you're just getting started, a junior analyst, or a weathered and pale operator with years hunting experience.


## Use Cases

This project has many practical use cases, and we're excited to see how it's used. A few examples:

- Cyber Defense education
- Generating training data
- Threat intelligence training
- Writing and validating [detection rules](https://github.com/elastic/detection-rules)
- Writing and testing threat [tactics and techniques](https://attack.mitre.org/tactics/enterprise/)


## Workflow

Let's look at an overview of the mini-range and demonstrate a basic exercise workflow.
(Image below needs updated)

<br>
<br>
<p align="center">
<img src="/images/ts-workflow2.png">
</p>

1. Access the `ts.elastic` control box interfaces
1. Choose your target host (currently windows10 or centos)
2. Launch either a prebuilt threat tactic / technique or your own custom
3. Victim machines report back to `ts.elastic` where artificacts can be observed

<br>

---
The next page will cover some basic hardeware and requirements.