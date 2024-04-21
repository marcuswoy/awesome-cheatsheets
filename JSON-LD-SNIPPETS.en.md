[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/LeCoupa/awesome-cheatsheets/blob/master/LICENSE)

# Structured Data Snippets: The Practical Cheat Sheet 😎

## 🤔 Why Cheat Sheets
"You don't have to know everything, just know where to find it." With this motto in mind, I create cheat sheets that make my professional and personal life easier. In this repository, you'll find a collection of useful, quickly accessible resources and guides to help you work more efficiently and save time.

## Schema.org JSON-LD for Sitelinks Search
Use this generic Schema.org JSON-LD snippet to make your website more transparent to search engines. This not only improves SEO but also enables the display of a Sitelinks search box in Google search results.

### Advantages
- **SEO Optimization**: Enhanced by structured data.
- **Visibility in Search Results**: Enables the Sitelinks search box on Google.

### JavaScript Integration
Here is the JavaScript code to integrate the JSON-LD snippet into your website:
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
