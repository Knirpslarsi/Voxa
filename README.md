# Voxa

Voxa zeigt in deinem Stream, wer in deinem Discord-Voice-Channel ist und gerade spricht, mit Profilbild und Namen. Die App läuft lokal auf deinem PC und wird als Browserquelle in OBS eingebunden.

**[Neueste Version herunterladen](https://github.com/Knirpslarsi/Voxa/releases/latest)**

Voraussetzungen: Windows 10 oder 11, der Discord-Desktop-Client und OBS Studio.

## Einrichtung

1. Lade `Voxa-1.2.0.exe` herunter und starte die Datei. Die App ist nicht signiert, deshalb kann Windows warnen. Klicke dann auf **Weitere Informationen** und **Trotzdem ausführen**.
2. Öffne das [Discord Developer Portal](https://discord.com/developers/applications) und lege mit **New Application** eine eigene Application an.
3. Trage unter **OAuth2** bei den Redirects `http://localhost` ein und speichere.
4. Kopiere dort **Client ID** und **Client Secret** in Voxa unter **Start** und klicke auf **Speichern und verbinden**.
5. Bestätige die Anfrage, die im Discord-Client erscheint.
6. Füge in OBS eine **Browser**-Quelle mit der URL `http://localhost:4747/overlay` hinzu, zum Beispiel mit 500 × 800 px.

Tritt jetzt einem Voice-Channel bei, dann erscheint das Overlay automatisch.

Dein Client Secret ist vertraulich. Zeig es nicht im Stream und gib es nicht weiter.

## Gut zu wissen

- **Fenster schließen:** Voxa läuft dann im Tray weiter, damit das Overlay in OBS aktiv bleibt. Beenden kannst du es über das Tray-Symbol.
- **Mit Windows starten:** Das schaltest du unter **Erweitert** ein.
- **Andere im Channel:** Sie müssen nichts einrichten und werden trotzdem angezeigt.
- **Aussehen:** Unter **Vorlagen** findest du fertige Looks, in den anderen Bereichen jede Einstellung einzeln. Änderungen wirken sofort, auch in OBS.
- **Deine Daten:** Einstellungen und Zugangsdaten liegen nur auf deinem PC unter `%APPDATA%\Voxa`.

## Probleme lösen

| Problem | Lösung |
| --- | --- |
| „Warte auf Discord“ | Starte den Discord-Desktop-Client. Die Browser-Version von Discord funktioniert nicht. |
| „Token-Abruf fehlgeschlagen“ | Prüfe das Client Secret und ob `http://localhost` als Redirect eingetragen ist. |
| Overlay in OBS ist leer | Prüfe, ob Voxa läuft und du in einem Voice-Channel bist. Lade die Browserquelle sonst einmal neu. |
| „Port 4747 ist schon belegt“ | Voxa läuft vermutlich schon. Sieh im Tray nach. |

## Hilfe und Kontakt

- [Discord](https://discord.gg/hHunMTsjfT)
- [E-Mail](mailto:support@knirpslarsi.de)

## Lizenz

Voxa ist kein Open-Source-Projekt. Es gelten die Bedingungen in der [LICENSE](LICENSE.txt).

Voxa ist ein unabhängiges Projekt und steht in keiner Verbindung zu Discord Inc. oder OBS Studio.
