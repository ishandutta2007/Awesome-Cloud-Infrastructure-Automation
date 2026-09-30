# Awesome-Cloud-Infrastructure-Automation

# Top Cloud Infrastructure Automation Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Multi-Cloud Provisioning, Infrastructure-as-Code Orchestration, Policy Enforcement & Cost Optimization*
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Infrastructure Automation**. These tools help platform teams and DevOps engineers provision, configure, and manage infrastructure consistently across public clouds, private data centers, and edge environments—using IaC, GitOps, and policy-as-code.

**Examples** include Morpheus Data, CloudBolt, Scalr, Flexera CMP, Cloudify, Terraform Cloud, env0, Spacelift, Quali Torque, and StormForge (the category leaders).

**Open-source emphasis**: Cloud infrastructure automation has a **mature and production-proven open-source ecosystem**. **Terrakube** provides a complete Terraform/OpenTofu collaboration platform positioned as a Terraform Enterprise replacement . **OpenMCF** delivers 360+ deployment components across 17 cloud providers with unified YAML workflows . **Atlantis** enables self-hosted Terraform PR automation for team collaboration . **OpenSible** unifies OpenTofu provisioning with Ansible configuration in a self-hosted control plane . **k0rdent** brings Kubernetes-native multi-cluster management with built-in FinOps and observability . This section documents these production-grade solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Morpheus Data](https://morpheusdata.com/)**
  Hybrid cloud management platform providing self-service provisioning, orchestration, and cost optimization across on-premises and public cloud environments.

- **[CloudBolt](https://www.cloudbolt.io/)**
  Cloud management platform with automated provisioning, cost optimization, and governance. Provides self-service IT and multi-cloud orchestration capabilities.

- **[Scalr](https://scalr.com/)**
  Terraform automation and collaboration platform. Provides remote operations, policy enforcement, cost estimation, and self-service infrastructure provisioning.

- **[Flexera CMP](https://www.flexera.com/)**
  Hybrid IT and cloud management platform. Provides cost optimization, governance, and automated provisioning across multi-cloud environments.

- **[Cloudify](https://cloudify.co/)**
  Open-source cloud orchestration platform based on TOSCA standard. Provides multi-cloud orchestration, infrastructure automation, and network function virtualization .

- **[Terraform Cloud](https://www.hashicorp.com/products/terraform)**
  HashiCorp's managed Terraform service. Provides remote state management, collaboration, policy enforcement, and private module registry.

- **[env0](https://www.env0.com/)**
  Infrastructure-as-Code automation platform. Provides self-service environments, cost governance, and approval workflows for Terraform and Terragrunt.

- **[Spacelift](https://spacelift.io/)**
  Infrastructure orchestration platform for Terraform, Pulumi, and CloudFormation. Provides policy-as-code, drift detection, and CI/CD integration.

- **[Quali Torque](https://www.quali.com/)**
  Environment-as-a-Service platform. Provides self-service infrastructure provisioning with governance and cost control across multi-cloud.

- **[StormForge](https://www.stormforge.io/)**
  Kubernetes resource optimization platform. Uses machine learning for rightsizing and performance tuning.

## Open-Source GitHub Projects

### Terraform/OpenTofu Automation & Collaboration

- **[Terrakube](https://github.com/terrakube-io/terrakube)**
  **The most complete open-source Terraform/OpenTofu collaboration platform.** **Apache-2.0 licensed**, explicitly positioned as a **Terraform Enterprise, Scalr, and env0 replacement** . **Key features**: Private Terraform module and provider registry ; Organizations and Workspaces for structured infrastructure management; VCS integration with GitHub (Cloud/Enterprise), GitLab (EE/CE), Bitbucket, and Azure DevOps; Remote Terraform/OpenTofu workflow execution (plan, apply, destroy) with variable and state file management; **Custom workflows** with OPA, Infracost, and security scanning via TCL extensions ; Dex-based authentication (Azure AD, Google Cloud Identity, GitHub, GitLab, SAML) with granular permissions ; Remote backend and cloud block support for CLI-driven workflows. Deployment via Helm or Docker Compose . **Terraform BSL License compatible** — confirmed by HashiCorp .

- **[Atlantis](https://github.com/runatlantis/atlantis)**
  **Self-hosted Terraform Pull Request automation for team collaboration.** Go-based application that listens for Terraform PR events via webhooks. Runs `terraform plan`, `import`, and `apply` remotely, then comments back on the pull request with output . **Key benefit**: Makes Terraform changes visible to the whole team, enables non-operations engineers to collaborate on Terraform, and standardizes Terraform workflows. **Apache-2.0** (based on repository context). Simple deployment and integration with existing VCS workflows.

- **[Terramate](https://github.com/terramate-io/terramate)**
  **Open-source tool for managing Terraform and OpenTofu stacks at scale.** Provides **orchestration** for multi-stack deployments with DAG-based scheduling . **Code generation** for Terramate HCL, reducing duplication across environments. **Language Server (LSP)** with Go to Definition, Find References, and Rename Symbol for Terramate/HCL files . Supports **Terraform, OpenTofu, and Terragrunt** execution with configurable arguments. **Vendoring** for Terraform modules. Cloud offering (Terramate Cloud) available for team collaboration. **Open source**.

- **[OpenSible](https://github.com/ossopensible/opensible)**
  **Unified open-source automation platform for cloud provisioning and infrastructure operations.** Combines **infrastructure-as-code and configuration management** into a single self-hosted control plane . **OpenTofu-native** — every stack is rendered as plain OpenTofu code for inspection and local execution. **Ansible integration** for post-provisioning host configuration with playbook execution and inventory management. **Stack blueprints** for Docker, Kubernetes, observability, databases, and CI/CD runners. **OpenSible CI/CD** for multi-stage pipelines combining provisioning, configuration, and approvals. **GitOps-first** with version-controlled stacks and drift tracking. **Secrets and vaults** for encrypted credential management with rotation . **Execution engine** (Go worker) for asynchronous operations with full logs and history. **RBAC** with audit trails. Docker Compose deployment — **no external platform dependency** .

### Multi-Cloud Provisioning Frameworks

- **[OpenMCF](https://github.com/plantonhq/openmcf)**
  **Open-source multi-cloud deployment framework bringing Kubernetes-style consistency to infrastructure.** **Apache-2.0 licensed** . **360+ deployment components across 17 cloud providers** — AWS, GCP, Azure, Kubernetes, OCI, Alibaba Cloud, Hetzner Cloud, DigitalOcean, Cloudflare, Civo, Scaleway, OpenStack, Confluent, Snowflake, Auth0, MongoDB Atlas, and OpenFGA . **Unified structure**: Kubernetes Resource Model (apiVersion/kind/metadata/spec) for all deployments. **Zero abstraction**: Provider-specific configs preserve cloud capabilities while maintaining consistent experience. **Choice of IaC**: Built-in Pulumi and Terraform/OpenTofu modules with feature parity . **Protocol Buffer validation** catches errors in seconds. **Auto-generated SDKs** in Go, Python, TypeScript, and Java. CLI with `openmcf apply`, `pulumi up`, and `tofu apply` commands. **Open source**.

- **[CB-Tumblebug (Cloud-Barista)](https://github.com/cloud-barista/cb-tumblebug)**
  **Multi-cloud infrastructure orchestration and management system.** Provides **VM and network orchestration** across cloud providers with a management server and agents . **Architecture**: CB-Tumblebug API server, CB-Spider (Cloud API controller), MC-Terrarium (multi-cloud enrichment), OpenBao (secrets management for CSP credentials), ETCD (KeyValue DB), PostgreSQL (specs and images storage), CB-MapUI (map-based GUI), and **MCP Server for AI assistant interface** . **Docker Compose deployment** with Traefik reverse proxy. Supports CLI, REST API, and browser interfaces. **Open source**.

### Kubernetes-Native Multi-Cluster Management

- **[k0rdent](https://github.com/k0rdent/k0rdent)**
  **Open-source Kubernetes-native platform for managing distributed infrastructure at massive scale.** **CNCF project** . Provides **multi-cluster management** with a unified control plane. **k0rdent Observability & FinOps (kOF) module** delivers comprehensive observability with **VictoriaMetrics** for time-series metrics and logs, **Grafana** for dashboards, **OpenCost** for Kubernetes cost monitoring and FinOps alignment, and **OpenTelemetry** for structured observability . **NVIDIA GPU monitoring** via DCGM Exporter for AI/ML environments. **GitOps-ready** with ArgoCD and FluxCD compatibility. **100% open-source and community-driven** .

- **[OSM (Open Source MANO)](https://osm.etsi.org/)**
  **ETSI-hosted open-source orchestration platform for managing infrastructure, platforms, and applications across cloud platforms.** Release SIXTEEN introduces **declarative operations** for cloud-native infrastructure management . **Key concepts**: **KSU (Kubernetes Software Unit)** as minimal unit of state to sync; **Profiles** as collections of KSUs; **Cluster Intents** defining profiles to apply to each cluster across 4 synchronization layers . **GitOps-based workflows** with Argo Workflows integration. Manages **cluster add-ons** (Multus, cert-manager, Service Mesh, K-Native, Ingress Controller, Flux, Crossplane) and **workload applications**. Designed for large multi-cloud deployments where "naïve GitOps-like operations can become highly complex" . **Open source**.

### Supporting Tools

- **[Atlantis](https://github.com/runatlantis/atlantis)** — Self-hosted Terraform PR automation .
- **[Terramate](https://github.com/terramate-io/terramate)** — Terraform/OpenTofu stack orchestration and code generation .
- **[OpenMCF](https://github.com/plantonhq/openmcf)** — 360+ deployment components across 17 providers .
- **[OpenSible](https://github.com/ossopensible/opensible)** — OpenTofu + Ansible unified automation .
- **[k0rdent](https://github.com/k0rdent/k0rdent)** — Kubernetes-native multi-cluster with built-in FinOps .

### Additional Strong Open-Source Options

- **Terraform Collaboration**: **Terrakube** (most complete, TFE replacement), **Atlantis** (PR automation) .
- **Stack Orchestration**: **Terramate** (DAG scheduling, LSP) .
- **Multi-Cloud Provisioning**: **OpenMCF** (17 providers, K8s-style), **CB-Tumblebug** (VM/network orchestration, MCP) .
- **Unified Automation**: **OpenSible** (OpenTofu + Ansible, self-hosted) .
- **K8s Multi-Cluster**: **k0rdent** (CNCF, FinOps + observability), **OSM** (ETSI, declarative GitOps) .
- **TOSCA Orchestration**: **Cloudify** (open-source, TOSCA-based multi-cloud) .

**Frameworks for building custom systems**: Combine **Terrakube** for Terraform/OpenTofu collaboration and remote operations, **OpenMCF** for multi-cloud provisioning across 17 providers, **OpenSible** for unified IaC + configuration management, **Terramate** for stack orchestration at scale, and **k0rdent** for Kubernetes-native multi-cluster management with FinOps. Add **Atlantis** for PR-based Terraform workflows and **CB-Tumblebug** for VM/network orchestration with AI assistant integration.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud infrastructure automation platforms handle sensitive infrastructure and credential data; ensure proper access controls, secrets management, and compliance with organizational security policies.
- **Open-source reality**: The open-source ecosystem for cloud infrastructure automation is **mature and production-proven** at the **Terraform/OpenTofu collaboration** (**Terrakube**, **Atlantis**), **multi-cloud provisioning** (**OpenMCF**, **CB-Tumblebug**), and **unified automation** (**OpenSible**) layers . **Terrakube** is explicitly compatible with HashiCorp's Terraform BSL License and positioned as a direct replacement for Terraform Enterprise, Scalr, and env0 . **k0rdent** brings CNCF-backed Kubernetes-native multi-cluster management with built-in FinOps and observability . **OSM** provides ETSI-standard declarative orchestration for large multi-cloud deployments . However, **commercial platforms** (Morpheus, CloudBolt, Scalr, Spacelift) provide **deeper enterprise integrations, managed services, and dedicated support** that open-source alternatives require significant operational investment to match. The open-source path is **genuinely viable** for organizations with strong platform engineering capacity seeking full data sovereignty and zero license fees.

---

**Made for platform engineers, DevOps leads, infrastructure architects, and cloud operations teams.**
Let's make cloud infrastructure automation more open, transparent, and scalable.
