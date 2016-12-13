urprünglich veröffentlicht auf <www.dastra.de>

## Herzlich Willkommen zum 1-Minuten-Blog mit Hugo!

Ich werde im Rahmen des [Web&Wine]
(https://www.meetup.com/de-DE/web-and-wine/events/235929431/)-Lightning-Talks
vorstellen, wie man mit dem *statischen Seitengenerator* [HUGO](https://gohugo.io/)
einen eigenen Blog erstellen kann. Die ersten Schritte können in einer Minute
bewältigt werden.

<!--more-->

### Was werden wir betrachten?

1. Erstellen einer Seite
2. Erstellen von Posts
3. Verwendung von Themen
4. Hosting des Blogs auf GitHub Pages
5. Einbettung von Kommentaren

### Erstellen einer Seite

Hugo kann über die [offizielle GitHub-Seite](https://github.com/spf13/hugo/releases/)
bezogen werden und wiegt nur etwa 5MB. Nach der Installation kann eine neue Seite
über folgenden Befehl erzeugt werden:

```
$ hugo new minuteblog
...
$ tree minuteblog
+--- minuteblog
|   +--- archetypes
|   +--- config.toml
|   +--- content
|   +--- data
|   +--- layouts
|   +--- static
|   +--- themes
```

### Erstellen von Posts

Posts werden zuerst mit Hugo generiert und können dann editiert werden. Posts
enthalten bereits Meta-Informationen.
Für die Strukturierung des Textes wird *Markdown* verwendet. Gute Ressourcen, um die Markdown-Syntax nachzuschlagen sind:

- [John Grubers urprüngliche Spezifikation](https://daringfireball.net/projects/markdown/)
- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

Ein Post wird über folgenden Befehl generiert:

```
$ hugo new post/first.md
```

Nach dem erstellen von Posts möchte man in der Regel eine Vorschau der Seite
anschauen. Dazu kann Hugos eingebauter Webserver verwendet werden. Dieser wird
gestartet über `hugo server -D`. Der Parameter `-D` bewirkt dabei, dass auch
Posts gerendert werden, die noch als `draft` markiert sind.

Allerdings bemerkt man, dass der Seite noch ein Thema fehlt.

### Verwendung von Themen

Es kann zwischen einer großen Anzahl von Themen für Hugo gewählt werden. Diese
werden auf der [offiziellen Seite](https://themes.gohugo.io) präsentiert. Für
diesen Blog verwenden wir [hugo-tranquilpeak-theme]
(https://themes.gohugo.io/hugo-tranquilpeak-theme/). Eine Demo des Themas kann
hier betrachtet werden: <https://tranquilpeak.kakawait.com/>

```
$ cd themes
$ git submodule add https://github.com/kakawait/hugo-tranquilpeak-theme.git
```

Anschließend sollte die Konfigurationsdatei des Themas in das
Projekt-Root-Verzeichnis kopiert und angepasst werden.

### Hosting des Blogs auf GitHub Pages

Mit Hugo muss vor dem Hosting die HTML-Version der Seite erzeugt werden. Dies
geschieht über den Befehl `hugo`. Dabei werden aus dem Thema und den Markdown-
Dateien eine gültige Seitenstruktur erzeugt und unter `public` abgelegt.

Mit dem Dienst [Pages](https://pages.github.com/) bietet GitHub die Möglichkeit,
statische Seiten direkt zu hosten. In der Regel wird ein ganzes Repository als
Internetseite verstanden und kann über die URL `https://username.github.io/repo`
erreicht werden.

Gibt es in dem Repository jedoch einen Unterordner `docs`, so kann dieser als
Quellverzeichnis gewählt werden. Damit Hugo die Seite in `docs` ablegt,
bedarf es eines kleinen Tricks:

```
$ mkdir docs
$ ln -s docs public
$ hugo
```

Danach geht man in dem GitHub-Repository auf *Settings > GitHub Pages* und wählt
*master branch /docs folder* als Quelle aus. Nach dem nächsten Push des Codes ist
die Seite über <https://username.github.io/repo> erreichbar.

### Einbettung von Kommentaren

Viele Themen erlauben es, [Disqus](https://disqus.com/) zur Einbettung von
Kommentaren einzubinden. Auch mit dem verwendeten Thema ist dies möglich. Nach
der Registrierung bei Disqus, kann eine neue Seite angelegt werden. Diese wird
eindeutig über den sog. *shortname* identifiziert. Die ganze URL für diesen Blog
lautet *minutenblog*.disqus.com.

Damit Kommentare eingebettet werden können, muss nur folgender Eintrag in
`config.toml` gesetzt werden:

```
disqusShortname = "minutenblog"
```

Herzlichen Dank für die Aufmerksamkeit!
