---
lab:
  task: Configure Communication Compliance
  exercise: Exercise 4 - Configure Communication Compliance
---
## WWL-Mandanten – Nutzungsbedingungen

Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

# Übung 4: Qualifikationsaufgaben

- **Vordefinierte Vorlagenrichtlinie**: Erstellen Sie eine Richtlinie zur Kommunikationscompliance anhand einer vordefinierten Vorlage.
- **Angepasste Vorlagenrichtlinie**: Erstellen Sie eine Richtlinie zur Kommunikationscompliance, indem Sie eine vordefinierte Vorlage ändern.
- **Benutzerdefinierte Kommunikationsrichtlinie**: Erstellen Sie eine Richtlinie zur Kommunikationscompliance, die auf die spezifischen Bedürfnisse Ihres Unternehmens zugeschnitten ist.

## Aufgabe 1: Erstellen einer Richtlinie zur Kommunikationscompliance aus einer Vorlage

In dieser Aufgabe erstellen Sie eine Richtlinie mithilfe einer vordefinierten Vorlage, um allgemeine Complianceszenarien schnell zu beheben.

1. Navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an.
1. Wählen Sie **Alle Lösungen anzeigen** aus.
1. Wählen Sie unter **Risiko & Compliance** die Karte **Kommunikationscompliance**.
1. Wählen Sie im linken Navigationsbereich die Option **Richtlinien** aus.
1. Wählen Sie **Richtlinie erstellen** und sehen Sie sich die verfügbaren Richtlinienvorlagen an:

   - **Copilot-Interaktionen**: Überwacht alle Interaktionen mit Copilot für Microsoft 365.
   - **Unangemessene Inhalte**: Erkennt Hass, Gewalt, sexuelle Inhalte und Selbstbeschädigung in Microsoft Teams.
   - **Unangemessener Text**: Kennzeichnet Bedrohungen, Diskriminierungen und Belästigungen in Exchange Online, Microsoft Teams und Viva Engage.
   - **Unangemessene Bilder**: Identifiziert nicht jugendfreie und rassistische Bilder in Exchange Online und Microsoft Teams.
   - **Sensible Informationen**: Überwacht sensible Informationen in Exchange Online, Microsoft Teams und Viva Engage mit einem geringeren Überprüfungsanteil.
   - **Einhaltung gesetzlicher Vorschriften**: Gewährleistet die Einhaltung von Finanzvorschriften in Exchange Online, Microsoft Teams und Viva Engage.
   - **Interessenkonflikt**: Erkennt potenzielle Interessenkonflikte innerhalb von Exchange Online, Microsoft Teams und Viva Engage.

1. Wählen Sie die Richtlinienvorlage für **Unangemessenen Text erkennen** aus.
1. Auf der Aufklappseite **Kommunikation auf unangemessenen Text erkennen** auf der rechten Seite geben Sie im Feld **Prüfer** den Benutzer bzw. die Benutzerin ein, der bzw. die die Warnungen zur Einhaltung der Kommunikationscompliance prüfen soll.
1. Wählen Sie unten auf der Flyout-Seite **Richtlinie erstellen** und wählen Sie dann **Schließen** auf der Seite **Ihre Richtlinie wurde erstellt**.

Sie haben erfolgreich eine Richtlinie zur Kommunikationscompliance mithilfe der Vorlage **Unangemessenen Text erkennen** erstellt.

## Aufgabe 2: Erstellen einer Richtlinie zur Kommunikationscompliance aus einer angepassten Vorlage

Hier ändern Sie eine Richtlinienvorlage so, dass sie auf bestimmte Organisationsanforderungen zugeschnitten wird.

1. Sie sollten sich immer noch auf der Seite **Richtlinien** innerhalb von **Kommunikationscompliance** im Microsoft Purview Portal befinden.

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal `https://purview.microsoft.com` und melden Sie sich an. Wählen Sie die Karte **Alle Lösungen anzeigen** > **Kommunikationscompliance** unter **Risiko & Compliance**.

1. Wählen Sie **Richtlinie erstellen** > **Unangemessene Bilder erkennen**.
1. Wählen Sie auf der Flyout-Seite **Kommunikation auf unangemessene Bilder erkennen** auf der rechten Seite **Richtlinie anpassen** unten auf der Flyout-Seite.
1. Wählen Sie **Richtlinie anpassen** unten auf der Flyout-Seite.
1. Auf der Seite **Richtlinie benennen und beschreiben** wählen Sie **Weiter**.
1. Geben Sie auf der Seite **Benutzer und Prüfer auswählen** den Benutzer bzw. die Benutzerin, der/die die Warnungen zur Einhaltung der Kommunikationscompliance prüfen soll, in das Feld **Prüfer** ein und wählen Sie dann **Weiter**.
1. Aktivieren Sie auf der Seite **Standorte für die Kommunikationserkennung auswählen** die Standorte für:

   - Exchange:
   - Teams
   - Viva Engage

