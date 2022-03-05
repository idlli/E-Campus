## use-case
```mermaid
graph LR
    l-admin{{limited admin}} --- profile & settings & notifications & requests & logout
    
    %% links
    
```
## sequence
```mermaid
sequenceDiagram
    actor ladmin as limited admin
    participant site as web-site
    par profile
        ladmin ->> site : onclick(profile)
        site ->> site : redirect(profile.php)
    and settings
        ladmin ->> site : onclick(settings)
        site ->> site : redirect(settings.php)
    and notifications
        ladmin ->> site : onclick(notifications)
        site ->> site : redirect(notifications.php)
    and requests
        ladmin ->> site : onclick(requests)
        site ->> site : redirect(requests.php)
    and logout
        ladmin ->> site : onclick(logout)
        site ->> site : delete_cookie(login_string)
        site ->> site : redirect(sign-in.php)
    end
```
