---
icon: messages
---

# Game Chat

DopeRaider includes Cherry-powered game chat directly inside the game HUD. It is a community surface for talking while you trade, produce, travel, raid, and defend your district.

Game chat is separate from the gameplay transaction flow. Chat access does not give the chat service permission to move your funds, and joining chat does not change your game balances or inventory.

## Where chat appears

On the desktop command center, chat mounts in the right-side dock below the context rail. On narrower layouts, it becomes a floating panel above the mobile controls. It can be open, minimized, or disabled without leaving the game route.

The chat panel header shows:

* **Game chat** as the channel name.
* **Cherry live** when the embed is ready.
* **Connecting** while the embed is starting.
* An unread counter when messages are waiting.
* A minimize or open control.

Chat is intentionally hidden on the landing page, login, intro, admin, and public share routes. It becomes available after the player profile and wallet session are ready on a gameplay route.

## Open, minimize, or disable chat

To minimize chat, press the minus control in the chat header. The panel becomes a compact button; press the open control to restore it. Your collapsed preference is remembered locally.

To disable chat completely:

1. Open the gear icon.
2. Find **Game chat** under Settings.
3. Switch it to **OFF**.

Turn it back on from the same setting. Chat preferences are local to the browser/device and do not change your player profile.

## Wallet-bound access

Chat uses the wallet associated with the current DopeRaider player session. A short-lived Cherry chat token is requested from the logged-in game session, and the wallet can be asked to sign a challenge when authentication is needed.

This means:

* You must be logged into a player profile before posting.
* The connected wallet must match the wallet used by the player profile.
* Reconnecting a different wallet can make the chat session read-only or require re-authentication.
* A chat signature is an authentication challenge; it is not a payment approval.

Never approve a transaction you did not intend to make, and never give anyone a seed phrase or private key. If a wallet prompt appears to request a transfer, close it and verify the origin before continuing.

## Read-only fallback

If the Cherry authentication token cannot be obtained, the embed may still mount as a read-only preview. In that state you may be able to see the channel, but posting is unavailable.

If you cannot post:

1. Confirm the connected wallet address matches the player profile.
2. Reconnect that wallet in the game.
3. Reload the gameplay route and let chat reconnect.
4. If the panel remains read-only, note the public wallet address and approximate time for support.

Do not create a new wallet or make a payment just to recover chat access.

## Chat behavior and notifications

Unread counts appear in the chat header and can also be reflected in the game HUD notification state. The game refreshes player notifications periodically, so the badge may update after a short delay.

Minimizing chat does not stop the session from receiving messages. Disabling chat prevents the embed from mounting until you enable it again.

## Cherry and the DopeRaider game are related but different surfaces

DopeRaider can run as a standalone game or inside Cherry-supported surfaces. Embedded game chat is a Cherry service inside the normal game UI; it is not the same thing as the complete game mini-app hosted inside a chat client.

The gameplay state, wallet connection, avatar identity, and chat authentication can therefore fail independently. When reporting a problem, say which surface you are using:

* Standalone game at `game.doperaider.com`.
* Cherry-hosted game or mini-app.
* Game chat embedded in the standalone game.

This distinction helps support investigate the correct session and dependency.

## Troubleshooting

| Problem | Likely cause | What to try |
| --- | --- | --- |
| Chat is not visible | You are on a hidden route, chat is disabled, or no player wallet is connected. | Open a gameplay route, enable Game chat in Settings, and reconnect the player wallet. |
| Chat says **Connecting** for a long time | The session token or Cherry dependency is unavailable. | Reload once, confirm the wallet/profile match, and try again. |
| You can read but not post | Chat fell back to read-only or the wallet challenge was not completed. | Reconnect the matching wallet and reload the route. |
| Chat keeps asking for a wallet | The active wallet changed or the previous challenge expired. | Confirm the abbreviated address, reconnect once, then retry. |
| The panel covers a control on mobile | The floating panel is open over the responsive HUD. | Minimize it, or disable Game chat in Settings. |
| Messages look stale | The embed or unread refresh has not completed. | Reopen the panel or reload the gameplay route. |

## Related features

* [The New Game UI](new-ui.md) for the context rail, settings, notifications, and responsive layout.
