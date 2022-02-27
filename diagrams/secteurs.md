## use-case
```mermaid
graph LR
    admin{{admin}} --- sc[create] & srr[recherche] & sr[read] & su[update] & sd[delete]
    sr & su & sd --> |include| ss[select secteur]
```