1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Bedingungen auswählen und Prozentsatz überprüfen** überprüfen Sie die Standardaktionen für die Vorlage für unangemessene Bilder und wählen **Weiter**.
1. Wählen Sie auf der Seite **Überprüfen und fertigstellen** die Option **Richtlinie erstellen** aus und wählen Sie dann auf der Seite **Ihre Richtlinie wurde aktualisiert** die Option **Fertig** aus.

Sie haben erfolgreich eine Richtlinie zur Kommunikationscompliance mithilfe der Vorlage **Unangemessene Bilder erkennen** angepasst.

## Aufgabe 3: Erstellen einer benutzerdefinierten Richtlinie zur Kommunikationscompliance

In dieser Aufgabe erstellen Sie eine Richtlinie zur Kommunikationscompliance von Grund auf neu, um eindeutige Complianceanforderungen zu erfüllen.

1. Sie sollten sich immer noch auf der Seite **Richtlinien** innerhalb von **Kommunikationscompliance** im Microsoft Purview Portal befinden.

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal `https://purview.microsoft.com` und melden Sie sich an. Wählen Sie die Karte **Alle Lösungen anzeigen** > **Kommunikationscompliance** unter **Risiko & Compliance**.

1. Wählen Sie **Richtlinie erstellen** > **Benutzerdefinierte Richtlinie**.
1. Auf der Seite **Richtlinie benennen und beschreiben**, geben Sie Folgendes ein:

   - **Name**: `Global Communication Compliance Policy`
   - **Beschreibung:** `Monitors emails and Teams messages for policy violations.`

1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Benutzer und Prüfer auswählen**:

   - Wählen Sie unter **Benutzer und Gruppen auswählen** die Option **Alle Benutzer**.
   - Lassen Sie das Feld für **Ausgeschlossene Benutzer und Gruppen** leer.
   - Geben Sie im Feld **Prüfer** die Prüfenden ein, die Compliancewarnungen überwachen sollen.

1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Standorte für die Kommunikationserkennung auswählen** aktivieren Sie lediglich Folgendes:

   - Exchange
   - Teams

   Stellen Sie sicher, dass alle anderen Standorte nicht ausgewählt sind.

1. Wählen Sie **Weiter** aus.
1. Lassen Sie auf der Seite **Bedingungen auswählen und Prozentsatz überprüfen** die Standardeinstellungen für **Kommunikationsrichtung** ausgewählt.
1. Aktivieren Sie unter **Bedingungen** die Option zur Verwendung des **neuen Bedingungsgenerators (Vorschau)**.
1. Wählen Sie **+ Bedingung hinzufügen** > **Inhalt entspricht trainierbarem Klassifizierer**.
1. Wählen Sie unter **Inhalt entspricht trainierbaren Klassifizierer** die Option **Hinzufügen** > **Trainierbare Klassifizierer**.
1. Wählen Sie auf der Flyout-Seite **Trainierbare Klassifizierer** auf der rechten Seite Klassifizierer für **Regulatorische Absprachen**, **Aktienmanipulation**, **Unbefugte Offenlegung** und **Unternehmenssabotage**.
1. Wählen Sie **Hinzufügen** unten auf der Aufklappseite **Trainierbare Klassifizierer** auf der rechten Seite.
1. Zurück auf der Seite **Bedingungen und Prozentsatz der Überprüfung auswählen**, stellen Sie den Schieberegler **Prozentsatz der Überprüfung** auf **25 %**.
1. Wählen Sie **Weiter** unten auf der Seite **Bedingungen auswählen und Prozentsatz überprüfen**.
1. Wählen Sie auf der Seite **Überprüfen und fertigstellen** die Option **Richtlinie erstellen** und anschließend auf der Seite **Ihre Richtlinie wurde erstellt** die Option **Fertig** aus.

Sie haben erfolgreich eine benutzerdefinierte Richtlinie zur Kommunikationscompliance mit dem Namen _Globale Richtlinie zur Kommunikationscompliance_ erstellt.
