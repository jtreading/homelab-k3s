# homelab-k3s

A collection of miscellaneous scripts, commands, etc., used in setting up my homelab k3s cluster.

## Steps Taken So Far

1. **Install Proxmox VE on Supermicro Server**
    - There's a hardware RAID controller configured with one drive in RAID0.
    - Proxmox indicates that this should rule out ZFS, but it still works.

2. **Download Latest Debian ISO and Add to Proxmox**

3. **Create a Virtual Machine Template**
    - Include needed utilities, IP configuration, and k3s (note: it may be better not to include k3s in the template).

4. **Clone the Template**
    - Create one master node and two worker nodes.

5. **Utilize Manifests and Helm**
    - Installed on the master node.
    - Create k3s pods, NodePorts, etc., to enable testing services.

## Resources Used

- [Proxmox VE Installation Guide](https://www.youtube.com/watch?v=X9fSMGkjtug)
- [How to Set Up k3s on a Raspberry Pi 4](https://dev.to/jhqcat/how-to-set-up-k3s-on-a-raspberry-pi-4-4343)
- [Helm Installation Documentation](https://helm.sh/docs/helm/helm_install/)
- [Kubectl Quick Reference](https://kubernetes.io/docs/reference/kubectl/quick-reference/)
