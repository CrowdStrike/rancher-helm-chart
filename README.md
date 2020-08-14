# Rancher Helm Charts for Falcon
This project provides sample helm charts to deploy CrowdStrike's Falcon Sensor for Linux into Rancher RKE and k3s products.

## Problem
Problem statement (*1-2 sentences*)
* Learn more (link to details below)
* Problems we're not trying to solve (link to ever-growing list)

### Objectives
* What you want to do about the problem, in broad terms. Desired future state.
* What "good" would look like, in 1 - 2 sentences that anyone can understand.
* May not be needed, if captured in problem statement.

### Who May Be Impacted
* Hint: they are usually your stakeholder groups and potential stakeholder groups.

## Timeline

| Phase | Ideation + Research | Prototyping + Testing | Development | Launch |
|:------|:--------------------|:----------------------|:------------|:-------|
| Timing | TBD | TBD | TBD |
| Milestones | TBD | TBD | TBD | TBD | TBD |

* [View detailed timeline and project plan](#) (*link to details, e.g. view-only smartsheet or other document)
* Link key milestones in timeline to relevant documents and details, where people can learn more.

### What's Happening?
* Latest status update goes here
* [Learn more](#) (*link to detailed notes*)

### Make Your Voice Heard
Questions? Ideas? Here's what to do:
* List feedback + collaboration channels; highlight opportunities to provide input (e.g. surveys, join focus group, comment on this page).
* Share feedback loop
* Share decision-making process
* Explain how to stay informed
* [Learn more](#)

## Team

| Executive Sponsor(s) | Project Owner(s) | Stakeholders | Contributors | Questions? |
|:--------------------:|:----------------:|:------------:|:------------:|:-----------|
| Shawn Wells<br/>Vice President, Global Solution Architecture, CrowdStrike<br/>[@shawndwells](https://github.com/shawndwells)<br/><br/>Keith Basil<br/>Vice President, Edge Solutions, Rancher<br/>[@noslzzp](https://github.com/noslzzp) | Chris Kachigian<br/>Sr Director, Technical Integrations & OEMs, CrowdStrike<br/>[@ckachigian](https://github.com/ckachigian) | TBD | TBD | TBD |

## Open Decision Making Targets
Based on our project team's experience and the scope of this project, we are aiming to demonstrate the following [maturity levels](https://github.com/red-hat-people-team/open-decision-framework/tree/master/maturity-model) as we apply the [Open Decision Framework](https://github.com/red-hat-people-team/open-decision-framework):

| Communication | Transparency | Release Early + Release Often | Collaboration |
|:-------------:|:------------:|:-----------------------------:|:-------------:|
| ESTABLISHED | TRANSFORMATIVE | ESTABLISHED | TRANSFORMATIVE |

# What We've Learned So Far
* Short the wording of headlines like these, as your project progresses

## Possible Approaches
* In the early states, list any option or solution under evaluation or consideration.
  * As your project progresses, update heading (e.g. "Approaches we're testing," then "Proposed solution").
* [Learn about other solutions considered](#) (*link*)

## Business Requirements
* TBD

## Constraints
* While Kubernetes Helm charts [follow an open specification](https://helm.sh/docs/topics/chart_template_guide/), Rancher's Helm charts differ slightly in directory structure from upstream Helm repos. To align with Rancher's partner and ISV certification program, this project must use the [Rancher-specific Helm directory structure and specifications](https://github.com/rancher/charts).

* To ensure supportability by [CrowdStrike Customer Service](https://www.crowdstrike.com/contact-support/) of Falcon agent deployments on Rancher RKE or K3, the Helm chart must use [CrowdStrike's supported Ubuntu packages](https://falcon.crowdstrike.com/hosts/sensor-downloads). 

## Assumptions
This is where you'll want to state the obvious (and invite others to question your reasoning). Need help?
* [Requirements vs constraints vs assumptions](https://www.bridging-the-gap.com/ba-stories-its-not-all-requirements-assumptions-and-constraints-matter-too/)
* [Have You Checked Your Assumptions Lately? | Inc.com](https://www.inc.com/robert-kaplan/have-you-challenged-your-assumptions-lately.html)

## Risks
(*Known risks, potential areas of controversy, cultural impacts, unintended impacts*.)

TBD.

## Decision Criteria
* High-level, most important criteria
* Weighted importance

### Scope
* TBD

### Tradeoffs
| Tradeoff | Trigger(s) to Revisit Decision |
|:---------|:-----------------------------|
| While K3s [should run on just about any flavor of Linux](https://rancher.com/docs/k3s/latest/en/installation/installation-requirements/), Rancher limits official support and testing of to Ubuntu 16.04, Ubuntu 18.04, and Raspbian Buster. **To accelerate time to market, this project will initially focus on Ubuntu 18.04 LTS on amd64.** | <ul><li>Rancher formally expanding k3s support to other Linux distributions that CrowdStrike's Falcon agent supports, such as Red Hat Enterprise Linux.<br/><br/></li><li>Customer requests to support expand testing to one of Falcon's supported Linux distributions (ref: [What Linux versions does Falcon agent support?](https://www.crowdstrike.com/endpoint-security-products/crowdstrike-falcon-faq/)).</li></ul>|

## Research

### Feedback Gathered
This project is still initializing. As feedback is received, this section will contain:
* Summarize + link to details
* Changes made based on feedback
* Changes not made, despite feedback (and why)
* Prototype + user testing results
* Post-launch feedback and metrics

### Data and Findings
(*Summarize and link to details*)

## Background

### History + Context
In August 2020, [CrowdStrike](https://www.crowdstrike.com/) and [Rancher](https://rancher.com/) formed a partnership to integrate their respective technologies in support of joint IoT and Edge customers. 

| Rancher | CrowdStrike |
|:--------|:------------|
| Rancher's [k3s](https://k3s.io) provides a certified Kubernetes distribution that is purpose built for resource-constrained, remote locations or inside IoT appliances. | CrowdStrike's Falcon enables and accelerates critical detection, investigation, and threat hunting tasks performed on containers — even on ephemeral containers after they have been decommissioned — while tracking threat events unique to IoT and Edge customers. |

With Rancher and CrowdStrike integrated together, security teams can secure container-based IoT and Edge infrastructure at the speed of DevOps without adding friction.

### About the Problem
[According to Gartner](https://www.gartner.com/smarterwithgartner/what-edge-computing-means-for-infrastructure-and-operations-leaders/), 75 percent of enterprise data will be created and processed outside of data centers and cloud deployments by 2025. This shift of computing to the edge drives a market need to provide an integrated solution that spans cybersecurity detection, response, and forensives to stop breaches and provide extensive visibility into IoT and Edge infrastructure. 

The Rancher and CrowdStrike integration provides an integrated solution that spans across cybersecurity detection, response, and forensics to stop breaches and provide extensive visibility into IoT and Edge infrastructure based off Rancher RKE and k3s technologies.

With this integration, joint customers can achieve the following:

* **Replace existing legacy AV solutions:** Receive protection against malware and malware-free attacks for online/offline endpoints in cloud and on-premise IoT and edge environments;

* **Comprehensive monitoring:** Comprehensive and continuous real-time and historical visibility into Rancher RKE and k3s infrastructure, to identify and prevent threat activities as they happen.

Problems we're ***not*** trying to solve:
* Related problems that you know people will ask you about
* Related things you wish you could solve, but cannot
* Optional, but very helpful to include

Detailed business requirements:
* Requirement #1: Details here to help others understand it
* Requirement #2: Details here to help others understand it
* Order from most to least important. Include info like weighting, relative importance, etc.
* Link to detailed requirement documents, if it's complex.

#### How We Gathered the Requirements
*Explain the process and stakeholders you worked with, external research, etc. Helps validate them.*
* *Link to detailed data, survey results, etc.*

### Other Solutions Considered

Eliminated early on:
* Providing [Kubernetes DaemonSet](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/) to deploy CrowdStrike's Falcon Sensor into Rancher RKE and k3s. During discovery with Rancher, we learned that [Rancher requires Helm charts](https://github.com/rancher/charts).

Eliminated later in the process
* *Name + why*
+ *Name + why*

Good solutions that we didn't move forward with:
* *Name + why (e.g. higher cost, might reconsider in the future, etc.)*