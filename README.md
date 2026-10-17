# Trampolin-Zähler (PWA)

Dateien zusammen in einen Ordner auf einem Webserver mit **HTTPS** legen
(Kamera und Bewegungssensor funktionieren in Safari nur über HTTPS).

Möglichkeiten:
- Homelab: z. B. Caddy/Nginx-LXC hinter deinem Reverse Proxy mit gültigem Zertifikat
- GitHub Pages oder Cloudflare Pages (kostenlos, HTTPS automatisch)
- Schnelltest im LAN: `npx serve` + Tunnel wie `cloudflared tunnel --url http://localhost:3000`

Auf dem iPhone: Seite in Safari öffnen → Teilen → „Zum Home-Bildschirm“.

## Modi
- **Sensor**: Handy am Körper (enge Tasche/Armband). Erkennt freien Fall (Flug) und
  Landestoß. Liefert Flugzeit und Sprunghöhe (h = g·t²/8).
- **Kamera**: Handy auf Stativ seitlich zum Trampolin. Bilddifferenz → Höhe der
  Bewegung → Scheitelpunkte werden gezählt.

Empfindlichkeit über den Regler anpassen; die gestrichelten Linien im Signal-Plot
zeigen die aktuellen Schwellen (orange = freier Fall, grün = Landung).
