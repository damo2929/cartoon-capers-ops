# Project Summary

This project is designed to support Managed Service Providers (MSPs) and large-scale, multi-tenant private cloud environments by delivering a secure, fully automated infrastructure provisioning framework.

At the foundation of this solution is **NetBox**, serving as the single source of truth and default administrative interface. The private cloud platform is powered by **Proxmox**, which is seamlessly integrated via **Ansible playbooks**, **Ansible rulebooks**, and **webhooks** to deliver comprehensive automation and lifecycle management across the environment.

---

## Primary Objectives

- **Zero-touch automated deployment**  
  Enable full system provisioning without requiring manual user intervention.

- **Tenant isolation and security**  
  Ensure robust and secure separation between tenant environments.

- **Usage-based metrics collection**  
  Capture resource utilization data to support accurate billing and cost allocation.

---

## Deployment Architecture

Operating systems are provisioned from scratch using **Kickstart** and **PXE environments**, eliminating the need to maintain bespoke OS images. This method reduces maintenance overhead and avoids unnecessary customer delays associated with post-clone system updates.

---

## Core Technologies

- [CoreDNS](https://coredns.io/).\
- [CoreDNS netbox plugin](https://github.com/oz123/coredns-netbox-plugin).\
- [Kea DHCP](https://www.isc.org/kea/).\
- [Netbox](https://netboxlabs.com/).\
- [Ansible Core](https://docs.ansible.com/core.html).\
- [Ansible Rulebook](https://ansible.readthedocs.io/projects/rulebook).\
- [netbox ansible modules](https://github.com/netbox-community/ansible_modules).\
- [community.proxmox](https://github.com/ansible-collections/community.proxmox) this is recent folk from community.general.

---

## Enhanced Data Context with NetBox

The framework enhances automation by leveraging NetBox's **Configuration Contexts**, utilizing JSON payloads to supply Ansible with dynamic, context-sensitive data. This approach allows for significantly richer and more targeted automation logic than conventional variable inheritance in Ansible alone.

