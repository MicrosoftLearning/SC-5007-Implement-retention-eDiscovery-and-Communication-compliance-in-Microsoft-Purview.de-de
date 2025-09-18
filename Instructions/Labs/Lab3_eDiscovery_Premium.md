---
lab:
  task: Case investigation with eDiscovery
  exercise: Exercise 3 - Case investigation with eDiscovery
---

## WWL-Mandanten – Nutzungsbedingungen

Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

# Übung 3: Qualifikationsaufgaben

Contoso vermutet, dass vertrauliche Zahlungsdaten, einschließlich Kreditkarten- und Kontonummern, falsch behandelt oder offengelegt wurden. Als ermittelnde Person besteht Ihre Aufgabe darin, Microsoft Purview-eDiscovery zu verwenden, um einen Fall zu erstellen, mehrere Datenquellen zu durchsuchen, vertrauliche Inhalte zu identifizieren und Bearbeitungen anzuwenden, bevor die Ergebnisse für Compliance oder die rechtliche Überprüfung erstellt werden.

Ihre Aufgabe besteht darin, eDiscovery-Fälle zu erstellen und zu verwalten, die den Untersuchungskriterien entsprechen:

- **Erstellen eines neuen eDiscovery-Falls**: Richten Sie einen Fall ein, um die Untersuchung der Zahlungsdaten zu verwalten.
- **Ausführen einer eDiscovery-Suche**: Durchsuchen Sie alle Datenquellen, um Dateien zu identifizieren, die Zahlungskarten- oder Kontoinformationen enthalten können.
- **Hinzufügen von Elementen zu einem Prüfdateisatz**: Setzen Sie Ihre Suchergebnisse auf einen Prüfdateisatz für eine umfassendere Analyse.
- **Kategorisieren von Elementen zur Überprüfung**: Wenden Sie Relevanz- und Bearbeitungstags an, um Dokumente für den Fall zu organisieren.
- **Anwenden von Bearbeitungen**: Verwenden Sie Anmerkungstools, um vertrauliche Details wie Karten- und Kontonummern zu maskieren.
- **Exportieren von Ergebnissen**: Exportieren Sie die bearbeiteten und markierten Elemente zusammen mit einem Elementbericht für die Produktion.

   > **Hinweis**: In diesem Lab wird der Zugriff auf einen M365 E5-Mandanten mit Daten vorausgesetzt, um eine Untersuchung durchzuführen. Sie können diese Übung auch ohne Daten durchführen, aber Sammlungen und Prüfdatensätze werden keine Ergebnisse liefern.

## Aufgabe 1: Erteilen von Berechtigungen für eDiscovery

Zum Exportieren von Dateien benötigen Sie bestimmte Berechtigungen aufgrund des direkten Zugriffs, den diese Option für Benutzerdateien gewährt.

1. Navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an.

1. Wählen Sie **Einstellungen** aus dem linken Navigationsbereich.

1. Erweitern Sie im linken Navigationsbereich **Rollen und Bereiche** und wählen Sie **Rollengruppen**.

1. Wählen Sie auf der Seite **Rollengruppen für Microsoft Purview-Lösungen** die Option **eDiscovery-Manager**.

1. Wählen Sie auf der Fly-out-Seite **eDiscovery-Manager** auf der rechten Seite **Bearbeiten**.

1. Wählen Sie auf der Seite **eDiscovery-Manager verwalten** die Option **Benutzer auswählen**.

1. Wählen Sie auf der Flyout-Seite **Benutzende auswählen** auf der rechten Seite die benutzende Person aus, mit der Sie in den nächsten Schritten die eDiscovery-Untersuchung durchführen wollen, und wählen Sie dann **Auswählen**.

    >**Hinweis**: Stellen Sie sicher, dass Sie die benutzende Person auswählen, die die Daten überprüfen und die Suchergebnisse exportieren soll.

1. Zurück auf der Seite **eDiscovery-Manager verwalten** wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **eDiscovery-Administrator verwalten** die Option **Benutzer auswählen** aus.

1. Wählen Sie auf der Seite **Rollengruppe überprüfen und fertigstellen** die Option **Speichern** aus, um Ihre Benutzenden zur eDiscovery-Manager-Rollengruppe hinzuzufügen.

