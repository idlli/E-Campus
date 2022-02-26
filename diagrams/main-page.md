## use-case
```mermaid
graph LR
    user{{user}} --- documents
    user & admin{{admin}} & l-admin{{limited admin}} & s-admin{{super admin}} --- profile & settings & notifications & requests & logout
    admin --- filières & groups & users & uploads
    s-admin --- admins
    
    %% links
    click settings "/settings.md" _blank
    click notifications "https://github.com/idlli/laravel-project/blob/main/diagrams/notifications.md" _blank
    click requests "https://github.com/idlli/laravel-project/blob/main/diagrams/requests.md" _blank
    click filières "https://github.com/idlli/laravel-project/blob/main/diagrams/filières.md" _blank
    click groups "https://github.com/idlli/laravel-project/blob/main/diagrams/groups.md" _blank
    click users "https://github.com/idlli/laravel-project/blob/main/diagrams/users.md" _blank
    click uploads "https://github.com/idlli/laravel-project/blob/main/diagrams/uploads.md" _blank
    click admins "https://github.com/idlli/laravel-project/blob/main/diagrams/admins.md" _blank
```
