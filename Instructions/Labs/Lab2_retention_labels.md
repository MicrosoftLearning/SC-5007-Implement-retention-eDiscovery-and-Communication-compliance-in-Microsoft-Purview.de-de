---
lab:
  task: Create retention labels
  exercise: Exercise 2 - Create retention labels
---

## WWL-Mandanten – Nutzungsbedingungen

Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

# Übung 2: Qualifikationsaufgaben

Ihre Aufgabe ist es, Aufbewahrungsbezeichnungen zu erstellen und zu verwalten, die die erforderlichen Kriterien erfüllen:

- **Erstellen von Aufbewahrungsbezeichnungen**: Richten Sie Aufbewahrungsbezeichnungen für verschiedene Arten von Dokumenten und E-Mails ein.
- **Veröffentlichen von Aufbewahrungsbezeichnungen**: Stellen Sie die Aufbewahrungsbezeichnungen für die Benutzenden zur Verfügung.
- **Automatisches Anwenden von Aufbewahrungsbezeichnungen:** Konfigurieren Sie Aufbewahrungsbezeichnungen, die basierend auf bestimmten Bedingungen automatisch angewendet werden.

## Aufgabe 1: Erstellen von Aufbewahrungsbezeichnungen

In dieser Aufgabe erstellen Sie Aufbewahrungsbezeichnungen, die Dokumenten und E-Mails zugewiesen werden können.

1. Navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an.
1. Wählen Sie **Lösungen** > **Datensatzverwaltung**.
1. Wählen Sie im linken Navigationsbereich **Ablageplan**.
1. Wählen Sie auf der Seite **Ablageplan** die Option **+ Bezeichnung erstellen**.
1. Auf der Seite **Aufbewahrungsbezeichnung benennen**, geben Sie Folgendes ein:

    - **Name**: `Financial Records`
    - **Beschreibung für Benutzende**: `Assign this label to financial documents to ensure they are retained for the required period.`
    - **Beschreibung für Administratoren**: `Financial records with retention period.`
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Dateiplandeskriptoren für diese Bezeichnung definieren** die Option **Weiter**.
1. Wählen Sie auf der Seite **Bezeichnungseinstellungen festlegen** die Option **Elemente für immer oder für einen bestimmten Zeitraum aufbewahren** und wählen Sie dann **Weiter**.

1. Auf der Seite **Zeitraum festlegen** geben Sie Folgendes ein:

    - **Wie lange ist der Zeitraum?**: 7 Jahre
    - **Wann sollte der Zeitraum beginnen?**: Bei Erstellung der Elemente
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Auswählen, was während des Aufbewahrungszeitraums geschieht** die Option **Elemente aufbewahren, auch wenn sie von den Benutzenden gelöscht werden** und wählen Sie dann **Weiter**.
1. Auf der Seite **Auswählen, was nach dem Aufbewahrungszeitraum geschieht** wählen Sie **Aufbewahrungseinstellungen deaktivieren** und dann **Weiter**.
1. Wählen Sie auf der Seite **Prüfen und beenden** die Option **Bezeichnung erstellen** aus.
1. Wählen Sie auf der Seite **Ihre Aufbewahrungsbezeichnung ist erstellt** die Option **Nichts tun** und dann **Fertig**. Die Bezeichnung wird später in der Übung veröffentlicht.
1. Zurück auf der Seite **Ablageplan** wählen Sie **+ Bezeichnung erstellen** aus, um eine weitere Aufbewahrungsbezeichnung zu erstellen.
1. Geben Sie auf der Seite **Aufbewahrungsbezeichnung benennen** Folgendes ein:

    - **Name**: `HR Records`
    - **Beschreibung für Benutzende**: `This label is auto-applied to HR records with a retention period of five years.`
    - **Beschreibung für Administratoren**: `Auto-applied retention label for HR records.`
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Dateiplandeskriptoren für diese Bezeichnung definieren** die Option **Weiter**.
1. Wählen Sie auf der Seite **Bezeichnungseinstellungen festlegen** die Option **Elemente für immer oder für einen bestimmten Zeitraum aufbewahren** und wählen Sie dann **Weiter**.
1. Auf der Seite **Zeitraum festlegen** geben Sie Folgendes ein:

    - **Wie lange ist der Zeitraum?**: 5 Jahre
    - **Wann sollte der Zeitraum beginnen?**: Bei Erstellung der Elemente
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Auswählen, was während des Aufbewahrungszeitraums geschieht** die Option **Elemente beibehalten, auch wenn sie von den Benutzenden gelöscht werden** und wählen Sie dann **Weiter**.
1. Wählen Sie auf der Seite **Auswählen, was nach dem Aufbewahrungszeitraum geschieht** die Option **Aufbewahrungseinstellungen deaktivieren** und wählen Sie dann **Weiter**.
1. Auf der Seite **Prüfen und fertigstellen** wählen Sie **Bezeichnung erstellen**.
1. Auf der Seite **Ihr Aufbewahrungsbezeichnung ist erstellt** wählen Sie **Nichts tun** und dann **Fertig**.

Sie haben Aufbewahrungsbezeichnungen für Finanzdatensätze mit einem siebenjährigen Aufbewahrungszeitraum und HR-Datensätzen mit einem Aufbewahrungszeitraum von fünf Jahren erfolgreich erstellt.

## Aufgabe 2: Veröffentlichen von Aufbewahrungsbezeichnungen

Im Anschluss an Aufgabe 1 veröffentlichen Sie nun die Aufbewahrungsbezeichnungen, sodass sie für die Benutzenden zur Anwendung auf Dokumente in Exchange-E-Mails und SharePoint-Dokumenten verfügbar sind.

