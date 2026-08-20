---
icon: layout-dashboard
---

# The New Game UI

The current DopeRaider interface is a command center for running an empire. It keeps your wallet, resources, operator identity, active upgrades, current district, live activity, and navigation visible while you work.

The desktop layout is organized around three working areas:

1. **Left rail:** your operator and persistent profile context.
2. **Center stage:** the screen you are actively using.
3. **Right rail:** screen-specific information and game chat.

On smaller screens, the same features collapse into a responsive layout. The controls may move or stack, but the gameplay routes remain the same.

<figure><img src=".gitbook/assets/screen-inventory-desktop.jpg" alt="DopeRaider desktop inventory interface"><figcaption><p>The command center keeps the economy, operator, and current activity in one view.</p></figcaption></figure>

## Read the HUD from top to bottom

### Brand and district

The top-left header identifies DopeRaider and shows the district currently loaded in the game shell. Your **home district** and **current location** are separate: home is where your profile is based, while current location changes when you travel.

### Resource strip

The header resource strip gives you a fast operating snapshot:

| Tile | What it tells you |
| --- | --- |
| **Dinero** | Your working cash for purchases, travel, upgrades, and other game actions. |
| **Respect** | Your reputation and progression position. It also matters for boss competition. |
| **DIRT** | Your current mined DIRT inventory, shown in GB. |
| **Weed** | Your current WEED inventory. |
| **Exploits** | Inputs used to mine DIRT. |
| **Seeds** | Inputs used to grow WEED. |
| **Capacity** | Current carried inventory versus your maximum carry capacity. |

The capacity meter changes color as you approach full. Treat a nearly full bag as a decision point: you may need room before producing, buying, raiding, or collecting a reward.

### Wallet state

The wallet panel shows whether the connected wallet is ready and which network the current game session expects. The production experience is labeled **MAINNET**. A wallet address is abbreviated for readability; use the full public address only when a support case requires it.

## The left profile rail

The profile rail is your persistent operator card. It includes:

* Your current avatar and username.
* Home district and current district.
* Player-since information.
* World rank when the leaderboard has enough data to calculate it.
* Raid totals, wins, and losses.
* Active timed upgrades, including tier and remaining time.
* A quick **Profile** action for your operator name, avatar, and shareable operator card.

The rail is useful for making decisions without leaving the screen you are playing. For example, you can check whether Raid Protection or Safe House is still active before committing to a valuable route.

## The center stage

The center stage is the active screen. The bottom navigation opens the main routes:

| Route | Use it for |
| --- | --- |
| **Inventory** | Review cash, inputs, product, capacity, profile information, and quick actions. |
| **Upgrades** | Buy protection, production, capacity, and raid-related advantages. |
| **Cartel** | Review your social and cartel-related progression. |
| **Missions** | Check current objectives, progress, and available mission rewards. |
| **Market** | Compare district prices and execute buys or sells. |
| **Production** | Start and monitor WEED growth or DIRT mining jobs. |
| **Map** | Compare districts, routes, travel costs, and destination context. |
| **Raid** | Find eligible rivals and resolve offensive or defensive raid activity. |

The active route is highlighted in the navigation bar. The Map icon also reflects the current district context.

## The right context rail

The right rail changes with the current screen. It can show screen status, district, network, wheel rules, market context, production context, or other supporting information. It is deliberately secondary: use the center stage for the action and the right rail for the conditions around it.

The right rail also contains the desktop chat dock when chat is available. On smaller layouts, chat becomes a floating panel so it does not permanently take space from the game controls.

## Notifications

The bell icon opens the notification panel. The unread badge updates while you are in the game. Notifications are useful for raid activity and other events that may happen while you are focused on production, trading, or travel.

If the unread count looks stale, open the panel once or refresh the game route. A notification badge is a convenience signal; always verify important balances and game state on the relevant screen.

## Settings and personal controls

The gear icon opens **Settings**. The current controls are:

| Setting | Effect |
| --- | --- |
| **Tutorial** | Shows or hides guided gameplay help on the inventory screen. |
| **Music** | Turns district soundtrack playback on or off. |
| **Cinematics** | Enables or disables travel, raid, and bust video sequences. |
| **Game chat** | Shows or hides Cherry chat inside the game HUD. |
| **Profile** | Opens your operator profile and share-card controls. |

Music and cinematic preferences are presentation choices. They do not change game results, prices, rewards, or transaction requirements.

## A reliable first-session routine

When the new UI first loads:

1. Confirm the wallet label and network before approving a transaction.
2. Read **Home district**, **Current location**, and **Capacity** together.
3. Check active upgrades and their remaining time in the left rail.
4. Open Inventory for the fastest overview of your position.
5. Use Market, Production, Map, and Raid as separate decisions rather than trying to do everything from one screen.
6. Open Settings to choose whether tutorial, music, cinematics, and chat are visible.

{% hint style="warning" %}
The interface can make information easier to see, but it does not remove game risk. Confirm the amount, wallet, destination, and network in your wallet before signing any paid action.
{% endhint %}

## Related features

* [Game Chat](chat.md) for the embedded Cherry community channel.
