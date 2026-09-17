# sra-fleet-lab

Lab repository for testing multi-cluster GitOps with Fleet on three Amazon EKS clusters managed from SUSE Rancher for AWS. Used to produce the screenshots and timings in a series of blog posts.

The clusters:

| Fleet cluster | Name | Region | Kubernetes |
|---|---|---|---|
| c-dvnnz | lab3-dev | eu-west-3 | 1.36 |
| c-dxxsm | lab3-staging | eu-north-1 | 1.36 |
| c-kqgtk | lab3-prod | eu-west-3 | 1.35 |

`podinfo/` deploys the podinfo Helm chart to every cluster with different values per cluster, set in `fleet.yaml` under `targetCustomizations`. There is one values block per cluster and no per-cluster values files.

Nothing here is production configuration.
