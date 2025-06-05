![kpt logo](https://github.com/kptdev/kpt/blob/main/logo/KptLogoSmall.png?raw=true)

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

## 👋 Comms 

### Slack

You can reach us in the #kpt channel on the [Kubernetes Slack](https://communityinviter.com/apps/kubernetes/community).

### Mailing list

We have a kpt users [mailing list](https://groups.google.com/forum/?oldui=1#!forum/kpt-users).

## Repository structure

- [kpt](https://github.com/kptdev/kpt): The main logic of kpt.
- [krm-function-catalog](https://github.com/kptdev/krm-functions-catalog): A [catalog](https://catalog.kpt.dev/) of
  off-the-shelf, tested functions. kpt makes configuration easy to create and transform, via reusable functions. Because
  they are expected to be used for in-place transformation, the functions need to be idempotent.
- [krm-function-sdk](https://github.com/kptdev/krm-functions-sdk): Any general-purpose or domain-specific language can
  be used to create functions to transform and/or validate the YAML KRM input/output format, but we provide SDKs to
  simplify the function authoring process in [Go](https://kpt.dev/book/05-developing-functions/02-developing-in-Go).
- [kpt-backstage-plugins](https://github.com/kptdev/kpt-backstage-plugins): We've created a proof-of-concept UI in the
  form of a [Backstage UI plugin](https://github.com/kptdev/kpt-backstage-plugins) to demonstrate the WYSIWYG
  experience that's possible on top of the package orchestrator. More scenarios can be supported by implementing
  form-based editors for additional Kubernetes resource types.
- [governance](https://github.com/kptdev/governance): Governance of the kpt project.
- [.github](https://github.com/kptdev/.github): GitHub organisation level settings (this repo)
