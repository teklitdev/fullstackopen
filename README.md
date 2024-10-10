sequenceDiagram

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: HTML document
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: CSS file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>browser: JavaScript file
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server.

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: [ {"content": "text", "date": "2024-10-09T20:46:43.287Z"}, {"content": "lkj", "date": "2024-10-09T20:49:22.976Z"}, {"content": "Vlo", "date": "2024-10-09T20:50:29.931Z"}, ... ]
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notes.


