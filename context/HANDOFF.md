# KI-Übergabe: picast.com

## Zweck
picast.com als eigenständige Website auf einem Server in Frankfurt betreiben. Dieses Vorhaben ist strikt von **manualAI** getrennt. Der Schweizer Quantencomputer und die Random-Funktion gehören nur zu manualAI; manualAI-Code darf nicht in picast.com deployt werden.

## Bestätigte Hosting-Entscheidung
Der Nutzer hat ausdrücklich zugestimmt:

- Amazon Lightsail
- Linux/Ubuntu
- Frankfurt, AWS-Region `eu-central-1`
- 1 GB RAM, 2 vCPU, 40 GB SSD, 2 TB Transfer
- Zum Zeitpunkt der Preisprüfung genannter Listenpreis: 7 USD/Monat; Steuern und mögliche Transfer-Mehrkosten können hinzukommen

Diese Entscheidung ist eine Bestätigung des Tarifs, **kein Nachweis, dass eine Instanz bereits erstellt wurde**.

## Bestehendes GitHub-Projekt
Privates Repository: [manuelpicard/server](https://github.com/manuelpicard/server). GitHub leitet den früheren Namen `makopipokam/picast-server` auf diesen kanonischen Namen um.

- Branch: `main`
- Scaffold-Commit: `e4efdce` (`Initialize picast.com Frankfurt hosting scaffold`)
- Struktur: `app/`, `infrastructure/lightsail/`, `deploy/`, `docs/`
- Gesprächsarchiv: [`CONVERSATION.md`](CONVERSATION.md)

## Status und offene Voraussetzungen

- **Server nicht provisioniert.** Es gab keinen erfolgreichen AWS-Login bzw. keine bestätigte Lightsail-Instanz.
- **Website-Quellcode fehlt.** Der Nutzer sagte, er werde Kontozugang und Repository bereitstellen; ein Quellcode-Repository wurde im bisherigen Verlauf noch nicht genannt. Nicht `manualai.org` oder anderen manualAI-Code als picast-Quelle verwenden.
- **DNS nicht konfiguriert.** Zugriff auf Registrar/DNS-Anbieter und aktuelle DNS-Zielwerte fehlen. Erst nach Bereitstellung der Instanz und Prüfung der App DNS-Einträge ändern.
- **Domain:** Nutzer sagt am 2026-10-07, picast.com gekauft zu haben. Ein früherer öffentlicher Prüfstand zeigte eine Verkaufsseite; diese alte Beobachtung ist durch die spätere Aussage des Nutzers überholt und kein Grund, die Domain als ungekauft zu behandeln.
- **AWS-Konsole:** Der Konsolenzugriff aus der damaligen Umgebung war nicht möglich. Einen sicheren, vom Nutzer autorisierten AWS-Zugang herstellen, ohne Zugangsdaten im Chat oder Repository zu erfragen/speichern.

## Empfohlene nächste Schritte

1. Vom Nutzer die URL des tatsächlichen picast.com-Quellcode-Repositories und den Anwendungstyp/Runtime klären, sofern nicht bereits verfügbar.
2. Einen sicheren AWS-Anmelde-/Autorisierungsweg herstellen; danach die bestätigte Lightsail-Instanz in `eu-central-1` erstellen. Vor dem Start weiterhin den aktuellen Tarif und mögliche Steuern/Mehrkosten im Konto prüfen.
3. Ubuntu absichern, HTTPS/TLS und minimale Firewall-Regeln konfigurieren, App nach ihrer tatsächlichen Laufzeit deployen und Betrieb/Logs prüfen.
4. DNS-Zugriff vom Nutzer erhalten; erst dann `picast.com` und ggf. `www.picast.com` auf die verifizierte Serveradresse umstellen.
5. Zugangsdaten, private Schlüssel und `.env`-Werte nie committen. Infrastruktur- und Deployment-Dokumentation im privaten Repository aktualisieren.