1. Wenn Sie die Benutzenden erfolgreich hinzugefügt haben, wählen Sie **Fertig** auf der Seite **Sie haben die Rollengruppe erfolgreich aktualisiert**.

Sie haben die eDiscovery-Manager-Berechtigung erfolgreich erteilt.

## Aufgabe 2: Erstellen eines eDiscovery-Falls

Bei dieser Aufgabe erstellen Sie einen neuen eDiscovery-Fall zum Verwalten der Untersuchung der Zahlungsdaten.

1. Wählen Sie in Microsoft Purview **Lösungen** > **eDiscovery**.

1. Wählen Sie auf der Seite **Fälle** die Option **Fall erstellen** aus.

1. Geben Sie im Dialogfeld **Neuer Fall** Folgendes ein:

   - **Fallname**: `Payment Data Leak Investigation`
   - **Fallbeschreibung**: `Investigation into potential exposure of payment card and account data at Contoso.`

1. Klicken Sie auf **Erstellen**.

   Nachdem Ihr Fall erstellt wurde, werden Sie direkt zu Ihrem neuen Fall weitergeleitet.

Sie haben einen neuen eDiscovery-Fall namens _Payment Data Leak Investigation_ erfolgreich erstellt.

## Aufgabe 3: Erstellen einer eDiscovery-Suche

Bei dieser Aufgabe erstellen Sie eine Suche, um E-Mails und Dokumente zu finden, die auf vertrauliche Zahlungsdaten verweisen.

1. Wählen Sie **Erstellen einer Suche** aus.

1. Geben Sie im Dialogfeld **Neue Suche** Folgendes ein:

   - **Namen suchen**: `Payment Data Exposure Search`
   - **Suchbeschreibung**: `Find emails and documents that reference credit cards, debit cards, or account numbers.`

1. Klicken Sie auf **Erstellen**.

1. Wählen Sie auf der Seite **Suche nach der Gefährdung für Zahlungsdaten** die Option **Quellen hinzufügen** aus.

1. **Filtern** Sie Ihre Quellen auf der Seite **Nach Quelle suchen** für **Nur Gruppen**.

1. Wählen Sie **Mandantenweite Quellen hinzufügen** aus, und lassen Sie die Kontrollkästchen für **Alle Personen und Gruppen** und **Alle öffentlichen Ordner** aktiviert.

1. Wählen Sie **Speichern**.

1. Fügen Sie wieder auf der Seite **Suche nach der Gefährdung für Zahlungsdaten** im **Bedingungs-Generator** Bedingungen hinzu:

   - Legen Sie im ersten Feld **Schlüsselwörter gleich** fest, und geben Sie dann `credit card` ein.
   - Geben Sie im zweiten Feld `debit card` ein.
   - Geben Sie im dritten Feld `account number` ein.

   > **Hinweis:** Bedingungen werden als ODER behandelt, wodurch die Suche Elemente zurückgibt, die die Kreditkarten-, Debitkarten- oder Kontonummer enthalten.

1. Wählen Sie **Abfrage ausführen** aus.

1. Wählen Sie auf der Seite **Suchergebnisse auswählen** die Option **Statistik** aus, und aktivieren Sie dann **Bericht für Abfrageschlüsselwörter einschließen**.

1. Wählen Sie **Abfrage ausführen** aus, um die Suche zu starten.

   > **Hinweis:** Dieser Vorgang kann etwa 5 Minuten dauern, um Ergebnisse zu generieren.

1. Wenn die Suche abgeschlossen ist, überprüfen Sie Ihre Ergebnisse auf der Registerkarte **Statistik**. Sehen Sie sich die Elementanzahl, Datenvolume und Schlüsselworttreffer an.

1. Wechseln Sie zur Registerkarte **Beispiel**. Wählen Sie **Beispielergebnisse generieren** aus.

1. Lassen Sie auf der Seite **Beispielansicht generieren** die Standardwerte ausgewählt, und wählen Sie dann **Abfrage ausführen** aus.

   > **Hinweis:** Dieser Vorgang kann etwa 5 Minuten dauern, um Ergebnisse zu generieren.

1. Überprüfen Sie nach Abschluss der Abfrage die Ergebnisse.

