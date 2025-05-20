---
lab:
  task: Configure Retention Policies
  exercise: Exercise 1 - Configure Retention Policies
---

## WWL-Mandanten – Nutzungsbedingungen

Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

# Übung 1: Qualifikationsaufgaben

Ihre Aufgabe ist es, Aufbewahrungsrichtlinien zu erstellen und zu verwalten, die die folgenden erforderlichen Kriterien erfüllen:

- **Unternehmensweite Aufbewahrungsrichtlinie**: Wenden Sie eine Aufbewahrungsfrist an und legen Sie die Standorte für diese Richtlinie fest.
- **Standortbasierte Aufbewahrungsrichtlinien**: Erstellen Sie Aufbewahrungsrichtlinien für bestimmte Standorte, wie z. B. Team-Kanäle und Chats, einschließlich bestimmter Benutzender.
- **PowerShell-Aufbewahrungsrichtlinien**: Implementieren Sie Aufbewahrungsrichtlinien mit PowerShell.
- **Anpassungsfähige Bereichsrichtlinien**: Erstellen und wenden Sie Aufbewahrungsrichtlinien mit anpassungsfähigen Bereichen für Abteilungen wie Recht und Einzelhandel an.

## Aufgabe 1. Erstellen einer unternehmensweiten Aufbewahrungsrichtlinie

Hier erstellen Sie eine Aufbewahrungsrichtlinie, die für die gesamte Organisation gilt.

1. Navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an.
1. Auf dem Bildschirm erscheint eine Meldung über das neue Microsoft Purview-Portal. Wählen Sie die Option, um den Bedingungen für die Veröffentlichung des Datenflusses und der Datenschutzerklärung zuzustimmen, und wählen Sie dann **Erste Schritte** aus.

    >![Screenshot des Bildschirms „Willkommen im neuen Microsoft Purview-Portal“.](./Media/welcome-purview-portal.png)

1. Wählen Sie **Lösungen für** > ** das Datenlebenszyklus-Management**.
1. Erweitern Sie **Richtlinien** und wählen Sie dann **Aufbewahrungsrichtlinien** aus dem linken Navigationsbereich aus.
1. Wählen Sie **+ Neue Aufbewahrungsrichtlinie** aus.
1. Geben Sie auf der Seite **Ihre Mitglieder-Aufbewahrungsrichtlinie benennen** den Namen und die Beschreibung ein:

   - **Name**: `Company wide`
   - **Beschreibung:** `All locations except for teams`

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Richtlinienbereich** **Weiter** aus.
1. Wählen Sie auf der Seite **Den Typ der zu erstellenden Aufbewahrungsrichtlinie auswählen** die Option **Statisch** und wählen Sie dann **Weiter**.
1. Auf der Seite **Auswählen, wo diese Richtlinie angewendet werden soll**, aktivieren Sie:

   - Exchange-Postfächer
   - Klassische SharePoint- und Kommunikationswebsites
   - OneDrive Konten
   - Microsoft 365-Gruppenpostfächer und -Websites

1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Entscheiden Sie, ob Sie Inhalte aufbewahren, löschen oder beides** möchten, geben Sie im Abschnitt **Elemente für einen bestimmten Zeitraum aufbewahren** die folgenden Informationen ein:

   - **Elemente für einen bestimmten Zeitraum aufbewahren**: Wählen Sie **Benutzerdefiniert** aus der Dropdownliste.
   - Ändern Sie das Jahr zu **3**.
   - **Beginnen Sie die Aufbewahrungsfrist basierend auf**: Wann die Elemente zuletzt geändert wurden.
   - **Am Ende des Aufbewahrungszeitraums**: Elemente automatisch löschen.

1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Überprüfen und beenden** wählen Sie **Absenden**.
1. Sobald Ihre Richtlinie erstellt ist, wählen Sie **Fertig**.

Sie haben erfolgreich eine unternehmensweite Aufbewahrungsrichtlinie erstellt, die Elemente drei Jahre ab dem Datum der letzten Änderung aufbewahrt.

## Aufgabe 2 – Erstellen von Speicherort-basierten Aufbewahrungsrichtlinien mit Filter

