## use-case
```mermaid
graph LR
    admin{{admin}} --- tc[create] & trr[recherche] & tr[read] & tu[update] & td[delete]
    tr & tu & td --> |include| ts[select type]
```
