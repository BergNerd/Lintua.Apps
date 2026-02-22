# Release Notes — Lintua.Cadet v2.3.3

Alle Änderungen seit Version 1.1.0.

---

## Neu in v2.3.3

### Für alle Nutzer

- **Sortierte Schüler-Übersicht**: Aktive Schüler stehen oben, prüfungsreife in der Mitte, deaktivierte am Ende der Liste.
- **Ruhige Synchronisation**: Die Schüler-Übersicht flackert nicht mehr während der Synchronisation — Daten werden batchweise aktualisiert statt einzeln pro Dokument.
- **Avatar-Farbe korrigiert**: Prüfungsreife Schüler werden nach einer Datenwiederherstellung sofort mit blauem Avatar angezeigt — ein Neustart ist nicht mehr nötig.
- **Ausbildungsnachweis-Export korrigiert**: Die Übungstabelle im PDF-Export wird jetzt vollständig auf mehreren Seiten dargestellt — auch bei Syllabi mit vielen Übungen.
- **Schüler-Unterschrift bei Übungsabschluss**: Beim Abschließen einer Übung wird neben der Fluglehrer-Unterschrift jetzt auch die Schüler-Unterschrift erfasst. Beide Unterschriften erscheinen im PDF-Export und werden über alle Geräte synchronisiert.
- **PDF-Export auf iOS/iPadOS verbessert**: Der PDF-Export öffnet jetzt das iOS Share Sheet statt den Druckdialog — so werden Querformat-PDFs korrekt dargestellt und können direkt gedruckt, gespeichert oder per AirDrop geteilt werden.

### Für Administratoren

- **Schema-Update v18**: Neue Spalte `student_signature` (BLOB) in ExerciseCompletions. Migration füllt bestehende Completions mit einem Platzhalter-Bild.

---

## Neu in v2.3.2

### Für alle Nutzer

- **Schüler-Übersicht überarbeitet**: Die Startseite zeigt auf einen Blick den Status jedes Schülers — Ausbildungsphase (Icon), Medical- und Flugaktivitäts-Ampel (Avatarfarbe) sowie letzter Flug und Übungsfortschritt. Tippen auf den Avatar öffnet eine Detailansicht aller Statuskriterien.
- **Responsive Layout**: Die Schüler-Übersicht passt sich an die Bildschirmbreite an — kompakt auf dem iPhone, zweispaltig auf dem iPad, einzeilig auf dem Desktop.
- **Übungsdetails**: In der Übungsverwaltung können Details zu jeder Übung eingesehen werden, einschließlich Syllabus-Zuordnung.
- **Übungsliste verbessert**: Übungen sind nach Praxis/Theorie gruppiert und zeigen ihre Syllabus-Zuordnung an.
- **Schutz vor Datenverlust**: Beim Verlassen von Bearbeitungs-Screens mit ungespeicherten Änderungen erscheint eine Sicherheitsabfrage.
- **Korrekte Zeitverarbeitung**: Alle Zeitangaben werden einheitlich in UTC verarbeitet und gespeichert.
- **Login-Eingabe**: Die Rechtschreibprüfung korrigiert nicht mehr den Benutzernamen.
- **Signatur-Upload (macOS)**: Das Laden von Signaturbildern über den Dateidialog funktioniert wieder korrekt.
- **Ersteinrichtung**: Übungen werden jetzt vor dem Syllabus eingerichtet — die logische Reihenfolge.
- **Diverse Korrekturen**: Kontextmenü-Texte, Dialog-Texte und Darstellung auf dem iPhone verbessert.

### Für Administratoren

