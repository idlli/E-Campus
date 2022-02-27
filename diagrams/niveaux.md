## use-case
```mermaid
graph LR
    admin{{admin}} --- nxc[create] & nxrr[recherche] & nxr[read] & nxu[update] & nxd[delete]
    nxr & nxu & nxd --> |include| nxs[select niveau]
```