Sie haben die Suche erfolgreich ausgeführt und die Ergebnisse mit den Ansichten „Statistik“ und „Beispiel“ überprüft.

## Aufgabe 4: Hinzufügen der Suche zu einem Prüfdateisatz

In dieser Aufgabe committen Sie Ihre Suchergebnisse auf einen Prüfdateisatz, damit diese weiter analysiert werden können.

1. Wählen Sie auf der Seite **Suche nach der Gefährdung für Zahlungsdaten** die Option **Zu Prüfdateisatz hinzufügen** aus.

1. Wählen Sie im Flyout **Zu Prüfdateisatz hinzufügen** die Option **Zu neuem Prüfdateisatz hinzufügen** aus.

   - Geben Sie einen Namen ein: `Payment Data Review Set`.

1. Lassen Sie unter **Elemente auswählen, die eingeschlossen werden sollen** die Option **Indizierten Elemente, die Ihrer Suchabfrage entsprechen** ausgewählt.

1. Wählen Sie unter **Elemente in Listen und Anlagen auswählen** die Option **Anlagen auflisten**, damit angefügte Dateien im Prüfdateisatz enthalten sind.

1. Behalten Sie für alle weiteren Optionen die Standardeinstellungen bei, und wählen Sie dann **Zu Prüfdateisatz hinzufügen** aus.

   > **Hinweis:** Dieser Vorgang kann etwa 5 Minuten dauern, um Ergebnisse zu generieren.

Sie haben den **Zahlungsdatenprüfsatz** erfolgreich erstellt und ihre Suchergebnisse hinzugefügt.

## Aufgaben 5: Überprüfen und Kategorisieren von Elementen

Bei dieser Aufgabe filtern Sie Prüfdateisatzelemente und wenden Tags an, um sie für die Untersuchung zu organisieren.

1. Wählen Sie auf der Seite **Zahlungsdatenprüfsatz** die Option **Abfrage** aus, und konfigurieren Sie Folgendes:

   - Erste Dropdownliste: **Schlüsselwörter**
   - Operator: **Gleich beliebige von**
   - Schlüsselwörter eingeben:

     - `Visa`
     - `Master Card`
   - Wählen Sie **+ Bedingungen hinzufügen** aus.
   - Bedingung hinzufügen:

     - Feld: **Dateiklasse**
     - Operator: **Gleich beliebige von**
     - Wert: `Document`
   - Wählen Sie **Abfrage ausführen** aus.

1. Wählen Sie **Speichern** aus, um diese Suchabfrage zu speichern. Geben Sie im Feld „Filtername“ `Payment data docs` ein.

1. Wählen Sie auf der Befehlsleiste **Tagdateien** aus.

1. Wählen Sie im Flyout **Tagdateien** die Option **Tags erstellen/bearbeiten** aus.

1. Konfigurieren Sie auf der Seite **Tags verwalten** Folgendes:

   - **Taggruppenname**: `Relevance`

     - **Tagname**: `Relevant`
     - Wählen Sie **Tag hinzufügen** aus, und fügen Sie dann `Not relevant` hinzu.
   - Wählen Sie **Taggruppe hinzufügen** aus.
   - **Taggruppenname**: `Review status`
     - **Tagname**: `Needs redaction`

1. Wählen Sie **Speichern** und dann **Schließen** aus.

1. Markieren Sie im Flyout **Tagdateien** das erste Element als **Relevant** und das zweite Element als **Nicht relevant**.

1. Suchen Sie im Prüfdateisatz nach **Contoso Purchasing Permissions - Q1.docx** von **Irvin S** vom **2. August 2019**.

1. Wählen Sie das Element aus, und markieren Sie es als **Benötigt Bearbeitung**.

1. Wählen Sie **Schließen** aus, um das Flyout **Tagdateien** zu schließen.

Sie haben relevante und nicht relevante Dokumente sowie Dokumente erfolgreich markiert, die eine Bearbeitung benötigen.

## Aufgabe 6: Anwenden von Bearbeitungen

Bei dieser Aufgabe maskieren Sie vertrauliche Informationen aus einem Dokument in Ihrem Prüfdateisatz.

1. Wählen Sie im **Zahlungsdatenprüfsatz** das Element **Contoso Purchasing Permissions - Q1.docx** von **Irvin S** am **2. August 2019** aus, um den Dokument-Viewer zu öffnen.