- **Geräte-Fernsteuerung**: Administratoren können über ein Server-Script Geräteaktionen auslösen — vollständige Datenaktualisierung oder Werksreset. Die App prüft bei jeder Synchronisation auf ausstehende Aktionen.
- **Automatische Wiederverbindung**: Bei Authentifizierungsfehlern (401/403/404) versucht die App automatisch, die Zugangsdaten wiederherzustellen — ohne Benutzereingriff.
- **Robustere Synchronisation**: Automatische Wiederholung bei Serverüberlastung (HTTP 429), zuverlässigere Datenwiederherstellung bei großen Datenmengen, korrektes Sync-Verhalten bei allen Datenänderungen.
- **Verbose Sync-Logging**: In den Einstellungen kann ein erweitertes Fehler-Logging aktiviert werden (Sektion „Entwickler", nur für Admins sichtbar). Zeigt CouchDB-Antworten bei Sync-Fehlern — hilfreich zur Fehlerdiagnose.
- **Sicherheit**: Personenbezogene Daten werden in Log-Ausgaben gekürzt oder unterdrückt. Mindestlänge für Passwörter auf 8 Zeichen erhöht.
- **Datenmigration verbessert**: Übungsinhalte aus v1.1 werden bei der Migration nicht mehr ungewollt überschrieben.

---

## Neu in v2.2.0

### Für alle Nutzer

- **In-App Hilfe**: Unter Einstellungen → Informationen → „Hilfe & Anleitung" erklärt eine aufklappbare Kurzanleitung alle Funktionen der App.
- **Datenschutzerklärung**: Unter Einstellungen → Informationen → „Datenschutz" ist die vollständige DSGVO-konforme Datenschutzerklärung einsehbar.
- **Verbesserte leere Zustände**: Alle Listen zeigen hilfreiche Hinweise und Aktionsbuttons, wenn noch keine Daten vorhanden sind.
- **Nachtflüge**: Die Blockzeitberechnung funktioniert jetzt korrekt bei Landungen nach Mitternacht.
- **Kennungseingabe**: Flugzeugkennungen werden beim Speichern automatisch bereinigt (Leerzeichen, Bindestriche).
- **Schülerfreigabe wird synchronisiert**: Schülerfreigaben (Sharing zwischen Fluglehrern) werden nun zwischen allen Geräten synchronisiert.
- **Doppelte Flugnummern behoben**: Bei gleichzeitiger Flugerfassung auf mehreren Geräten werden Flugnummern nach der Synchronisation automatisch chronologisch korrigiert.

### Für Administratoren

- **Einrichtungs-Checkliste**: Nach der ersten Anmeldung zeigt der Startbildschirm eine Checkliste mit den wichtigsten Einrichtungsschritten (Syllabus, Übungen, Kennungen, erster Schüler). Die Checkliste verschwindet, sobald alle Schritte erledigt sind.
- **Pflicht-Passwortwechsel**: Beim ersten Login mit dem Standard-Passwort `admin` wird automatisch zur Passwortänderung aufgefordert.
- **Geräteregistrierung**: Neue Geräte können sich per DNS-Autodiscovery mit dem Server verbinden. Registrierungsanfragen werden serverseitig genehmigt oder abgelehnt.
- **Automatische Fehlerberichte**: Bei Synchronisationsfehlern werden anonymisierte Fehlerberichte an den Server übermittelt (ohne personenbezogene Daten). Im Einzelgeräte-Modus werden Fehler lokal protokolliert.
- **Datenmigration von v1.1**: Bestehende Daten aus Version 1.1.0 werden beim ersten Start automatisch in das neue Format überführt. Die Migration erkennt bestehende Daten auf dem Server und vermeidet Duplikate.

---

## In v2.1.0 eingeführt

### Für alle Nutzer

- **Passwortgeschützter Login**: Die App erfordert eine Anmeldung mit Benutzername und Passwort beim Start.
- **Automatische Anmeldung**: Optional kann die Anmeldung gespeichert werden (verschlüsselt im Systemschlüsselbund). Ein-/Ausschalten über Einstellungen mit Passwortbestätigung.
- **Schülerfreigabe**: Standardbenutzer können ihre Schüler gezielt für andere Benutzer freigeben.
- **Logout**: Abmeldung über die Startseite oder Einstellungen.
- **Synchronisation**: Alle Daten werden automatisch über einen zentralen Server synchronisiert. Die App funktioniert auch vollständig offline — Änderungen werden beim nächsten Verbindungsaufbau synchronisiert.
- **Sync-Status**: In der Kopfzeile zeigt ein Cloud-Symbol den aktuellen Synchronisationsstatus an.
- **Einzelgeräte-Modus**: Die App kann ohne Server betrieben werden — alle Funktionen sind auch ohne Synchronisation verfügbar.
- **Papierkorb**: Gelöschte Schüler, Flüge und andere Einträge werden im Papierkorb aufbewahrt und können wiederhergestellt werden.
- **Praktische Ausbildung**: Checkpoint-Logik und Abhängigkeiten für Übungen. Gesamtstunden und Landungen werden direkt im Tab angezeigt.
- **PDF-Export**: Ausbildungsnachweis und Flugnachweis werden einzeln exportiert. Unterschriften werden direkt eingebettet und automatisch komprimiert.
- **Responsive Design**: Flugeingabe, Flugnachweis und Unterschriften-Dialog passen sich an die Bildschirmbreite an (iPhone, iPad, Desktop). Schülerdetails scrollen mit und geben Platz frei.
- **Werksreset**: Auf dem Anmeldebildschirm kann das Gerät vollständig zurückgesetzt werden.

### Für Administratoren

- **Mehrbenutzerbetrieb**: Zwei Rollen — Administrator (Vollzugriff, sieht alle Schüler) und Standardbenutzer (eigene und freigegebene Schüler).
- **Benutzerverwaltung**: Benutzer anlegen, bearbeiten, deaktivieren, löschen, Passwort zurücksetzen.
- **Fluglehrerstatus**: Benutzer können als Fluglehrer markiert werden, mit optionalem Ablaufdatum. Abgelaufene Fluglehrer werden in Dropdowns automatisch ausgeblendet.
- **Übungsverwaltung**: Übungen und Syllabi anlegen, duplizieren und konfigurieren. Übungen als Flug- oder Bodenübung kategorisierbar.
- **Kennungen**: Flugzeugkennungen können deaktiviert statt gelöscht werden. Sie erscheinen weiterhin in bestehenden Flügen mit dem Zusatz „(inaktiv)".
- **Server-Konfiguration**: Server-Adresse und Zugangsdaten in den Einstellungen konfigurierbar. Bei gleichzeitiger Bearbeitung auf mehreren Geräten gewinnt die zuletzt geänderte Version.
- **Datensicherung**: Datenbank als Datei exportieren/importieren. Daten vollständig vom Server wiederherstellen.
- **Einstellungen**: In Bereiche gegliedert — Anmeldung, Benutzerverwaltung, Ausbildungsinhalte, Synchronisation, Datensicherung, Informationen.

### Plattform-spezifisch

- **Windows**: Die Datenbank wird im AppData-Verzeichnis gespeichert, um Konflikte mit Cloud-Sync-Diensten zu vermeiden.
- **iOS**: Werksreset funktioniert zuverlässig auf iOS-Geräten.