Hier erstellen Sie Aufbewahrungsrichtlinien speziell für Teams-Kanäle und -Chats, einschließlich Filtern für bestimmte Benutzende.

1. Sie sollten sich immer noch auf dem Bildschirm **Aufbewahrungsrichtlinien** im Microsoft Purview Portal befinden.

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an. Wählen Sie die Karte **Datenlebenszyklusverwaltung** > **Richtlinien** > **Aufbewahrungsrichtlinien**, sobald Sie angemeldet sind.

1. Wählen Sie **+ Neue Aufbewahrungsrichtlinie** aus.
1. Geben Sie auf der Seite **Ihre Mitglieder-Aufbewahrungsrichtlinie benennen** den Namen und die Beschreibung ein:

   - **Name**: `Teams Retention`
   - **Beschreibung:** `Retention for Teams locations`

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Richtlinienbereich** **Weiter** aus.
1. Wählen Sie auf der Seite **Den Typ der zu erstellenden Aufbewahrungsrichtlinie auswählen** die Option **Statisch** und wählen Sie dann **Weiter**.
1. Aktivieren Sie im Abschnitt „Speicherorte auswählen, auf die die Richtlinie angewendet werden soll“ Folgendes:

   - Teams-Kanalnachrichten
   - Teams-Chats und Copilot-Interaktionen

   Stellen Sie sicher, dass alle anderen Optionen deaktiviert sind.

1. Wählen Sie unter **Teams-Chat und Copilot-Interaktionen** den Link **Bearbeiten** unter **Alle Benutzenden** aus und fügen Sie zwei Benutzende hinzu.

    >![Der Screenshot zeigt die Option zum Hinzufügen von Benutzenden für Teams-Chats und Copilot-Interaktionen.](./Media/add-users-retention-policy.png)

1. Wählen Sie auf der Flyout-Seite **Teams-Chats und Copilot-Interaktionen**, sobald die Benutzenden hinzugefügt sind, **Fertig** und dann **Weiter**.
1. **Auf der Seite „Entscheiden, ob Inhalte beibehalten, gelöscht oder beides getan werden soll“** geben Sie Folgendes ein:
   - **Elemente für einen bestimmten Zeitraum aufbewahren**: Wählen Sie **Benutzerdefiniert** aus der Dropdownliste.
   - Ändern Sie das Jahr zu „3“.
   - **Beginnen Sie die Aufbewahrungsfrist auf der Grundlage von**: Wann die Objekte zuletzt geändert wurden.

1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Überprüfen und beenden** wählen Sie **Absenden**.
1. Sobald Ihre Richtlinie erstellt ist, wählen Sie **Fertig**.

Sie haben erfolgreich eine Aufbewahrungsrichtlinie für Teams-Speicherorte mit einem Aufbewahrungszeitraum von drei Jahren erstellt und einen Filter für bestimmte Benutzende angewendet.

## Aufgabe 3: Erstellen einer Aufbewahrungsrichtlinie mithilfe von PowerShell

In dieser Aufgabe verwenden Sie PowerShell zum Erstellen und Verwalten von Aufbewahrungsrichtlinien.

1. Öffnen Sie ein PowerShell-Fenster mit erhöhten Rechten.
1. Geben Sie das folgende Cmdlet ein, um die neueste Version des Exchange Online PowerShell-Moduls zu installieren:

    ```powershell
    Install-Module ExchangeOnlineManagement
    ```

1. Bestätigen Sie den NuGet-Anbieter-Sicherheitsdialog mit **Y** für „Ja“ und drücken Sie die **Eingabetaste**. Dieser Vorgang nimmt einige Zeit in Anspruch.
1. Bestätigen Sie den Sicherheitsdialog „Nicht vertrauenswürdiges Repository" mit **Y** für Ja und drücken Sie die **Eingabetaste**.  Dieser Vorgang nimmt einige Zeit in Anspruch.
1. Geben Sie das folgende Cmdlet ein, um Ihre Ausführungsrichtlinie zu ändern und drücken Sie die **Eingabetaste**. Der Befehl geht davon aus, dass Sie als Benutzerkonto mit entsprechenden Berechtigungen angemeldet sind.

    ```powershell
    Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```

