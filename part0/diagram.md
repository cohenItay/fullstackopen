sequenceDiagram
  participant browser
  participant server
  
  browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note, application/x-www-form-urlencoded, Form Data: note=Sure+thang
  activate server
  server->>browser: Response code 302 (Redirect) to location /exampleapp/notes
  deactivate server
