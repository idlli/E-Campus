## use-case
```mermaid
graph LR
    s-admin{{super admin}} --- arr[recherche] & ar[read] & au[update] & ad[delete]
    ar & au & ad --> |include| as[select admin]
```
