﻿# wenn man im Laufmodus startet und stoppt und den Modus NICHT wechselt, stürzt die App 10 Sekunden später ab (von Erwin)
 - Schritte zur Rekonstruktion
  - 1. App starten
  - 2. Kopfhörer verbinden
  - 3. Laufmodus starten
  - 4. 30 Schritte machen
  - 5. Laufmodus beendet und PopUp noch nicht weggecklickt
  - 6. Warten
  - 7. App stürtzt ab wegen Null Pointer exception

# wenn man ein zu kleines Display hat, wird manches abgeschnitten!! (von Jan)
  - z.B. bei Laufmodus (aktiv)
  - es könnte sich jemand das hier anschauen :) https://docs.microsoft.com/de-de/xamarin/xamarin-forms/user-interface/layouts/flex-layout (von valle)
  
# wenn man im Musikmodus ein paar mal öfter auf Start/Stopp klickt stürzt die App schnell ab (von Valle)
  - zuverlässig reproduzierbar, sobald man den Button 3 bis 4 mal kurz hintereinander drückt.

# Akzent TTS (unassigned - mittelwichtig)
  - Listen and Perform z.B. auf deutsch zu deutscher Aussprache usw. zwingen müsste machbar sein: https://docs.microsoft.com/de-de/xamarin/essentials/text-to-speech
### (Auf deutsch) Im Listen and Perform modus sagt die gute Frau "Nächste Aktivität Komma Eins Null Liegestütze" (von Erwin) - das ist nur bei dir so, es hängt von der Systemsprache ab!! das kann man fixen (s.o.)
### (Auf englisch) Im Listen and Perform modus sagt die gute Frau "Next Activiti Eins Null Liegstütze" (von Erwin)
# Muic Mode ( unassigned - nicht soo wichtig)
  - Gif seems to take some time loading!
  - (fixed) Message when going out of music mode should be removed! (was a debug message)

# Listen and perform (unassigned - nicht soo wichtig)
  - Feature: Anfeuern ("noch 5 usw.")
  
# Settings Hinweis (unassigned - nicht so wichtig)
  - Beim Ändern der Sprache sollte der Hinweis angezeigt werden, dass man die App neu starten soll.
  



 ------- erledigt --------

 # edit entry in listenandperform (Jan)
  - (fixed) Dialog wegklicken führt zu Löschung, sollte aber da bleiben
  - (fixed) Dialog überarbeiten (edit führt zu "add activity", was, wenn man dann abbricht?) (drüber reden)
  # Resource Strings formatieren(valle) 
  - (fixed) Ausrufezeichen weg usw.
  - (fixed) "you have taken 123 seps done" (Stepmode) - grammatikalische Struktur in Nachrichten berücksichtigen
  - (fixed) Data Overview (valle)
  - (fixed) Shouldn't say "welcome to", Strings besser formatieren.
  
 # Listen and perform (WICHTIG) 
  - Ausführungen von Liegestütze werden nicht korekt gespeichert (aber korrekt runtergezählt während Ausführung), aber nur wenn die App auf Englisch
	eingestellt ist!!! Sit-ups werden korrekt gespeichert, der Bug tritt im Countmode nicht auf. 
  - Bug tritt nicht auf wenn die App auf Deutsch eingestellt ist
  - Rekonstruktion
   - 1. App auf Englisch stellen und neu Starten
   - 2. Verbinden, in Listen&Perform wechseln, beliebigen Trainingsplan mit Liegestützen erstellen (Getestet: 3 Liegestütze, 5 Pause, 3 Sit-ups)
   - 3. Modus Starten, Trainingsplan abarbeiten
   - 4. Resultatspopup zeigt 0 Liegestütze und korrekte Anzahl ausgeführter Sit-ups an. (Angezeigt beim Test: 0 Liegestütze, 3 Sit-ups)
   - 5. Im Dataoverview werden nur die Sit-ups gespeichert
  
# Frequenz - Berechnung anpassen (valle)
  - (fixed) -- statt 0, falls stehend
  - (fixed) Berechnung anpassen (regression über letzte 5 Schritte).

# SamplingRate
  - (fixed) Einstellen funktioniert noch nicht zuverlässig (hinkt immer eine Einstellung hinterher oder so?)
  - (fixed) wenn man die App neu startet, wird die in den Einstellungen angezeigte Samplingrate zurückgesetzt (- fehlt hier logik?)

# Listen and Perform
  - (fixed) Popup sollte beim Ändern der Aktivität bei cancel nix löschen und generell nich "add activity" sagen - text wurde angepasst
# Impressum 
  - (fixed) Impressum fehlt noch... (benni)
# Timer im Zählmodus hat ADHS
  - (fixed) auch die Millisekunden sind zuverlässig dreistellig, sodass die Zahl nicht immer hin und her springt.

# Püp-üp Hinweis (valle)
  - (fixed) beim Verbinden: anzeigen, dass Verbindung gerade hergestellt wird, damit Nutzer nicht weg klickt.
  
  # MusicMode
  - (fixed) Label ändert sich nicht