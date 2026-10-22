# Accessibility audit with wcag-scout

Audit a website for accessibility from your own GitHub repository, without installing anything.
The audit runs [wcag-scout](https://github.com/locorida/wcag-scout) (axe-core in headless
Chromium) and produces an HTML and PDF report mapped to WCAG 2.2 and EN 301 549, in German or
English.

*Deutsch: [siehe unten](#deutsch).*

## Use it

1. Click **Use this template** → **Create a new repository**.
   Choose **Private**, so that only you can see your reports.
2. In your new repository, open **Actions** → **Accessibility audit** → **Run workflow**.
3. Enter a **sitemap URL** or one or more **URLs**, choose the language, and start.
4. When the run has finished:
   - the **job summary** shows the number of findings by severity;
   - under **Artifacts**, download `accessibility-report`. It contains `report.html`,
     `report.pdf`, `report.json` and the screenshots.

### Privacy and costs
- The report only exists in **your** repository and is deleted after 7 days (`retention-days`
  in `.github/workflows/audit.yml`). Nothing is sent to or stored by the author of the template.
- In a **public** repository, artifacts, job summaries and logs, including the audited URLs,
  are visible to everyone. Use a private repository.
- Runs count against your GitHub Actions minutes. A typical audit of 50 pages takes a few minutes.

### Please crawl responsibly
- Only audit websites you own or are allowed to audit.
- wcag-scout honours robots.txt, pauses between requests (1 s), loads at most `max-pages`
  pages, and never submits forms or sends data to the site.
- Enter your own **contact URL**, so site operators can reach you.
- Some sites block requests from cloud servers such as GitHub's; those pages are listed in the
  report as "could not be loaded".

### Limits
Automated tests detect only part of all accessibility problems. The report is not proof of
conformance with WCAG, EN 301 549 or the BFSG and does not replace a manual audit. The report
lists what has to be checked by hand.

---

## Deutsch

Prüfen Sie eine Website auf Barrierefreiheit aus Ihrem eigenen GitHub-Repository, ohne etwas zu
installieren. Der Lauf verwendet [wcag-scout](https://github.com/locorida/wcag-scout) (axe-core
im Headless-Chromium) und erzeugt einen HTML- und PDF-Report mit Zuordnung zu WCAG 2.2 und
EN 301 549, auf Deutsch oder Englisch.

### So geht's

1. **Use this template** → **Create a new repository** klicken.
   **Private** wählen, damit nur Sie Ihre Reports sehen.
2. Im neuen Repository **Actions** → **Accessibility audit** → **Run workflow** öffnen.
3. Eine **Sitemap-URL** oder eine oder mehrere **URLs** eintragen, Sprache wählen, starten.
4. Nach dem Lauf:
   - zeigt die **Zusammenfassung** die Anzahl der Befunde nach Schweregrad;
   - liegt unter **Artifacts** der Download `accessibility-report` mit `report.html`,
     `report.pdf`, `report.json` und den Bildschirmfotos.

### Datenschutz und Kosten
- Der Report liegt nur in **Ihrem** Repository und wird nach 7 Tagen automatisch gelöscht
  (`retention-days` in `.github/workflows/audit.yml`). Beim Autor der Vorlage kommt nichts an.
- In einem **öffentlichen** Repository sind Artefakte, Zusammenfassungen und Logs samt der
  geprüften URLs für alle sichtbar. Verwenden Sie ein privates Repository.
- Die Läufe zählen gegen Ihre GitHub-Actions-Minuten. Ein typischer Lauf mit 50 Seiten dauert
  wenige Minuten.

### Verantwortungsvoll prüfen
- Prüfen Sie nur Websites, die Ihnen gehören oder für die Sie die Erlaubnis haben.
- wcag-scout beachtet die robots.txt, wartet zwischen Anfragen (1 s), lädt höchstens
  `max-pages` Seiten und schickt nie Formulare oder andere Daten an die Website.
- Tragen Sie Ihre eigene **Kontakt-URL** ein, damit Betreiber Sie erreichen können.
- Manche Websites sperren Anfragen von Cloud-Servern wie denen von GitHub; solche Seiten stehen
  im Report als „konnte nicht geladen werden“.

### Grenzen
Automatisierte Tests erkennen nur einen Teil der Barrierefreiheitsprobleme. Der Report ist kein
Nachweis der Konformität mit WCAG, EN 301 549 oder BFSG und ersetzt keine manuelle Prüfung. Der
Report nennt, was manuell geprüft werden muss.

## License

[MIT](LICENSE)
