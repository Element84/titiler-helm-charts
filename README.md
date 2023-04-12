# Titiler Helm Charts

A public Helm repository hosting Titiler helm charts. This repository hosts the Helm charts found in the deployments directory of the [Titiler](https://github.com/developmentseed/titiler) repository. We're currently hosting them in a separate repository because the development repository does not host as a Helm repository and therefore can't easily be pulled into a different project.

The eventual goal is to move this repository under the [developmentseed](https://github.com/developmentseed) organization.

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm is installed you can install Titiler by running the following commands:

```bash
cd charts/titiler
helm install titiler .
```

Visit https://element84.github.io/titiler-helm-charts/ for installation instructions if you prefer to install this service via a Helm repository.

Once installed you can verify Titiler is running by first configuring port forwarding from the Titiler pod:

```bash
kubectl port-forward {TITILER_POD_NAME} 3000:80
```

Then with your browser of choice navigate to `http://localhost:3000`.
