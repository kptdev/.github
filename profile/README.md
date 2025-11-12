![kpt logo](../kpt_stacked_color-100x123.png)

# kpt: Automate Kubernetes Configuration Editing

kpt is a package-centric toolchain that enables a WYSIWYG configuration authoring, automation, and delivery experience,
which simplifies managing Kubernetes platforms and KRM-driven infrastructure (e.g.,
[Config Connector](https://github.com/GoogleCloudPlatform/k8s-config-connector), [Crossplane](https://crossplane.io/))
at scale by manipulating declarative
[Configuration as Data](https://github.com/kptdev/kpt/blob/main/docs/design-docs/06-config-as-data.md).

Configuration as Data is an approach to management of configuration which:

- makes configuration data the source of truth, stored separately from the live state
- uses a uniform, serializable data model to represent configuration
- separates code that acts on the configuration from the data and from packages / bundles of the data
- abstracts configuration file structure and storage from operations that act upon the configuration data; clients
  manipulating configuration data don’t need to directly interact with storage (git, container images).

See the [FAQ](https://kpt.dev/faq/) for more details about how kpt is different from alternatives.

## 📖 Documentation 

Documentaion of the kpt project is in [https://kpt.dev/](https://kpt.dev/).

## ⚖️ Governance

Governance of the kpt project is described in the
[Governance repository](https://github.com/kptdev/governance/blob/main/README.md).

## 🦟 Issues

Issues of all repos are managed under the [issues of the kpt repo](https://github.com/kptdev/kpt/issues). 

## 👋 Comms 

### Slack

You can reach us in the #kpt channel on the [Kubernetes Slack](https://communityinviter.com/apps/kubernetes/community).

### Discussions

Discussion about all the repos in this organisation are in the
[Discussions of the kpt repo](https://github.com/kptdev/kpt/discussions).

### Mailing list

We have a kpt users [mailing list](https://groups.google.com/forum/?oldui=1#!forum/kpt-users).

## Repository structure

- [kpt](https://github.com/kptdev/kpt): The main logic of kpt.
- [governance](https://github.com/kptdev/governance): Governance of the kpt project.
- [.github](https://github.com/kptdev/.github): GitHub organisation level settings (this repo)
