---
title: Kiali Chart
type: Configuration
---

To configure the Kiali chart, override the default values of its `values.yaml` file. This document describes parameters that you can configure.

>**TIP:** To learn more about how to use overrides in Kyma, see the following documents:
>* [Helm overrides for Kyma installation](/root/kyma/#configuration-helm-overrides-for-kyma-installation)
>* [Top-level charts overrides](/root/kyma/#configuration-helm-overrides-for-kyma-installation-top-level-charts-overrides)

## Configurable parameters

This table lists the configurable parameters, their descriptions, and default values:

| Parameter | Description | Default value |
|-----------|-------------|---------------|
| **server.webRoot** | Defines the context root path for Kiali console, API endpoints, and readiness probes. | `/` |
| **deployment.viewOnlyMode** | When set to `true`, Kiali is available in view-only mode, allowing you to view and retrieve management data for the Service Mesh. You cannot modify the Service Mesh.  | `true` |
| **deployment.accessibleNamespaces** | Specifies the Namespaces Kiali can access to monitor the Service Mesh components deployed there. You can provide the names using regex expressions. The default value is `**`(two asterisks) meaning Kiali can access any Namespace. | `**` |
| **deployment.resources.requests.cpu** | Minimum number of CPUs requested by the Kiali operator to use. | `10m` |
| **deployment.resources.requests.memory** | Minimum amount of memory requested by the Kiali operator to use. | `20Mi` |
| **deployment.resources.limits.cpu** | Maximum number of CPUs available for the Kiali operator to use. | `100m` |
| **deployment.resources.limits.memory** | Maximum amount of memory available for the Kiali operator to use. | `100Mi` |
| **deployment.kubernetes_config.qps** | Defines the allowed queries per second to adjust the API server's throttling rate. | `50` |


For details on Kiali configuration and customization, see the [Kiali CRD](https://github.com/kiali/kiali-operator/blob/master/deploy/kiali/kiali_cr.yaml) and the [values file](https://github.com/kyma-project/kyma/blob/master/resources/kiali/values.yaml).
