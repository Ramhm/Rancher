# Rancher
## How to Install Rancher on a Single Node

[![Build Status](https://drone-publish.rancher.io/api/badges/rancher/rancher/status.svg?branch=master)](https://drone-publish.rancher.io/rancher/rancher)
[![Docker Pulls](https://img.shields.io/docker/pulls/rancher/rancher.svg)](https://store.docker.com/community/images/rancher/rancher)
[![Go Report Card](https://goreportcard.com/badge/github.com/rancher/rancher)](https://goreportcard.com/report/github.com/rancher/rancher)

Rancher is an open source project that provides a container management platform built for organizations that deploy containers in production. Rancher makes it easy to run Kubernetes everywhere, meet IT requirements, and empower DevOps teams.


### Minimum Requirements

* Operating Systems
  * Ubuntu 16.04 (64-bit)
  * Red Hat Enterprise Linux 7.5 (64-bit)
  * RancherOS 1.4 (64-bit)
* Hardware
  * 4 GB of Memory
* Software
  * Docker v1.12.6, 1.13.1, 17.03.2

<br/>

## Quick Start

    sudo docker run -d --restart=unless-stopped -p 80:80 -p 443:443 rancher/rancher

Open your browser to https://localhost

<br/>

## Docker Compose

Image:
```bash
rancher/rancher:latest
```
Ports:
```bash
- '80:80'
- '443:443'
```
Volumes:
```bash
- './ssl/fullchain.pem:/etc/rancher/ssl/cert.pem'
- './ssl/privkey.pem:/etc/rancher/ssl/key.pem'
- './data:/var/lib/rancher'
```
Command:
```bash
--no-cacerts
```




<br/><br/>

### Reference:

[Single Node Install](https://rancher.com/docs/rancher/v2.x/en/installation/single-node/)

[Rancher Github](https://github.com/rancher/rancher/blob/master/README.md)
