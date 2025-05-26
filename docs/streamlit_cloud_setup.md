# Streamlit Cloud Einrichtungsanleitung

Diese Anleitung beschreibt, wie Sie die CV2Profile/Galdora-Parser-App auf Streamlit Cloud einrichten.

## 1. Secrets einrichten

Damit die App ordnungsgemäß funktioniert, müssen Sie die erforderlichen Geheimnisse in Streamlit Cloud konfigurieren:

1. Gehen Sie zu Ihrer App in Streamlit Cloud
2. Klicken Sie auf den Button "Manage app" in der rechten unteren Ecke
3. Wählen Sie den Tab "Secrets"
4. Fügen Sie den folgenden Inhalt ein (ersetzen Sie den Platzhalter durch Ihren tatsächlichen OpenAI API-Schlüssel):

```toml
# OpenAI API Key
openai_api_key = "IHRE_ECHTE_API_KEY_HIER_EINFÜGEN"

[general]
default_template = "Klassisch"
show_extracted_text = false
```

## 2. Umgebungsvariablen (optional)

Für eine verbesserte Modul-Erkennung können Sie auch diese Umgebungsvariable hinzufügen:

1. Gehen Sie zu "Manage app" > "Settings" > "Advanced settings"
2. Fügen Sie folgende Umgebungsvariable hinzu:
   - Name: `PYTHONPATH`
   - Wert: `.`

## 3. Deployment-Neustart

Nach dem Einrichten der Secrets:

1. Gehen Sie zurück zur Übersicht Ihrer App
2. Klicken Sie auf die drei Punkte (...) oben rechts
3. Wählen Sie "Reboot app"

## 4. Fehlerbehebung

Wenn weiterhin Probleme auftreten:

- Prüfen Sie die Logs unter "Manage app" > "Logs"
- Stellen Sie sicher, dass der API-Schlüssel gültig ist
- Überprüfen Sie, ob alle erforderlichen Pakete in `requirements.txt` enthalten sind 