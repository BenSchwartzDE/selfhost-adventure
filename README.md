# Zazubi.de

Zazubi.de ist das Endresultat eines 7-wöchigen Projektes, welches erfolgreich am 8.03.2022 abgeschlossen wurde. Das Grundkonzept der Zazubi.de Webseite besteht aus 2 Teilen.

- Öffentliche Webseite mit anmelde Funktion

- Interne App zum Erstellen und verschicken von Anmeldecodes per Mail.

## Öffentliche Webseite mit anmelde Funktion

Die Login-Page ist ziemlich übersichtlich aufgebaut. Lediglich ein zentriertes Login Formular.

<img title="" src="https://i.imgur.com/VkDANYU.png" alt="" data-align="center">

Durch das Eingeben des einmaligen 5 stellen Anmeldecodes gelangt man auf die Hauptseite der Zazubi.de Webseite.<img title="" src="https://i.imgur.com/ON647CL.png" alt="" data-align="center">

In der Datenbank wurden folgende Informationen gespeichert:

- Name (Vor + Nachname)

- E-Mail-Adresse

- Login code (5-stellig)

- download code

- Erstellungsdatum

- Login Datum

- Download Datum

- Login Status

- Download Status

Der Login Vorgang prüft, ob der Anmeldecode existiert und gültig ist. Ist das der Fall speichert er den Namen, Downloadcode und den download Status in die Session. Dadurch kann auf der Hauptseite der Nutzer begrüßt und der download Button angezeigt werden. Durch das Klicken des Download-Buttons wird eine Funktion ausgelöst, die prüft, ob der download code existiert und gültig ist. Ist das der Fall wird der Datei download angestoßen, falls nicht, wird der Nutzer auf eine Errorpage weitergeleitet.

# Internes Tool (Budibase)

Kommen wir zur internen Seite der Zazubi.de Webseite. Hierbei nutze ich Budibase, eine open source low-code Plattform für die interne Abwicklung von Erstellung und Versand der Anmeldecodes.

<img title="" src="https://i.imgur.com/9qsCOyO.png" alt="" data-align="center">

Hierbei wird der Anmelde- und Downloadcode automatisch generiert und bereitgestellt. Nach dem Absenden werden diese Daten, inklusive der Input Daten in der Datenbank gespeichert und eine automatisch generierte E-Mail wird an den angegebenen Empfänger versendet.


