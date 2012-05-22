Aus dem Pad übernommen:

Wie ändere ich das Zonefile richtig
-----------------------------------

Die Zonefiles müssen nach einem bestimmten Schema geändert werden, da es sonst zu epischen Problemen kommt und Fritz euch dann tötet, weil ihr Domains wegbuxt oder einfach eine falsche Serial-Nummer eintragt!

Bevor du irgendwelche Änderungen tust, mache bitte ein git pull origin master. Solltest du bereits Änderungen getan haben, tue vor dem git pull ein git stash und nach dem Pull ein git stash pop.

Wenn du ein Zonefile änderst, achte darauf, dass du die Serial-Nummer im SOA-Record erhöhst. Das Format ist YYYYMMDDNN, wobei YYYY das Jahr ist, MM der Monat, DD der Tag und NN eine Zahl. Also z.B. 2012052201 für die erste Änderung am 22. Mai 2012. Wenn du dies nicht tust, dann wird der DNS-Server die Zone nicht aktualisieren, also tue es!

Noch ein wichtiger Hinweis: Tue niemals einen Force-Push! Also gib niemals -f als Flag für git push an, sonst werde ich dich wie gesagt töten!

Wenn dies für dich zu kompliziert ist, so frage jemanden™ (Wie z.B. mich), ob er dir die Änderungen einbaut

