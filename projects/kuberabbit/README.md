# KubeRabbit

- [KubeRabbit](#kuberabbit)
  - [Introduction](#introduction)
  - [Problem](#problem)
  - [Hints](#hints)
  - [Requirements](#requirements)
    - [Functional Requirements:](#functional-requirements)
    - [Non-functional Requirements:](#non-functional-requirements)
  - [Bonus](#bonus)

## Introduction

[RabbitMQ](https://www.rabbitmq.com) is one of the most widely deployed open source message broker.

RabbitMQ is lightweight and easy to deploy on premises and in the cloud. It supports multiple messaging protocols. RabbitMQ can be deployed in distributed and federated configurations to meet high-scale, high-availability requirements.

The community also provides support for their [Kubernetes Operator](https://www.rabbitmq.com/kubernetes/operator/operator-overview.html) to simplify administration and configuration operations on your clusters by taking the advantage of the `Infrastructure As Code`.

## Problem

The [operator](https://github.com/rabbitmq/cluster-operator), currently, misses some capabilities, like the _runtime definition_ of users, vhosts, queues and bindings, which is useful when you don't know upfront the configuration that your broker should manage.

Given all the preconditions of the operator, the scope is to help administrators simplifing the management of the clusters configuration by adding new resources to the domain managed opensource operator, by supporting _at least one_ following resources in the following list:

- Users
  - create/update/delete users
  - manage tags
  - define permissions
- Queues
  - create/update/delete queues
  - support different types of queues
  - support queue parameters
- Exchanges
  - create/update/delete exchages 
  - support exchange parameters
- Bindings
  - bindings creation/deletion/update
- Virtual Hosts
  - create/update/delete virtual hosts
  - support vhost limits

Choose the degree of freedom you prefer, if you want to extend the API of the official operator or create a new operator that connects to an existing instance of RabbitMQ.

## Hints
RabbitMQ exposes Management APIs, but you can also take the advantage of the `rabbitmqctl` by connecting to a remote cluster.

## Requirements

### Functional Requirements:

- Choose **at least one** resource for the one listed above
- For the chosen resources, you should take care of propagating error to the administrator for debugging purposes
- Manage reconciliation and all other phases of the operator lifecycle properly
  
### Non-functional Requirements:

- provide project information via the README.md
  - how to build
  - how to test
  - how to execute
  - how to install
- Use Github as CVS
- show knowledge of using [Operator Framework](https://sdk.operatorframework.io) or similar frameworks (PREFERRED)
  - alternatively, you can propose other solutions to manage this same problem, elaborating the approach and showing a practical example

## Bonus
- full CIntegration (build and package) process for the operator using the tools of your preference (github actions, travis, ...)
- full CDelivery using the tools of your preference (ex. release on github and docker image published to docker.io)
- demonstration on a live Kubernetes cluster (ex. K0s, K3s, microk8s, ...)
- Write down some unit tests to demonstrate familiarity with test frameworks