1. Sie sollten immer noch auf der Seite **Ablageplan** im Microsoft Purview-Portal sein.
1. Aktivieren Sie das Häkchen neben der Aufbewahrungsbezeichnung **Finanzdatensätze** und wählen Sie dann die Schaltfläche **Bezeichnungen veröffentlichen** aus.

    >![Screenshot, der zeigt, wo die Aufbewahrungsbezeichnung und die Schaltfläche „Bezeichnungen veröffentlichen“ ausgewählt werden können.](./Media/publish-labels.png)

1. Auf der Seite **Bezeichnungen zur Veröffentlichung auswählen** sollte die Beschriftung **Finanzdatensätze** angezeigt werden.
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Richtlinienbereich** **Weiter** aus.
1. Wählen Sie auf der Seite **Den Typ der zu erstellenden Aufbewahrungsrichtlinie auswählen** die Option **Statisch** und wählen Sie dann **Weiter**.
1. Wählen Sie auf der Seite **Veröffentlichungsort für Bezeichnungen auswählen** die Option **Bestimmte Orte auswählen** und aktivieren Sie sie Folgendes:

   - Exchange-Postfächer
   - Klassische SharePoint- und Kommunikationswebsites
   - OneDrive Konten

1. Stellen Sie sicher, dass „Microsoft 365 Group-Postfächer und -Websites“ auf **Aus** festgelegt ist, und wählen Sie dann **Weiter**.
1. Geben Sie auf der Seite **Benennen Sie Ihre Richtlinie** Folgendes ein:

   - Name: `Financial Records Retention Label`
   - Description (Beschreibung): `Retention label for financial records with a seven-year retention period.`
1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Fertig** wählen Sie **Übermitteln**.
1. Auf der Seite **Ihre Aufbewahrungsbezeichnung wurde veröffentlicht** wählen Sie **Fertig**.

Sie haben die Aufbewahrungsbezeichnung für Finanzdatensätze erfolgreich veröffentlicht.

## Aufgabe 3: Veröffentlichen von automatisch angewendeten Aufbewahrungsbezeichnungen

Nach Aufgabe 1 wenden Sie jetzt die Aufbewahrungsbezeichnung für HR-Datensätze automatisch an, sodass Informationen aufbewahrt werden.

1. Sie sollten sich immer noch in der **Datensatzverwaltung** im Microsoft Purview-Portal befinden.

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an. Wählen Sie **Lösungen** > **Datensatzverwaltung**.

1. Erweitern Sie im linken Navigationsbereich **Richtlinien** und wählen Sie dann **Bezeichnungsrichtlinien**.
1. Wählen Sie **Bezeichnung automatisch zuweisen**, um die Konfiguration der **Richtlinie zur automatischen Bezeichnung erstellen** zu starten.
1. Auf der Seite **Erste Schritte** geben Sie für **Name** und **Beschreibung** die folgenden Informationen ein:

   - **Name**: `HR Records auto-applied`
   - **Beschreibung:** `HR Records auto-applied retention label, with a retention period of five years for all locations.`
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Inhaltstyp auswählen, auf den die Bezeichnung angewendet werden soll** die Option **Bezeichnung auf Inhalt anwenden, der sensible Informationen enthält** und wählen Sie dann **Weiter**.
1. Wählen Sie auf der Seite **Inhalt, der sensible Informationen enthält** die Kategorie **Erweitert** und die Daten-verbesserte Regulierung **U.S. Personenbezogene Informationen (Personally Identifiable Information, PII)**, und wählen Sie dann **Weiter**.

    >![Screenshot, der den Typ der personenbezogenen Daten zeigt, der für eine automatisch zugewiesene Aufbewahrungsbezeichnung ausgewählt wurde.](./Media/sensitive-info-pii.png)

1. Lassen Sie auf der Seite **Inhalte definieren, die vertrauliche Informationen enthalten** die Standardeinstellungen ausgewählt und wählen Sie dann **Weiter** aus.
1. Wählen Sie auf der Seite **Richtlinienbereich** **Weiter** aus.
1. Wählen Sie auf der Seite **Den Typ der zu erstellenden Aufbewahrungsrichtlinie auswählen** die Option **Statisch** und wählen Sie dann **Weiter**.
1. Aktivieren Sie auf der Seite **Standorte für die Anwendung der Richtlinie auswählen** die Optionen für:

   - Exchange-Postfächer
   - Klassische SharePoint- und Kommunikationswebsites
   - OneDrive Konten
   - Microsoft 365-Gruppenpostfächer und -Websites

1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Bezeichnung für automatische Anwendung auswählen** wählen Sie **Bezeichnung hinzufügen**.
1. Aktivieren Sie auf der Flyout-Seite **Bezeichnung auswählen** auf der rechten Seite das Kontrollkästchen neben **HR-Datensätze** und wählen Sie dann **Hinzufügen**.
1. Zurück auf der Seite **Bezeichnung auswählen, die automatisch angewendet werden soll** wählen Sie **Weiter**.
1. Auf der Seite **Entscheiden Sie, ob Sie Ihre Richtlinie testen oder ausführen möchten**, wählen Sie **Richtlinie aktivieren** und dann **Weiter**.
1. Auf der Seite **Überprüfen und beenden** wählen Sie **Absenden**. Wenn die Richtlinie erstellt ist, wählen Sie **Fertig**.

Sie haben erfolgreich eine Aufbewahrungsbezeichnung mit automatischer Anwendung veröffentlicht. In den nächsten sieben Tagen werden alle relevanten Dokumente automatisch mit der veröffentlichten Bezeichnung gekennzeichnet.
