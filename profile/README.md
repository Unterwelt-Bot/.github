<div align="center">

# 🔥 Willkommen in der Unterwelt

**Unterwelt-Bot** – ein Discord-Bot, der die Gameserver einer Freundesgruppe verwaltet.<br>
Mit KI-Gestalten aus der griechischen Unterwelt, die im Gespräch erledigen, was sonst ein Admin per Hand tut.

[🌐 Vorstellung](https://unterwelt-bot.github.io/) · [🎬 Einführung ansehen](https://youtu.be/9Z54kDcur0U)

</div>

---

## Was er tut

Server starten und stoppen, Zugangsdaten herausgeben, Mods pflegen, Einstellungen ändern, neue Server bauen, kranke Server heilen, Musik spielen – und das alles im Gespräch. Man schreibt einfach in Discord, und die Gestalt antwortet, die in dem Kanal wohnt.

- 💬 **Ansprechen statt Menüs** – „Charon, wie komme ich auf den Server?“
- ❗ **Befehle ohne KI** – was mit `!` beginnt, wird sofort erledigt.
- 🎙️ **Sprechen statt tippen** – Sprachnachrichten werden verstanden, und auf Wunsch antworten die Gestalten im Voice mit eigener Stimme.

## Wer hier wohnt

Jede Gestalt ist eine KI-Figur mit fester Rolle. Sie kann nur, was ihre Werkzeuge erlauben – und was jemand darf, prüft der Bot, nicht die KI.

| Ort | Gestalt | Aufgabe |
|---|---|---|
| 🚪 **Die Pforte** | 🐕 Kerberos | erklärt den Bot. Beißt nicht. Meistens. |
| | ⛵ Charon | bringt Neue auf die Server: Einladung, Launcher, Mods |
| | 🃏 Momos | spottet, spielt kleine Spiele, beantwortet allgemeine Fragen |
| | 🍇 Dionysos | alles im Spiel: Durchsagen, Whitelist, Events |
| 🎻 **Das Orchester** | 🎵 Orpheus | macht Musik und liest vor |
| ✉️ **Direktnachricht** | 🪽 Hermes | sieht nach und richtet Botschaften an die Verwalter aus |
| 👑 **Der Thronsaal** | 🔱 Hades | der Alltag der Server: Status, Start und Stopp |
| | 📐 Daidalos | Einstellungen und Dateien |
| | 🔨 Hephaistos | baut Mods und Modpacks |
| | 🌸 Persephone | erschafft als Einzige neue Server |
| | 📜 Mnemosyne | weiß alles über die Games. Wirklich alles. |
| | ⚕️ Asklepios | heilt Server, wenn sie krank sind |

## Drei Regeln

1. **Stufen** – Fremde, Spieler, Eingeweihte, Verwalter, Besitzer. Je höher, desto mehr darf man. Stufen vergeben nur Menschen, keine KI.
2. **Einwilligung** – Die Gestalten denken mit einer KI außerhalb der Unterwelt. Bevor etwas von einer Person dorthin geht, willigt sie ein; für Sprachnachrichten und Stimmen gesondert.
3. **Erst planen, dann ändern** – Keine Gestalt ändert einfach so etwas an einem Server. Sie schreibt einen Plan, ein Verwalter übernimmt ihn, vorher wird gesichert – und wenn es schiefgeht, kommt alles zurück.

## Wie es gebaut ist

```
 Discord ──► n8n-Workflows (läuft Tag und Nacht) ──► Claude-Gestalten mit festen Werkzeugen
                     │
                     ▼  REST
             Agent auf dem Gameserver-Rechner (einzige Stelle, die Docker anfasst)
                     │
                     ▼
             Gameserver als Docker-Container ◄── Mitspieler über ein privates Netz
```

- **Kern:** [n8n](https://n8n.io/)-Workflows auf einem kleinen Rechner, der rund um die Uhr läuft
- **Gestalten:** [Claude](https://www.anthropic.com/claude)-Modelle mit fest verdrahteten Werkzeugen
- **Server:** [Docker](https://www.docker.com/)-Container auf einem großen Rechner, der nachts schläft und sich aus Discord wecken lässt
- **Zugang:** über ein privates Netz ([Tailscale](https://tailscale.com/)) – nichts davon ist aus dem Internet erreichbar

---

<div align="center">
<sub>Ein Hobbyprojekt. Die Repos dieser Organisation sind privat – diese Seite und <a href="https://unterwelt-bot.github.io/">unterwelt-bot.github.io</a> sind die öffentliche Vorstellung.</sub>
</div>
