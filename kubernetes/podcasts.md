# Kube Podcasts

# PODCTL
Brian Gracely & Tyler Britten

Hosted by Red Had Openshift devs. Regular episodes cover news and extra episodes provde a primer on containers and k8s.

## Basics: What is Kubernetes (Aug 21)
- Start here
#### history
- Google creates k8s
    - G has internal container cluster called Borg
    - too coupled to G so they rewrote and contributed k8s to Open Contianer Initiative
    - OCI then contributed it to github
#### Archeticture
- Key-value store (etcd)
- Core scripts (running on controller nodes and worker nodes)
- API (via http/cli)

Typical work flow is user will update values in etcd via the api, the core scripts will then decide if they need to do anything based on the changes

- kublet
    - A program that runs on all worker nodes
    - Periodically checks etcd to see if it needs to do anything
- Pod
    - a unit of work

## Basics: Linux Containers
- Set of technologies to isolate a process
- Mostly involves limiting what a process' can see or do
- Security concerns
    - Process runs as user on the host os 
    - Engine will do what it can to trick the process into thinking it's isolated but theoretically it can do anything that host user can do
- Devices 
    - possible to share a device w/ a container but requires more tooling to manage device names

### How to containerize an application
- docker basics
- 

## Ep 1.
- Can skip this one
- Open Service Broker API
- Lots of Openshift plugging

## Ep 2.
- github.com running on k8s https://githubengineering.com/kubernetes-at-github/
- k8s becomming mainstream fast. Big companies contributing back
##### Learning Kube
- Hard, start from scratch
    - k8s the hard way  https://github.com/kelseyhightower/kubernetes-the-hard-way
    - Hard in prod, have to self-manage cluster
- Easier, use a managed service 
    - Openshift 
    - Google Container Engine (GKE)

## Ep 3. Container Standards
w/ Vincent Batts (Redhat)
- KubeCon - CloudNativeCon Europe, Copenhagen May 2018

## Ep 4.
- installers, lots of options mostly creatied by k8s vendors
- Prometheus, time series key-value store

## Ep 5. Tooling Rundown
- Envoy: high performance proxy (Lyft)
- Istio: Collection of tools (envoy)
- Jaeger: tracing (Uber)
- Zipkin: tracing (Twitter)
- Container Storage Interface
    - Standardized storage for container engines

#### Standards
Standardizing efforts between container engines
- CNCF Cloud Native Computing Foundation
- CSI
- CNI 

## Ep. 6
- Oracle joins CNCF, getting involved in eco system
- Jaegar and Envoy now a part of CNCF
- Heptio, k8s startup
    - ksonnet, config templates
- CoreOS, container focussed linux distribution w/ kubernetes distribution Tectonic 
    
##### k8s setups
- Roll your own
    - Hard 
    - Install k8s, services
    - Lots of expertise needed
    - Have to install and configure services
- k8s distribution
    - Easier, 
    - install distro w/ provided scripts
    - management scripts and GUIs
    - CoreOS/Tectonic, OpenShift
    - Still need some expertise
    - Milage may vary
- Manaaged k8s (KaaS) 
    - Easiest
    - Pre-setup distro
    - Auto updated
    - Just bring your containers
    - Add pre configured services
    - GKE

## Ep. 7
- 