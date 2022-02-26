## use-case
```mermaid
graph LR
    user{{user}} --- n-password[new password]
    n-password --> |include| c-password[confirm password]
    n-password --> |include| answer[answer of selected question if exists]
    answer --> |include| email
    answer --> |include| cin[cin or code-massar]
    answer --> |include| f-name[first-name]
    answer --> |include| l-name[last-name]
    answer --> |include| d-birth[date of birth]
```
