## use-case
```mermaid
graph LR
    admin{{admin}} --- gc[create] & grr[recherche] & gr[read] & gu[update] & gd[delete]
    gr & gu & gd --> |include| gs[select group]
```
