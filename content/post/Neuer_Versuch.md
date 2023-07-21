+++
title = "Neuer Versuch"
date = 2023-07-21T21:41:59+02:00
description = "This text was generated using the After Dark post archetype."
draft = false
toc = false
categories = ["Emacs"]
tags = ["emacs", "hugo"]
images = [
  "https://source.unsplash.com/collection/983219/1600x900"
] # overrides site-wide open graph image
[[copyright]]
  owner = "Matthias Fuchs"
  date = "2023"
  license = "cc-by-nc-sa-4.0"
+++

So, hier beginne ich neu. Eine andere Möglichkeit ist, dass ich in Emacs `eshell` öffne und dort die Befehle ausführe, welche ich in dem Post "Github.." beschrieben habe.

## Positives
Natürlich ist das möglich. Und in Emacs lässt sich Markdown problemlos bearbeiten. Bei den Überschriften ist zu beachten: Headlines mit einem "#" erhalten im Blog eine durchgezogene Linie. Ab zwei "##" verschwindet diese Linie - siehe Blog. Headlines werden in Markdown mit dem Befehl: C-c C-s 1(2,3, ... - Level) eingefügt. Was ist eine "automatische Headline" (C-c C-s h)? Aha, das fügt eine nächste Hedaline auf dem selben Niveau wie die vorhergehende ein.

Gibt es sog. capture-templates in Markdown? Nein, gibt es nicht.

## Negatives
Was nicht so gut klappt: ich kann nicht die Server-Adresse `anklicken`. Das liegt wohl an eshell; eventuell geht das mit anderen Emacs-Methoden (so etwas wie: url markieren und diesen Link öffnen?). Hab es gefunden: browse-url-firefox. In Konsole kann ich mit C-c den Hugo Server stoppen. Das geht in eshell nicht.

Ein weiterer "Nachteil": ich kenne Markdown kaum. Es wird wohl einfacher sein, ein org-file zu schreiben (mit dem denote-template) und dieses hinterher nach Markdown zu exportieren, wobei noch ein paar Dinge im Header des Files zu verändern sind.

## Conclusion
So: ich werde wohl bei org-mode bleiben.

Thank you for choosing After Dark.
