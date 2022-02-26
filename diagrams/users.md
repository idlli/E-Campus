## use-case
```mermaid
graph LR
    admin{{admin}} --- uc[create] & urr[recherche] & ur[read] & uu[update] & ud[delete]
    ur & uu & ud --> |include| us[select user]
```
