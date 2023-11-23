
# Monitoring with Prometheus Exporter
Prometheus exporter, consist of ansible playbook for install node exporter, redis exporter, ipmi exporter, ... on defined hosts.

---

## Running

> change hosts ip in inverory.yml file, base on your infrastructure add your ips in defined hosts. 

### Node exporter

The Prometheus Node Exporter exposes a wide variety of hardware- and kernel-related metrics.

```
ansible-playbook playbook/node.yml -i inventory.yml
```

[node-exporter](https://github.com/prometheus/node_exporter)

### IPMI exporter

IPMI (Intelligent Platform Management Interface) is a set of standardized specifications for hardware-based platform management systems that makes it possible to control and monitor servers centrally.
With the help of the ipmi ipmi and freeipmi-tools, can extract the hardware information.

```
ansible-playbook playbook/ipmi.yml -i inventory.yml
```

[ipmi-exporter](https://github.com/prometheus-community/ipmi_exporter)

### Redis exporter
Collect Redis metrics like Redis uptime, commands executed per second, memory utilization, and more. 

```
ansible-playbook playbook/redis.yml -i inventory.yml
```

[redis-exporter](https://github.com/oliver006/redis_exporter)

## What to do

- [ ] ipmi exporter has problem with freeIPMI tools
- [ ] add mongodb exporter
