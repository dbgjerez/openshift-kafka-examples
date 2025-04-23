# OpenShift Kafka Examples

This repository contains a collection of practical examples for deploying and managing Kafka clusters on OpenShift using Red Hat Streams for Apache Kafka. The examples range from basic Kafka cluster setups to integrations with web consoles and GitOps practices.

## Prerequisites

- **OpenShift**: A running OpenShift cluster.
- **OC CLI**: The OpenShift CLI tool.
- **ArgoCD**: Optional, for implementing GitOps workflows.

## Repository Structure

| Folder                         | Description                                                                 |
|--------------------------------|-----------------------------------------------------------------------------|
| `20-kafka-cluster-zookeeper`  | Example of deploying a Kafka cluster using Zookeeper as the coordinator.   |
| `21-kafka-cluster-kraft`      | Example of deploying a Kafka cluster using KRaft mode (no Zookeeper).      |
| `30-console`                  | Configuration to deploy a Kafka web console for monitoring and management. |
| `gitops`                      | GitOps setup examples using ArgoCD on OpenShift.                           |

## Usage

1. Clone the repository:
  ```bash
    git clone https://github.com/dbgjerez/openshift-kafka-examples.git
    cd openshift-kafka-examples
  ```
2. Apply the ArgoCD bootstrap:
  ```bash
    oc apply -f gitops/project.yaml
    oc apply -f gitops/bootstrap.yaml
  ```
3. Syncronize the proyect you want to discover