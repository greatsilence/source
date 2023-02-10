+++
title = "Posting Hugo Github"
date = 2021-10-27T20:10:09+02:00
description = "This text was generated using the After Dark post archetype."
toc = false
categories = ["hacking"]
tags = ["after", "dark"]
images = [
  "https://source.unsplash.com/collection/983219/1600x900"
] # overrides site-wide open graph image
[[copyright]]
  owner = "Matthias Fuchs"
  date = "2021"
  license = "cc-by-nc-sa-4.0"
+++

Wow, das war eine 'lange Reise' bis zu dieser Website. Mehrere Blogs habe ich besucht.

Jetzt habe ich's endlich geschafft. Im Folgenden beschreibe ich den Workflow, um eine statische Website mit Hugo und After-Dark auf Github zu betreiben.

## Workflow
 - Zuerst After-Dark und Hugo installieren.
 - Dann auf Github zwei Repositories erstellen: eines für den Blog-Inhalt (posts), das andere für den Blog selber (Module, theme, search, ...).
 - Das Repo für den Blog-Inhalt **muss** den Namen USER.github.io besitzen. Hier lade ich per Git den Inhalt des public Verzeichnisses hoch. Da auf meinem ersten Account bereits ein Repo mit diesem USER Namen besteht {{< external href="https://mfuchs1.github.io/" text="the lion blog" />}}, musste ich einen zweiten Account extra für diese Website anlegen (und dazu eine andere Email-Adresse verwenden).
 - Das zweite Repo kann einen beliebigen Namen tragen. Besser wäre es allerdings, eine Bezeichnung mit `source` oder `Hugo` zu verwenden (damit man erkennt, wozu dieses Repo dient). Dorthin kommt das Eltern-Verzeichnis von public.
 - Jetzt kommt der 'tricky part': Das public-Verzeichnis wird per submodule mit dem Eltern-Verzeichnis verbunden.
 
 ```console
 $ git submodule add -b main -f https://github.com/USER/USER.github.io.git public 
 ```
 - Eine kleine, aber wichtige Info: ich habe bemerkt, dass man - nach dem Erstellen eines Repos - besser nicht im Webbrowser die `Back`-Buttons benutzen soll, um zurück zu gehen. Dies macht (fast) alle bisherigen Einstellungen rückgängig. Also: einfach den Tab schließen. 
 - Ab jetzt muss ich beide Repos bei jeder Änderung mit git 'bearbeiten'. 
 
 ```console
$ hugo new post/<Name_des_posts>.md   	## mit Editor bearbeiten (draft auf 'false' setzen)
$ hugo server -D			## Kontrolle; startet lokalen Server
$ Crtl-C 				## lokalen Server beenden
$ hugo 					## Website in /public erstellen
$ git add .				## git-Befehle 
$ git commit -m "einen commit schreiben"
$ git push -u origin main
 ```
 
 - Voilà!
 
Zum Schluss noch ein Bild von einem Löwen:

![Löwe](/lion.png)
 
Thank you for choosing After Dark.
