## use-case
```mermaid
graph LR
    admin{{admin}} --- cc[create] & crr[recherche] & cr[read] & cu[update] & cd[delete]
    cr & cu & cd --> |include| cs[select categorie]
```
