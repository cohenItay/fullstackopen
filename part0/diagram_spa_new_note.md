```mermaid

  sequenceDiagram
    participant browser
    participant server

    browser->>browser : Create the note and render it on screen

    browser->>server: POST exampleapp/new_note_spa<br>application/json
    activate server
    server-->>browser: Response code 201 (Created)
    deactivate server
```
