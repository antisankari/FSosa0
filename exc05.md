0.5: Single Page App
Tee kaavio tilanteesta, jossa käyttäjä menee selaimella osoitteeseen https://studies.cs.helsinki.fi/exampleapp/spa eli muistiinpanojen Single Page App-versioon

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note left of browser: klikataan linkkiä tmv.
    browser->>server: GET pyyntö palvelimelle (pyydetään sisältöä)
    activate server
    server-->>browser: Vastataan sisällöllä (JSON, HTML & JS)
    deactivate server
    
    activate browser
    Note left of browser: koostetaan HTML
    Note left of browser: suoritetaan ladattu JS, täytetään JSON tiedoilla
    deactivate browser


```