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
 - Das Repo für den Blog-Inhalt muss den Namen <Benutzername>.github.io besitzen. Hier lade ich per Git den Inhalt des public Verzeichnisses hoch.
 - Das andere Repo trägt einen anderen Namen. Dorthin kommt das Eltern-Verzeichnis von public.
 - Jetzt kommt der 'tricky part': Das public-Verzeichnis wird per submodule mit dem Eltern-Verzeichnis verbunden.
 
 ```sh
 git submodule add -b main -f https://github.com/greatsilence/greatsilence.github.io.git public 
 ```

 - Ab jetzt muss ich beide Repos bei jeder Änderung mit git 'bearbeiten'. 
 - Voilà!
 
 
Thank you for choosing After Dark.
