# Installationsanleitung — Lintua.Cadet

Diese Anleitung richtet sich an Flugschulen, die Lintua.Cadet auf ihren Geräten installieren möchten.

---

## iOS (iPhone / iPad)

Die App wird über Apples TestFlight verteilt.

### Voraussetzungen

- iPhone oder iPad mit iOS 13 oder neuer
- Apple-ID (für TestFlight)

### Installation

1. **TestFlight installieren**: Laden Sie die kostenlose App „TestFlight" aus dem App Store herunter.
2. **Einladungslink öffnen**: Sie erhalten von uns einen Einladungslink per E-Mail. Öffnen Sie diesen auf dem Gerät.
3. **App installieren**: In TestFlight auf „Installieren" tippen. Die App erscheint auf dem Home-Bildschirm.

### Updates

TestFlight benachrichtigt Sie automatisch, wenn eine neue Version verfügbar ist. Öffnen Sie TestFlight und tippen Sie auf „Aktualisieren".

### Hinweis

TestFlight-Builds sind 90 Tage lang gültig. Sie erhalten rechtzeitig eine neue Version.

---

## macOS

Die App wird als signierte und notarisierte ZIP-Datei bereitgestellt.

### Voraussetzungen

- Mac mit macOS 12 (Monterey) oder neuer

### Installation

1. **ZIP herunterladen**: Sie erhalten einen Download-Link per E-Mail.
2. **ZIP entpacken**: Doppelklick auf die heruntergeladene Datei.
3. **App in Programme verschieben**: Ziehen Sie `Lintua.Cadet.app` in den Ordner „Programme".
4. **Erster Start**: Doppelklick auf die App. macOS prüft die Signatur — das kann beim ersten Start einige Sekunden dauern.

### Updates

Sie erhalten per E-Mail einen neuen Download-Link. Ersetzen Sie die bestehende App im Programme-Ordner durch die neue Version. Ihre Daten bleiben erhalten.

---

## Windows

Die App wird als MSIX-Paket bereitgestellt.

### Voraussetzungen

- Windows 10 (Version 1709) oder Windows 11

### Erstinstallation

Beim ersten Mal muss einmalig das Signaturzertifikat installiert werden:

1. **MSIX-Datei herunterladen**: Sie erhalten einen Download-Link per E-Mail.
2. **Zertifikat installieren**:
   - Rechtsklick auf die `.msix`-Datei → **Eigenschaften** → **Digitale Signaturen**
   - Signatur auswählen → **Details** → **Zertifikat anzeigen**
   - **Zertifikat installieren** → **Lokaler Computer** → **Vertrauenswürdige Stammzertifizierungsstellen** → Fertigstellen
3. **App installieren**: Doppelklick auf die `.msix`-Datei → **Installieren**.

Die App erscheint im Startmenü unter „Lintua.Cadet".

### Updates

Laden Sie die neue `.msix`-Datei herunter und installieren Sie sie per Doppelklick. Das Zertifikat muss nur einmal installiert werden. Ihre Daten bleiben erhalten.

---

## Nach der Installation (alle Plattformen)

### Erster Start

1. Melden Sie sich mit den Zugangsdaten an, die Sie von Ihrer Flugschule erhalten haben.
2. Beim ersten Login mit dem Standard-Passwort werden Sie aufgefordert, ein eigenes Passwort zu vergeben.

### Server-Verbindung

Wenn Ihre Flugschule einen Synchronisationsserver nutzt:

- **Automatisch**: Falls DNS-Autodiscovery eingerichtet ist, wird der Server automatisch erkannt. Das Gerät sendet eine Registrierungsanfrage, die vom Administrator genehmigt werden muss.
- **Manuell**: Unter Einstellungen → Synchronisation → „Konfigurieren" können Sie die Server-Adresse und Zugangsdaten eingeben.

### Ohne Server

Die App kann auch ohne Server im Einzelgeräte-Modus betrieben werden. Alle Funktionen sind verfügbar — die Daten werden nur lokal gespeichert.

---

## Hilfe

Bei Fragen zur Bedienung finden Sie eine ausführliche Anleitung direkt in der App unter **Einstellungen → Informationen → Hilfe & Anleitung**.
