## use-case
```mermaid
graph LR
    admin{{admin}} --- fc[create] & frr[recherche] & fr[read] & fu[update] & fd[delete]
    fr & fu & fd --> |include| fs[select filière]
```
