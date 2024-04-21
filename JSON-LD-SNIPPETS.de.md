[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

# Strukturierte Daten Snippets: Der praktische Spickzettel 😎

## 🤔 Warum ein Spickzettel?
"Du musst nicht alles wissen, nur wissen, wo du es findest." Spickzettel sind ein unverzichtbares Werkzeug, um wichtige Informationen schnell zur Hand zu haben. Sie sind perfekt, um sich schnell in ein neues Thema einzuarbeiten oder als Erinnerungshilfe bei selten genutzten Befehlen oder Konzepten.

## Schema.org JSON-LD für Sitelinks-Suche
Nutze dieses generische Schema.org JSON-LD Snippet, um deine Website für Suchmaschinen transparenter zu machen. Dies verbessert nicht nur die SEO, sondern ermöglicht auch die Anzeige eines Sitelinks-Suchfelds in den Google-Suchergebnissen.

### Vorteile
- **SEO-Optimierung**: Verbesserung durch strukturierte Daten.
- **Sichtbarkeit in Suchergebnissen**: Ermöglicht das Sitelinks-Suchfeld bei Google.

### JavaScript-Integration
Hier ist der JavaScript-Code, um das JSON-LD Snippet in deine Website einzubinden:
```javascript
jQuery(document).ready(function () {
    class Init {
        createScriptTag(data) {
            var script = document.createElement('script');
            script.type = 'application/ld+json';
            script.innerHTML = JSON.stringify(data);
            document.getElementsByTagName('head')[0].appendChild(script);
        }
    }
    const Schema = new Init();
    Schema.createScriptTag({
        "@context": "https://schema.org",
        "@type": "WebSite",
        "url": "https://example.com/",
        "potentialAction": [{
            "@type": "SearchAction",
            "target": "https://example.com/?search={search_term_string}",
            "query-input": "required name=search_term_string"
        }]
    });
});
