---
lab:
  task: Case investigation with eDiscovery (Premium)
  exercise: Exercise 3 - Case investigation with eDiscovery (Premium)
---

## WWL-Mandanten – Nutzungsbedingungen

Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

# Übung 3: Qualifikationsaufgaben

Ihre Aufgabe besteht darin, eDiscovery-Fälle zu erstellen und zu verwalten, die den Untersuchungskriterien entsprechen:

- **Erstellen eines neuen eDiscovery-Falls**: Richten Sie einen neuen Fall ein, um mit Ihrer Untersuchung zu beginnen.
- **Hinzufügen von Verwahrenden zum Fall**: Nehmen Sie relevante Personen auf, die möglicherweise über sachdienliche Daten verfügen.
- **Erstellen und Ausführen einer Sammlungsschätzung**: Analysieren des Datenvolumens und der Relevanz für die Untersuchung.
- **Überprüfen und Verfeinern der Schätzung der Sammlung**: Stellen Sie sicher, dass die Sammlung Ihren Kriterien entspricht.
- **Commit der Sammlung auf einen Prüfdateisatz**: Bereiten Sie die Daten für eine detaillierte Analyse vor.
- **Exportieren der Suchergebnisse**: Speichern Sie die gesammelten Daten für weitere Überprüfungs- und Compliancezwecke.

>**Hinweis**: In diesem Lab wird der Zugriff auf einen M365 E5-Mandanten mit Daten vorausgesetzt, um eine Untersuchung durchzuführen. Sie können diese Übung auch ohne Daten durchführen, aber Sammlungen und Prüfdatensätze werden keine Ergebnisse liefern.

## Aufgabe 1: Erteilen von Berechtigungen für eDiscovery (Premium)

Zum Exportieren von Dateien benötigen Sie bestimmte Berechtigungen aufgrund des direkten Zugriffs, den diese Option für Benutzerdateien gewährt.

1. Navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an.
1. Wählen Sie die Karte **Einstellungen**.

   Wenn die Karte **Einstellungen** nicht angezeigt wird, wählen Sie **Alle Lösungen anzeigen** aus, und suchen Sie im Abschnitt **Core** nach **Einstellungen**.

1. Erweitern Sie im linken Navigationsbereich **Rollen und Bereiche** und wählen Sie **Rollengruppen**.
1. Wählen Sie auf der Seite **Rollengruppen für Microsoft Purview-Lösungen** die Option **eDiscovery-Manager**.
1. Wählen Sie auf der Fly-out-Seite **eDiscovery-Manager** auf der rechten Seite **Bearbeiten**.
1. Wählen Sie auf der Seite **eDiscovery-Manager verwalten** die Option **Benutzer auswählen**.
1. Wählen Sie auf der Fly-out-Seite **Benutzer auswählen** auf der rechten Seite den Benutzenden aus, mit dem Sie diese interaktive Übung durchführen möchten, und wählen Sie dann **Auswählen**.
1. Zurück auf der Seite **eDiscovery-Manager verwalten** wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **eDiscovery-Administrator verwalten** die Option **Benutzer auswählen** aus.
1. Wählen Sie auf der Seite **Rollengruppe überprüfen und fertigstellen** die Option **Speichern** aus, um Ihre Benutzenden zur eDiscovery-Manager-Rollengruppe hinzuzufügen.
1. Wenn Sie die Benutzenden erfolgreich hinzugefügt haben, wählen Sie **Fertig** auf der Seite **Sie haben die Rollengruppe erfolgreich aktualisiert**.
1. Wählen Sie **Startseite** aus, um zurück zur Startseite des Microsoft Purview-Portals zu navigieren.

Sie haben die eDiscovery-Manager-Berechtigung erfolgreich erteilt.

## Übung 2: Erstellen eines eDiscovery-Falls (Premium)

Nachdem Sie nun über die erforderlichen Berechtigungen verfügen, können Sie einen neuen eDiscovery-Fall erstellen, um ihre Untersuchung zu starten.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Portals befinden.

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an.

1. Wählen Sie **Alle Lösungen anzeigen** aus.
1. Wählen Sie unter **Risikomanagement und Compliance** die Karte **eDiscovery** aus.
1. Erweitern Sie im linken Navigationsbereich **Premium-Fälle** und wählen Sie dann **Fälle** aus.
1. Wählen Sie auf der Seite **eDiscovery (Premium)** die Option **+Fall erstellen** erstellen aus.
1. Geben Sie auf der Flyout-Seite **Fall benennen** rechts Folgendes ein:

   - **Name**: `Legal Investigation 2024`
   - **Beschreibung:** `eDiscovery case for the 2024 legal investigation involving relevant emails and documents.`

1. Fügen Sie auf der Seite **Teammitglieder hinzufügen und Einstellungen festlegen** die Benutzenden hinzu, die die Untersuchung durchführen werden, und wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Fall überprüfen** **Absenden** und dann **Fertig** aus.

