# Pagespeed-Optimierungen

Auf dieser Seite finden Sie ein paar Hinweise zur Optimierung des Pagespeeds.

## Contao Speed Bundle

Um Bilder erst dann zu laden, wenn Sie wirklich sichtbar sind, können Sie z. B. das Contao Speed Bundle von heimrichhannot installieren. Suchen Sie im Contao Manager nach der Erweiterung **heimrichhannot/contao-speed-bundle** und installieren diese. Wie Sie Lazyload bei Bildern aktivieren können, finden Sie in der [Dokumentation](https://github.com/heimrichhannot/contao-speed-bundle).

## Cache aktivieren

Wenn Sie in der .htaccess, die unter dem Ordner **/web** liegt, folgenden Code einfügen, aktivieren Sie das Caching für Bilder, HTML, CSS und JavaScript.

```
<IfModule mod_expires.c>
ExpiresActive On
ExpiresByType text/html "access plus 500 seconds"
ExpiresByType image/gif "access plus 1 year"
ExpiresByType image/ico "access plus 1 year"
ExpiresByType image/jpeg "access plus 1 year"
ExpiresByType image/jpg "access plus 1 year"
ExpiresByType image/png "access plus 1 year"
ExpiresByType text/css "access plus 1 month"
ExpiresByType text/javascript "access plus 1 month"
ExpiresByType application/x-javascript "access plus 1 month"
ExpiresByType application/javascript "access plus 1 month"
</IfModule>
```

## Bilder in WEBP ausliefern

Ab Contao 4.8 haben Sie bei den Bildgrößen die Möglichkeit die Bilder per WEBP auszuliefern. Das können Sie unter **Themes** > **Bildgrößen des Theme bearbeiten** (zweitletztes Icon) > **Einstellungen der Bildgröße bearbeiten** (zweites Icon) unter den **Experten-Einstellungen** einstellen. Beim Demodaten-Import ist dies standardmäßig nicht aktiv, da es nicht bei jedem Hosting-Paket unterstützt wird.

![](../_images/nature-theme/einrichtung/webp_aktivieren.png)

## Bildgrößen verwenden

Wenn Sie ein Bild platzieren, sollten Sie immer eine Bildgröße verwenden, damit das Bild auch wirklich nur entsprechend groß geladen wird, wie es auch dargestellt wird. Für News, Events und Slider und weitere Elemente liefert das Nature Theme bereits vordefinierte Bildgrößen mit.

## SSL aktivieren

Liefern Sie Ihre Webseite am besten per HTTPS aus. Das können Sie in Ihrem Hosting Paket anpassen, viele Anbieter bieten auch bereits kostenlose SSL-Zertifikate an.