1. Wählen Sie auf der Symbolleiste des Viewers die Option **Kommentieren** aus.

1. Wählen Sie in den Anmerkungstools die Dropdownliste für **Zeichnung** aus, und wählen Sie dann **Bereichsbearbeitung** aus.

    >![Screenshot: Auswählen der Bereichsbearbeitung](./Media/area-redaction.png)

1. Zeichnen Sie mit dem Cursor ein Feld um die vertraulichen Informationen in der Datei, z. B.:

   - Visa-Kartennummer
   - MasterCard-Nummer
   - Bankkontonummer

1. Wiederholen Sie diesen Vorgang nach Bedarf, bis alle vertraulichen Daten abgedeckt sind.

1. Schließen Sie den Dokument-Viewer.

1. Wählen Sie wieder auf der Seite **Zahlungsdatenprüfsatz** mit der ausgewählten Datei **Contoso Purchasing Permissions - Q1.docx** die Option **Aktionen** > **Bearbeitungen an PDF committen** aus.

   > **Hinweis:** Beim Committen von Bearbeitungen wird eine bearbeitete PDF-Datei im Prüfdateisatz gespeichert, während die Originaldatei unverändert bleibt.

Sie haben Bearbeitungen erfolgreich angewendet und an eine bearbeitete PDF-Kopie committet.

## Vorgang 7: Exportieren von Ergebnissen

Bei dieser Aufgabe exportieren Sie die bearbeiteten und markierten Elemente aus Ihrem Prüfdateisatz für die Produktion.

1. Aktivieren Sie im **Zahlungsdatenprüfsatz** die Kontrollkästchen neben den zu exportierenden Elementen.

   > Stellen Sie sicher, dass das durch Sie bearbeitete Dokument **Contoso Purchasing Permissions - Q1.docx** eingeschlossen ist.

1. Wählen Sie auf der Befehlsleiste **Aktionen** > **Exportieren** aus.

1. Konfigurieren Sie im Flyout **Exportieren** Folgendes:

   - **Exportname**: `PaymentData_Export_2025`
   - **Beschreibung:** `Export of review set items with redacted versions for Payment Data Leak Investigation.`

1. Unter **Elemente auswählen, die in den Export eingeschlossen werden sollen**:

   - Wählen Sie **Nur ausgewählten Dokumente** aus.
   - Lassen Sie **Ausgewählte Dokumente erweitern, um Folgendes einzuschließen > Zugeordnete Familienelemente** aktiviert. Dadurch wird sichergestellt, dass Anlagen eingeschlossen sind.

1. Wählen Sie unter **Exporttyp** die Option **Elemente mit Elementbericht exportieren** aus.

   - Aktivieren Sie das Kontrollkästchen **Bearbeitung exportieren**, um die bearbeiteten PDF-Dateien einzuschließen, und das Kontrollkästchen **Tags exportieren**, um Taginformationen einzuschließen.

1. Wählen Sie unter **Exportformat** die Option **MSG-Dateien für Nachrichten erstellen** aus, und lassen Sie alle weiteren Standardwerte ausgewählt.

1. Wählen Sie **Exportieren** aus.

1. Wählen Sie den **Prozess-Manager** aus, um den Status des Exports anzuzeigen.

1. Wählen Sie im Prozess-Manager **Aktualisieren** aus, bis der Exportstatus **Abgeschlossen** lautet.

1. Sobald der Status **Abgeschlossen** lautet, wählen Sie die Zeile für den Export aus.

1. Wählen Sie im Flyout **Exportieren** alle Dateien unter **Pakete exportieren** und dann **Herunterladen** aus.

1. Wählen Sie einen Speicherort aus, um Ihre Exporte herunterzuladen, und navigieren Sie dann zum Speicherort der heruntergeladenen Exporte.

1. Untersuchen Sie die Elemente Ihrer ZIP-Datei.

Sie haben einen Fall erstellt, nach vertraulichen Daten gesucht, einem Prüfdateisatz Elemente hinzugefügt, Tags und Bearbeitungen angewendet und die bearbeiteten Ergebnisse exportiert. Das sind die wichtigsten Schritte bei der Durchführung einer Untersuchung mit Microsoft Purview-eDiscovery.