Sie haben erfolgreich einen neuen eDiscovery-Fall mit dem Namen _Rechtsuntersuchung 2024_ erstellt.

## Aufgabe 3: Hinzufügen von Verwahrenden zum Fall

Nachdem Ihr Fall erstellt wurde, müssen Sie Verwahrende hinzufügen. Verwahrende sind Personen, die möglicherweise über relevante Informationen für die Untersuchung verfügen.

1. Nachdem Sie den Fall in der vorherigen Aufgabe erstellt haben, sollten Sie sich auf der Registerkarte **Übersicht** des Falles **Rechtsuntersuchung 2024** befinden.

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an. Wählen Sie die Karte **eDiscovery** unter dem Abschnitt **Risiko und Compliance**. Wählen Sie **Premium-Fälle** > **Fälle** und wählen Sie den neu erstellten Fall **Rechtsuntersuchung 2024** aus.

1. Wählen Sie in der oberen Navigationsleiste die Registerkarte **Datenquellen** und dann **Datenquelle hinzufügen** > **Neuen Verwahrer hinzufügen** aus.
1. Fügen Sie auf der Fly-out-Seite **Neuer Verwahrer** unter **Verwahrer auswählen** Verwahrende zu Ihrem Fall hinzu und wählen Sie dann **Weiter**.
1. Vergewissern Sie sich auf der Seite **Aufbewahrungsbereich**, dass die im vorherigen Schritt hinzugefügten Verwahrende ausgewählt sind, um sie auf die Warteschleife zu setzen.
1. Wählen Sie auf der Seite **Verwahrende überprüfen** die Option **Senden** und dann **Fertig**, sobald Ihre neuen Verwahrenden erstellt sind.

Sie haben dem Fall _Rechtsuntersuchung 2024_ erfolgreich Verwahrende hinzugefügt.

## Aufgabe 4: Erstellen und Ausführen einer Sammlungsschätzung

Nachdem Verwahrende hinzugefügt wurden, können Sie jetzt eine Sammlungsschätzung ausführen, um einen Überblick über das Datenvolumen und die Relevanz zu erhalten.

1. Nachdem Sie dem Fall in der vorherigen Aufgabe Verwahrende hinzugefügt haben, sollten Sie sich immer noch auf der Registerkarte **Datenquellen** des Falls **Rechtsuntersuchung 2024** befinden.  

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an. Wählen Sie die Karte **eDiscovery** unter dem Abschnitt **Risiko und Compliance**. Wählen Sie **Premium-Fälle** > **Fälle** und wählen Sie den neu erstellten Fall **Rechtsuntersuchung 2024** aus.

1. Wählen Sie die Registerkarte **Sammlungen** in der oberen Navigation und wählen Sie dann **+ Neue Sammlung**.
1. In der Konfiguration **Neue Sammlung** geben Sie der Sammlung einen **Namen und eine Beschreibung**. Geben Sie Folgendes ein:

   - **Name**: `Legal Data Collection`
   - **Beschreibung:** `Collecting emails and documents relevant to the 2024 legal investigation.`

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Verwahrte Datenquellen auswählen** die Option **+ Verwahrer auswählen**.
1. Fügen Sie auf der Aufklappseite **Verwahrer auswählen** auf der rechten Seite die Verwahrenden hinzu, die in der vorherigen Aufgabe zum Fall hinzugefügt wurden, und wählen Sie dann **Hinzufügen**.
1. Zurück auf der Seite **Verwahrte Datenquellen auswählen**, wählen Sie **Weiter**.
1. Zurück auf der Seite **Nicht-verwahrte Datenquellen auswählen**, wählen Sie **Weiter**.
1. Legen Sie auf der Seite **Zusätzliche Speicherorte** den Status auf **Ein** für diese Speicherorte fest:

   - Exchange-Postfächer
   - Öffentliche Exchange-Ordner

