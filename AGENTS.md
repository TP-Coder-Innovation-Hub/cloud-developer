# AGENTS.md

## Context

This repository contains the **Cloud Developer Fundamentals** learning path. The content is provider-agnostic: it teaches cloud computing concepts, architecture patterns, and operational practices that apply across AWS, Azure, and GCP. Learners range from entry-level developers encountering cloud for the first time to senior engineers deepening their understanding of cross-cutting concerns like cost optimization, security, and infrastructure as code.

## Audience

- **Entry-level developers** learning what cloud computing is and how compute, storage, and networking work.
- **Mid-level developers** building and deploying applications to the cloud who need to understand architecture decisions.
- **Senior developers and architects** designing systems, reviewing infrastructure, and establishing operational practices for their teams.

## How to Help

- **Teach patterns, not products.** When explaining a concept, describe the pattern first, then reference services across providers as examples. "Object storage is designed for key-based access to large, unstructured data. AWS calls it S3, Azure calls it Blob Storage, GCP calls it Cloud Storage."
- **Show tradeoffs, not prescriptions.** Every architectural decision involves tradeoffs. Present the options, explain the tradeoffs, and let the learner decide based on their constraints. "VMs give you full OS control but require patching and scaling management. Serverless containers remove operational burden but limit customization."
- **Reference all three major providers.** When naming a service, include AWS, Azure, and GCP equivalents. Use comparison tables when multiple services serve the same purpose.
- **Use Mermaid diagrams.** Architecture concepts benefit from visual representation. Use Mermaid flowcharts, sequence diagrams, and architecture diagrams to illustrate relationships and decision flows.
- **Use progressive depth.** Start with the concept, then add implementation details. Learners naturally sequence from basic to advanced.
- **Ground concepts in real-world scenarios.** Explain not just what something is, but when and why you would use it. "Use a cache when the same query runs dozens of times per second and the underlying data changes infrequently."
- **Encourage Well-Architected thinking.** Every design discussion should touch on reliability, security, performance, cost, and sustainability. These are not afterthoughts.

## How NOT to Help

- **Do not recommend a single provider as the default.** The cloud market is multi-cloud. Learners should understand concepts that transfer across providers. Avoid language like "just use AWS" or "Azure is the best choice."
- **Do not present vendor-specific features as universal patterns.** A feature unique to one provider (e.g., AWS Lambda@Edge, Azure Resource Manager templates) should be clearly labeled as provider-specific, not presented as a general cloud concept.
- **Do not skip the "why" before the "how."** Learners need to understand the problem before seeing the solution. Do not jump to implementation details without establishing the context and motivation.
- **Do not assume deep prior knowledge.** Entry-level learners may not know what a virtual machine is. Mid-level learners may not know what a VPC is. Define terms on first use or link to explanations.
- **Do not conflate price with cost.** A service's hourly rate is its price. The total cost includes engineering time to operate, monitor, and maintain it. Always consider total cost of ownership.
- **Do not present opinions as facts.** "Terraform is the most widely adopted IaC tool" is a factual observation backed by surveys. "Terraform is the best IaC tool" is an opinion. Use the former style.

## Key Concepts

Learners should understand these concepts by the end of this learning path:

1. **Shared Responsibility Model** -- what the cloud provider secures and what you secure
2. **Compute Models** -- VMs, containers, serverless, edge compute, and when each is appropriate
3. **Storage and Database Selection** -- matching access patterns to storage types
4. **Virtual Networking** -- VPCs, subnets, security groups, load balancers, and network topology
5. **IAM and Security** -- least privilege, RBAC, encryption, secrets management, compliance
6. **Infrastructure as Code** -- Terraform, state management, drift detection, modular design
7. **Cost Optimization** -- right-sizing, reserved capacity, FinOps practices, tagging
8. **Well-Architected Framework** -- reliability, security, performance, cost, operational excellence, sustainability

## Cloud Guidelines 2026

These guidelines reflect the current state of cloud computing and inform all content in this repository:

- **Terraform is the default IaC tool.** Pulumi is a strong alternative for teams that prefer general-purpose languages. Provider-specific tools (CloudFormation, Bicep) are valid for single-provider shops but limit portability.
- **Multi-cloud awareness is expected.** Even teams running on a single provider should understand how concepts map across providers. Acquisitions, mergers, and regulatory requirements frequently force multi-cloud scenarios.
- **Serverless containers are the default compute choice for new workloads.** VMs and managed Kubernetes remain important but are no longer the first choice for most applications.
- **Cost-aware architecture is a core skill.** FinOps practices, tagging discipline, and cost estimation during design reviews are standard expectations, not optional extras.
- **Security is built in, not bolted on.** Encryption by default, least-privilege IAM, secrets management, and regular security reviews are baseline practices.
- **Well-Architected Reviews are routine.** Teams conduct them annually for every production workload. Findings are tracked as engineering work, not compliance checkboxes.
- **Sustainability is a first-class pillar.** Efficient resource utilization reduces both cost and environmental impact. Serverless and managed services contribute to sustainability goals.
- **AI services are part of the standard toolkit.** Managed AI/ML services for vision, language, and generative AI are integrated into application architectures alongside traditional services.

## Repository Structure

```
cloud-developer/
  README.md          -- Cloud Developer Fundamentals (this guide)
  AGENTS.md          -- Agent instructions and context (this file)
```

As the learning path grows, additional modules may be added:

```
cloud-developer/
  README.md
  AGENTS.md
  modules/
    01-compute/
    02-storage/
    03-networking/
    04-security/
    05-iac/
    06-cost-optimization/
    07-observability/
    08-event-driven/
    09-ai-services/
```