1. Bestätigen Sie die Änderung der Ausführungsrichtlinie mit **Y** für „Ja“ und drücken Sie **Eingabe**.
1. Schließen Sie das PowerShell-Fenster.
1. Öffnen Sie ein reguläres PowerShell-Fenster ohne Rechteerweiterungen, indem Sie mit der rechten Maustaste auf die Windows-Schaltfläche klicken und **Windows PowerShell** auswählen.
1. Stellen Sie eine Verbindung mit dem Security & Compliance Center in Ihrem Mandanten mit dem folgenden Cmdlet her:

    ```powershell
    Connect-IPPSSession
    ```

1. Wenn Sie dazu aufgefordert werden, melden Sie sich mit entsprechenden Berechtigungen als Benutzerkonto an.
1. Führen Sie das folgende Cmdlet aus, um die erste Aufbewahrungsrichtlinie für alle Speicherorte außer Teams zu erstellen:

    ```powershell
    New-RetentionCompliancePolicy -Name "Company Wide PS" -ExchangeLocation All -ModernGroupLocation All -SharePointLocation All -OneDriveLocation All
    ```

1. Führen Sie das folgende Cmdlet aus, um den Aufbewahrungszeitraum mithilfe von Tagen als Einheiten basierend auf dem geänderten Datum festzulegen:

    ```powershell
    New-RetentionComplianceRule -Name "Company Wide PS Rule" -Policy "Company Wide PS" -RetentionDuration 1095 -ExpirationDateOption ModificationAgeInDays -RetentionComplianceAction Keep
    ```

Sie haben Aufbewahrungsrichtlinien erfolgreich über PowerShell mit einem Aufbewahrungszeitraum von drei Jahren erstellt.

<!--- Commenting out until adaptive scope issue is resolved

## Task 4 – Create retention policy with adaptive scope

Here, you will create a retention policy with adaptive scope targeting specific departments like Legal and Retail.

1. In Microsoft Edge, navigate to the Microsoft Purview portal, `https://purview.microsoft.com`, and log in.
1. Select **Settings** from the left navigation bar.
1. Expand **Roles and scopes** then select **Adaptive scopes**.
1. On the **Adaptive scopes** page select **+ Create scope**.
1. On the **Name your adaptive policy scope page**, enter:

   - **Name**: `Legal Documents Retention`
   - **Description**: `Retention for legal related documents`

1. Select **Next**.
1. On the **Assign admin unit page**, select **Next**.
1. On the **What type of scope do you want to create?** page, select **Users** and then **Next**.
1. On the **Create the query to define users** page, under **User attributes**, select:

   - **Attribute**: Department
   - **Operator**: is equal to
   - **Value**: `Legal`

1. Add a second attribute by selecting the **+ Add attribute** button with values:

   - **Query operator**: Or
   - **Attribute**: Department
   - **Operator**: is equal to
   - **Value**: `Retail`

    >![Screenshot showing the query to define users values.](./Media/query-to-define-users.png)

1. Select **Next** and then **Submit** on the **Review and finish** page.
1. Once your scope has been created select **Done** to get back to the **Adaptive scopes** page.
1. Select **Solutions** > **Data Lifecycle Management**.
1. Expand **Policies** then select **Retention policies**.
1. On the **Retention policies** page select **+ New retention policy**.
1. On the **Name your retention policy page**, enter:

   - **Name**: `Legal Data Retention`
   - **Description**: `Retention of all documents within the legal and retail departments.`

1. Select **Next**.
1. On the **Policy Scope** page, select **Next**.
1. On the **Choose the type of retention policy to create** page, select **Adaptive** and then **Next**.
1. On the **Choose adaptive policy scopes and locations** page, select **+ Add scopes** and choose the **Legal Documents Retention** scope.
1. Under **Choose locations to apply the policy** enable:

   - Exchange mailboxes
   - OneDrive accounts

1. Select **Next**.
1. On the **Decide if you want to retain content, delete it, or both** page, enter:

   - **Retain items for a specific period**: 5 years
   - **Start the retention period based on**: When items were created
   - **At the end of the retention period**: Do nothing

1. Select **Next** and then **Submit** on the **Review and finish**.
1. Once your policy is created, select **Done**.

You have successfully applied an adaptive scope to a retention policy.

--->