1. Wählen Sie **Weiter** aus.
1. Auf der Seite **Suchanfrage definieren** verwenden Sie die Suchfunktion, um eine Suche nach Inhalten zu erstellen, die für Ihren Fall relevant sind:

   - Verwenden Sie den Operator **AND**, um nach **Schlüsselwörtern** zu suchen, die **Equal** (gleich) mit `legal` sind.
   - Wählen Sie **Eine Untergruppe hinzufügen**.
   - Verwenden Sie den Operator **OR**, um nach **Schlüsselwörtern** zu suchen, die **Equal** (gleich) mit `contract` sind.

    >![Screenshot des Abfrage-Generators in eDiscovery Premium.](./Media/ediscovery-query-builder.png)

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Sammlung prüfen und erstellen** die Option **Senden** und dann **Fertig** auf der Seite **Neue Sammlung erstellt**.
1. Zurück auf der Seite **Sammlungen**, überprüfen Sie den Fortschritt Ihrer Sammlungsschätzung. Verwenden Sie die Schaltfläche **Aktualisieren**, um die Seite zu aktualisieren und den Status der Sammlungsschätzung zu überprüfen. Sobald der Status Ihrer Schätzung auf **Geschätzt** und der **Vorschaustatus** auf **Erfolgreich** aktualisiert wird, ist Ihre Sammelschätzung abgeschlossen.

    >![Screenshot der Schaltfläche „Aktualisieren“ und des Bewertungsstatus der Sammlung.](./Media/collection-estimate-status.png)

    >**Tipp**: Sobald Sie Ihre Sammlungsschätzung abgeschlossen haben, können Sie mit der Erstellung verschiedener Abfragen oder der Verwendung des KQL-Editors für erweiterte Suchvorgänge experimentieren. Aktivieren Sie dazu das Kontrollkästchen links neben der Sammlungsschätzung und wählen Sie **Sammlung bearbeiten**. So gelangen Sie direkt auf die Seite **Suchanfrage definieren**. Sie können Ihre Abfrage ändern und eine neue Sammlungsschätzung übermitteln, um zu untersuchen, wie Ihre Abfrage Ihre Sammlungsschätzung ändert.

1. Wählen Sie die **Rechtliche Datensammlung** und erkunden Sie die Sammlungsschätzung.

   - **Zusammenfassungs-Registerkarte**: Bietet einen Überblick über die Sammlungsstatistiken, einschließlich der abgerufenen Objekte, der Speicherorte mit Treffern und der Dateitypen.
   - **Datenquellen-Registerkarte**: Zeigt Informationen über verwahrte und nicht verwahrte Datenquellen an, die in der Sammlung enthalten sind.
   - **Suchstatistiken-Registerkarte**: Zeigt detaillierte Statistiken der letzten Sammlungsschätzung, einschließlich der Anzahl der Objekte und des Datenvolumens.
   - **Sammlungsoptionen-Registerkarte**: Listet die verschiedenen Optionen auf, die bei der Konfiguration einer Sammlung zur Verfügung stehen, z. B. die Einbeziehung von Cloud-Anhängen und Konversations-Threads.

    >![Screenshot, der die Registerkarten zeigt, die innerhalb der Schätzung für die Sammlung der gesetzlichen Datensammlung untersucht werden sollen.](./Media/explore-collection-estimate.png)

Sie haben erfolgreich eine Sammlung mit dem Namen _Rechtliche Datensammlung_ erstellt und geprüft.

## Aufgabe 5: Übertragen der Sammlung an einen Prüfdateisatz

Sobald die Sammlung zufriedenstellend ist, führen Sie einen Commit an einen Prüfdateisatz zur detaillierten Analyse durch.

1. Nachdem Sie in der vorherigen Aufgabe die Sammlungsschätzung erstellt haben, sollten Sie sich noch auf der Registerkarte **Sammlungen** des Falls **Rechtsuntersuchung 2024** befinden.  

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an. Wählen Sie die Karte **eDiscovery** unter dem Abschnitt **Risiko und Compliance**. Wählen Sie die Registerkarte **Premium-Fälle** > **Fälle** > **Rechtsuntersuchung 2024** > **Kollektionen**.

1. Wählen Sie die Sammlung **Rechtliche Datensammlung**.
1. Wählen Sie auf der Flyout-Seite **Rechtliche Datensammlung** auf der rechten Seite **Sammlung übertragen** (Commit ausführen).
1. Vergewissern Sie sich auf der Seite **Elemente an einen Prüfdateisatz übertragen**, dass die Option **Zu neuem Prüfdateisatz hinzufügen** ausgewählt ist, und geben Sie ihm einen Namen `Legal Case Review`.
1. Lassen Sie die anderen Standardeinstellungen ausgewählt und wählen Sie **Commit** aus, um die Sammlung in einen Prüfdatensatz zu übertragen.

Sie haben die Sammlung erfolgreich an einen Prüfdateisatz übertragen.

## Aufgabe 6: Erkunden des Prüfdateisatzes

1. Nachdem Sie die Sammlung in der vorherigen Aufgabe an einen Prüfdateisatz übertragen haben, sollten Sie sich immer noch auf der Registerkarte **Sammlungen** des Falls **Rechtsuntersuchung 2024** befinden.

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an. Wählen Sie die Karte **eDiscovery** unter dem Abschnitt **Risiko und Compliance**. Wählen Sie **Premium-Fälle** > **Fälle** > **Rechtsuntersuchung 2024** aus.

