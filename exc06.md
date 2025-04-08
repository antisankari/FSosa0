Tee kaavio tilanteesta, jossa käyttäjä luo uuden muistiinpanon single page ‑versiossa.

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST pyyntö palvelimelle (päivitä lista notella)
    activate server
    server-->>browser: Vastataan päivitys tehdyksi, JSON palautuu (201 Created)
    deactivate server
    
    activate browser
    Note left of browser: ei päivitetä koko sivua
    Note left of browser: suoritetaan palvelimelta saatu JS
    deactivate browser


```