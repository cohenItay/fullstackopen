```mermaid

sequenceDiagram
    participant browser
    participant server

    browser->>server: GET exampleapp/spa
    activate server
    server-->>browser: Response code 200
    deactivate server

    browser->>server: GET /exampleapp/notes
    activate server
    server-->>browser: Response code 200 OK
    deactivate server

    par
        browser->>server: GET /exampleapp/main.css
        activate server
        browser->>server: GET /exampleapp/spa.js
        server-->>browser: Response code 200 OK (main.css)
        server-->>browser: Response code 200 OK (spa.js)
        deactivate server
    end

    browser->>server: GET /exampleapp/data.json
    activate server
    server-->>browser: Response code 200 OK
    deactivate server

```