1. Wählen Sie die Registerkarte **Prüfdatensätze** in der oberen Navigation aus und wählen Sie dann den neu erstellten Prüfdatensatz **Rechtsfallprüfung** aus.
1. Wählen Sie auf der Flyout-Seite **Rechtsfallprüfung** rechts unten auf der Seite **Prüfdatensatz öffnen** aus.
1. Erfahren Sie, was Sie mit Elementen in Ihrem Prüfdateisatz tun können:

   1. **Filter**: Ermöglicht es Ihnen, Bedingungen anzuwenden, um die im Prüfdateisatz angezeigten Elemente einzugrenzen.
   1. **Tag**: Ermöglicht es Ihnen, Dokumente mit bestimmten Tags zu kennzeichnen, um eine bessere Organisation und Identifizierung zu ermöglichen.
   1. **Gruppe**: Ermöglicht ihnen das Organisieren von Prüfdateisatzinhalten nach verwandten Elementen wie Familien oder Unterhaltungen.
   1. **Ansichtsquelle**: Bietet eine umfassende Ansicht des ausgewählten Dokuments, wobei es im ursprünglichen Format angezeigt wird.
   1. **Nur-Text anzeigen**: Zeigt den extrahierten Text eines Dokuments an, ohne eingebettete Bilder und Formatierungen.
   1. **Anmerkungen**: Ermöglicht es den Benutzenden, Markups, Schwärzungen und andere Anmerkungen auf das Dokument anzuwenden.
   1. **Metadaten anzeigen**: Zeigt verschiedene Metadaten an, die mit dem ausgewählten Dokument verbunden sind, um einen detaillierten Einblick zu erhalten.

    >![Screenshot der verfügbaren Optionen für Prüfdateisätze in eDiscovery Premium.](./Media/review-set.png)

1. Nachdem Sie Ihren Prüfdateisatz untersucht haben, können Sie Elemente zur weiteren Analyse exportieren.

Sie haben Ihren Prüfdateisatz erfolgreich geöffnet und überprüft.

## Aufgabe 7 – Exportieren der Suchergebnisse

Um Ihre Arbeit zu speichern und weitere Analysen zu ermöglichen, exportieren Sie die Suchergebnisse.

1. Sie sollten sich immer noch im Prüfdateisatz **Rechtsfallprüfung** in eDiscovery (Premium) befinden.

   Falls nicht, navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden sich an. Wählen Sie die Karte **eDiscovery** unter dem Abschnitt **Risiko und Compliance**. Wählen Sie die Registerkarte **Premium-Fälle** > **Fälle** > **Rechtsuntersuchung 2024** > **Prüfdatensatz** > **Rechtsfallprüfung** aus.

1. Aktivieren Sie das Kontrollkästchen neben den Elementen, die Sie zur weiteren Analyse exportieren möchten.
1. Wählen Sie das Dropdown-Menü für **Aktionen** > **Exportieren** aus.

    >![Screenshot der Option zum Exportieren eines Prüfdateisatzes in eDiscovery Premium.](./Media/export-review-set.png)

1. Geben Sie auf der Flyout-Seite **Exportoptionen** auf der rechten Seite Folgendes ein:

   - **Exportname**: `LegalCaseExport_July2024`
   - **Beschreibung:** `Export of relevant emails and documents for the July 2024 legal case investigation.`
   - **Diese Dokumente exportieren**: Nur ausgewählte Dokumente
   - **Auswahl erweitern**: Nein
   - **Ausgabeoptionen**: Komprimierte Verzeichnisstruktur

1. Wählen Sie die Schaltfläche **Exportieren** am unteren Rand der Flyout-Seite.

    >![Screenshot der Konfigurationsoptionen zum Exportieren eines Prüfdateisatzes.](./Media/export-options-review-set.png)

1. Sie sollten eine Benachrichtigung erhalten, die besagt, dass **ein Auftrag erstellt** wurde, um Ihren Prüfdateisatz zu exportieren. Wählen Sie in dieser Benachrichtigung **OK** aus.
1. Um auf Ihren exportierten Prüfdateisatz zuzugreifen, erweitern Sie im linken Navigationsbereich **Premium-Fälle** und wählen Sie dann **Fälle** aus. Wählen Sie den Fall **Rechtsuntersuchung 2024** und dann die Registerkarte **Exporte** in der oberen Navigation.
1. Wählen Sie den Export **LegalCaseExport_July2024** aus.
1. Aktivieren Sie auf der Flyout-Seite **LegalCaseExport_July2024** auf der rechten Seite das Kontrollkästchen links neben jeder exportierten Datei und wählen Sie **Herunterladen**. Dadurch werden eine .csv-Zusammenfassung und eine Zip-Datei mit den exportierten Artikeln heruntergeladen.

    >**Tipp**: Möglicherweise müssen Sie den Popupblocker deaktivieren, um exportierte Dateien erfolgreich herunterzuladen.

Sie haben die Suchergebnisse für die Überprüfung erfolgreich exportiert.
