## Unbound Helm Chart
Forked from: https://github.com/ryantiger658/unbound-helm-chart

![release-chart](https://github.com/mjgarner/unbound-helm-chart/actions/workflows/chart-release.yml/badge.svg)

### What is Unbound
[According to Google:](https://www.nlnetlabs.nl/projects/unbound/about/)
> Unbound is a validating, recursive, caching DNS resolver. It is designed to be fast and lean and incorporates modern features based on open standards. Late 2019, Unbound has been rigorously audited, which means that the code base is more resilient than ever.

### How do I use it 
I will be running PiHole in the same cluster to block access to ads sites and other potentially harmful sites. Unbound will operate upstream from PiHole to forward  queries to an upstream resolver such as 1.1.1.1 or Google's 8.8.8.8. The end result will be both faster performance (Unbound caches DNS results and better security (Recurring requests are not forwarded to the upstream DNS services).

### How to Use This Repo and the Chart Repo

Chart Repo URL:  https://mjgarner.github.io/unbound-helm-chart/

Chart Name: unbound

### To Install
```
helm repo add unbound https://mjgarner.github.io/unbound-helm-chart/
helm install unbound/unbound deploymentname
```
### Changes to the original source
I have just built my first k3s cluster and am building a repository of helm charts for my own project. This project is my first published chart and so far the only thing that I changed from the original was the settings for the external port. 
