# Kasona mit Claude und ChatGPT verbinden

*English version below.*

Mit Kasona kannst du in Claude oder ChatGPT über dein Kasona-Konto sprechen: Depot-Check, Trade-Log, gespeicherte Thesen, Watchtower-Hinweise, Berichte, Unternehmensanalysen und deine Podcastfolgen. Die Antworten nennen Quellen und Datum.

Die Verbindung liest nur. Sie führt keine Trades aus, bewegt kein Geld und ist keine Anlageberatung.

## Voraussetzungen

- Ein Kasona-Konto mit **Plus** oder **Max** (auch in der Testphase).
- Ein Claude- oder ChatGPT-Konto, in dem du eigene Verbindungen hinzufügen darfst.

## In Claude (claude.ai oder Claude Desktop)

1. Öffne Claude und gehe zu **Customize > Connectors**.
2. Klicke auf **+ Add** und dann auf **Add custom connector**.
3. Name: `Kasona`. URL: `https://mcp.kasona.ai/mcp`. Speichern.
4. Klicke bei Kasona auf **Connect**. Du landest bei der Kasona-Anmeldung.
5. Melde dich mit deinem Kasona-Konto an, prüfe die angezeigten Berechtigungen und klicke auf **Erlauben**.
6. Starte einen neuen Chat und frag zum Beispiel: „Wie steht mein Depot?“

In Team- oder Enterprise-Konten kann nur die Administration eigene Verbindungen hinzufügen.

## In Claude Code (mit den Kasona-Skills)

```
/plugin marketplace add Kasonaops/kasona-claude-plugin
/plugin install kasona@kasona
```

Danach einmal mit deinem Kasona-Konto anmelden, wenn Claude Code danach fragt.

## In ChatGPT

1. Öffne **chatgpt.com/plugins** und klicke auf **+**.
2. Wähle **Add custom MCP server**.
3. Name: `Kasona`. URL: `https://mcp.kasona.ai/mcp`. Authentifizierung: **OAuth**.
4. Bestätige den Hinweis und klicke auf **Create as a plugin**.
5. Melde dich mit deinem Kasona-Konto an und klicke auf **Erlauben**.
6. Wähle Kasona im Chat über `@` aus und frag zum Beispiel: „Was hat Kasona zuletzt über Apple gesagt?“

Eigene Verbindungen sind in ChatGPT nicht in jedem Tarif verfügbar. In Business- und Enterprise-Arbeitsbereichen muss die Administration sie freischalten.

Sobald Kasona in den Verzeichnissen von Claude und ChatGPT gelistet ist, kannst du dort einfach nach „Kasona“ suchen.

## Beispielfragen

- „Wie steht mein Depot?“
- „Welche Watchtower-Hinweise gab es diese Woche?“
- „Fasse meinen Trade-Log des letzten Monats zusammen.“
- „Was hat Kasona zuletzt über Apple gesagt?“
- „Mach einen Deep Dive zu Microsoft.“

## Verbindung trennen

- **Claude:** unter **Customize > Connectors** Kasona entfernen.
- **ChatGPT:** das Kasona-Plugin öffnen und trennen oder entfernen.

Wenn Kasona zusätzlich den Zugriff sperren soll, schreib an hallo@kasona.ai. Bereits gespeicherte Chats verwaltest du in Claude oder ChatGPT.

## Probleme?

- **„Plus- oder Max-Abonnement erforderlich“:** dein Kasona-Konto hat keinen passenden Tarif. Prüfe den Tarif unter kasona.ai.
- **Falsches Konto angemeldet:** bei Kasona abmelden und die Verbindung in Claude oder ChatGPT neu starten.
- **Keine Ergebnisse:** prüfe, ob in deinem Konto Depots, Berichte oder Folgen vorhanden sind.
- Sonst: hallo@kasona.ai

Datenschutz: https://kasona.ai/datenschutz

---

# Connect Kasona to Claude and ChatGPT

With Kasona you can talk to your Kasona account in Claude or ChatGPT: depot check, trade log, saved theses, Watchtower alerts, reports, company research and your podcast episodes. Answers cite sources and dates.

The connection is read-only. It does not place trades, does not move money and is not investment advice.

## Requirements

- A Kasona account with **Plus** or **Max** (trial included).
- A Claude or ChatGPT account that allows you to add your own connections.

## In Claude (claude.ai or Claude Desktop)

1. Open Claude and go to **Customize > Connectors**.
2. Click **+ Add**, then **Add custom connector**.
3. Name: `Kasona`. URL: `https://mcp.kasona.ai/mcp`. Save.
4. Click **Connect** next to Kasona. You are taken to the Kasona sign-in.
5. Sign in with your Kasona account, review the permissions shown and click **Allow**.
6. Start a new chat and ask, for example: "How is my portfolio doing?"

In Team or Enterprise accounts, only an admin can add custom connections.

## In Claude Code (with the Kasona skills)

```
/plugin marketplace add Kasonaops/kasona-claude-plugin
/plugin install kasona@kasona
```

Then sign in once with your Kasona account when Claude Code asks.

## In ChatGPT

1. Open **chatgpt.com/plugins** and click **+**.
2. Choose **Add custom MCP server**.
3. Name: `Kasona`. URL: `https://mcp.kasona.ai/mcp`. Authentication: **OAuth**.
4. Confirm the notice and click **Create as a plugin**.
5. Sign in with your Kasona account and click **Allow**.
6. Select Kasona in the chat with `@` and ask, for example: "What did Kasona say about Apple recently?"

Custom connections are not available on every ChatGPT plan. In Business and Enterprise workspaces an admin has to enable them.

Once Kasona is listed in the Claude and ChatGPT directories, you can simply search for "Kasona" there.

## Example questions

- "How is my portfolio doing?"
- "Which Watchtower alerts came in this week?"
- "Summarize my trade log for last month."
- "What did Kasona say about Apple recently?"
- "Do a deep dive on Microsoft."

## Disconnect

- **Claude:** remove Kasona under **Customize > Connectors**.
- **ChatGPT:** open the Kasona plugin and disconnect or remove it.

If you also want Kasona to block access, email hallo@kasona.ai. Manage chats already stored in Claude or ChatGPT there.

## Problems?

- **"Plus or Max subscription required":** your Kasona account has no eligible plan. Check your plan on kasona.ai.
- **Wrong account signed in:** sign out of Kasona and restart the connection in Claude or ChatGPT.
- **No results:** check that your account has portfolios, reports or episodes.
- Otherwise: hallo@kasona.ai

Privacy: https://kasona.ai/datenschutz
