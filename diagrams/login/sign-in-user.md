## use-case
```mermaid
graph LR
    user{{user}} --- sign-in
    email[email or user-name] --> |include| sign-in
    password --> |include| sign-in
    reminder -.-> |extend| sign-in
    user --- f-password[forgot password]
    
    %% links
    click f-password "https://github.com/idlli/laravel-project/blob/main/diagrams/login/reset-password.md" _blank
```
## sequence
```mermaid
sequenceDiagram
    actor user
    participant site as web-site
    participant server as web-server
    alt click on sign-in
        user ->>+ site : onclick(sign_in)
        site ->> site : form validation
        note right of site : email and password
        alt form valid
            site ->> server : open connection
            site ->>+ server : find(user)
            server ->> server : find user
            server -->>- site : respond
            alt user exists
                alt remember me is checked
                    site ->> site : generate(login_string)
                    site ->>+ server : insert(login_string)
                    server ->> server : insert login string
                    server -->>- site : respond
                    site ->> site : cookie(login_string)
                end
                site ->> server : close connection
                site ->> site : redirect(main-page.php)
            else
                site ->> server : close connection
            end
        end
        site -->>- user : message()
    else click on forgot password
        user ->> site : onclick(forgot_password)
        site ->> site : redirect(reset-password.php)
    end
```
