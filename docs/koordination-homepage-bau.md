# Hochzeit der zwei Seiten — Homepage (Schaufenster) und Bau (Motor)

Kurz, damit beide Sessions dasselbe Bild haben. Stand 13.10.2026.

## Zwei Seiten, ein Projekt
- Schaufenster (Homepage): https://reraise.ai, liegt bei Cloudflare (Pages + D1).
  Startseite, acht Unterseiten, Brett-Vorfuehrung /board/, Boerse-Beta /trade/,
  Einbinde-Skript embed.js, Anmeldung mit laufender Nummer -> ERPNext. Von oben gebaut (die Sahne).
- Motor (Bau): Repo worldbuilder-app (apps/board, packages/mcp-server, packages/core,
  Board-API, Store). Von der Architektur hoch gebaut. Das ist dein (Groks) Revier.

## Die Schnittstelle (wo sie sich treffen)
- Das Brett unter /board/ auf der Homepage ist heute nur eine Vorfuehrung mit Beispieldaten
  — fest verdrahtet, keine echte Logik.
- Die Boerse /trade/ ist eine eigenstaendige Beta auf Cloudflare D1 (Nummer holen, Karte
  einbringen, nehmen, Rangliste).
- Dein Ziel: der echte Motor (Board-UI <-> Board-API <-> Store <-> MCP), bewiesen am
  Hormus-Szenario, CI gruen. Wenn M1 (Walking Skeleton) gruen ist, ersetzt das echte Board
  die Demo unter /board/. Das ist der Uebergabepunkt.

## Gemeinsame Sprache (bitte identisch bauen)
- Drei Szenarien zeigt das Schaufenster schon: Goldmarkt, Vitamin-D-Behauptung,
  Lagekarte Hormus. Baue denselben Satz.
- Features, die das Schaufenster bewirbt und die der Motor echt machen muss: Zeitschieber,
  "My stance", Rollenspiel-Schalter (Agenten als Spieler), Kamingespraech.
- Kartenformat: Apache 2.0, oeffentlich auf GitHub Reraise-ai/reraise/docs/card-format.md.
  App-Code: AGPL 3.0.

## Dein Rueckstand = die "noch nicht gebaut"-Liste der Homepage
Das Schaufenster verspricht, der Motor liefert: privater Tausch Geraet-zu-Geraet,
Trefferbilanz von Quellen, Rollenspiel mit Agenten als Spielern, Kartenstufen, Bezahlung,
fertige Anbindungen je System, und das Werkzeug selbst (Brett-App, API, MCP-Server) veroeffentlicht.

## Nur aus dem Katalog
Dienste nur aus docs/microservice-katalog.md. Fuer Reraise gelten Sockel 1,6,10,15,34,39,46
plus 2,3,12,26,30,36 (Guthaben-Konto 12, Rechte 3 = Kern). Eigenbau: ARCA, MercadoPago,
Agenten-Zaehler, Beleg-Spur. ERPNext-Grundregel: was ERPNext kann, laeuft dort.

## Quellen
- Homepage-Stand: Claude-Projekt "Wordbuilder", claude/handover-reraise-homepage-erpnext-2026-10-12.md
  und claude/uebergabe-reraise-homepage-2026-10-12.md; PDF in C:\Projects\Claude outputs\handover\.
- Homepage live-Quellen auf dem Server: C:\Projects\reraise-site\quellen5\ ; live: C:\Projects\reraise-site\live3\.
- Wissen: qmd query -c weltenbauer "<thema>".
