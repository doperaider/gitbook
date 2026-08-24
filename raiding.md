---
icon: bullseye
cover: .gitbook/assets/cover-raiding-lockup.jpg
---

# Raiding and the LockUp

Raiding is DopeRaider's player-versus-player risk system. A raid can take product, Respect, and the raid stake—but it is not a blanket random roll. In player raids, different weapon choices have a fixed outcome. The LockUp is separate: its lockpick attempt uses published crack and jackpot odds.

<figure><img src=".gitbook/assets/raid-rivals.png" alt="Two DopeRaider rivals ready to raid" width="520"><figcaption><p>Raids reward preparation, capacity, and reading the matchup.</p></figcaption></figure>

<figure><video src=".gitbook/assets/raid-italy.mp4" controls poster=".gitbook/assets/raid-italy-poster.jpg"></video><figcaption><p>A player raid in Little Italy.</p></figcaption></figure>

## At a glance

| Area | What decides the result |
| --- | --- |
| Player raid with different weapons | The weapon counter is deterministic. There is no percentage roll. |
| Player raid with the same weapon | Raid Tie Power first, then Respect when the tied power is equal. |
| LockUp attempt | 25% chance to crack the vault; a jackpot is a 10% chance among successful cracks. |
| Product taken | The target's available product and the winner's free carry capacity. |
| Respect | Respect helps settle equal-power weapon ties and is transferred on successful raids. |

## Starting a player raid

Choose a player in your current district and start the raid from the raid flow. The system checks the following before it can begin:

* You cannot raid yourself.
* Both players must be in the same district.
* Neither player can already have an unresolved raid.
* The target cannot have active **Raid Protection** or be hidden by an active **Safe House**.
* Starting a raid clears your own active Raid Protection and Safe House, so do not expect those protections to remain after you commit.

There is no product-holding threshold required merely to start a current player raid. Rewards still depend on what the target is carrying and on the capacity you have left to receive it.

### Cost, stake, and timer

The current mainnet raid settings are:

| Item | Current value | What it means |
| --- | ---: | --- |
| Raid charge | 1.40 DINERO | The amount charged to open the raid. |
| Raid stake | 1.05 DINERO | The value at risk in the player-raid settlement. |
| Raid fee | 0.35 DINERO | The non-stake portion of the standard raid charge. |
| Raid timer | 90 seconds | The time before an unresolved raid expires. |

If the target escapes or the raid expires, the initiating wallet can recover it. On the current mainnet recovery flow, the full 1.40 DINERO raid charge is returned automatically when possible; reconnect the wallet that started the raid if recovery is waiting. The amount displayed by the live raid result is the authoritative settlement record.

Starting a player raid also grants the challenger **+1 Respect**.

## Player-raid weapon matchups

Choose one weapon for the raid. The triangle is fixed:

| Your weapon | It defeats | It loses to |
| --- | --- | --- |
| Pistol | Shotgun | Rifle |
| Shotgun | Rifle | Pistol |
| Rifle | Pistol | Shotgun |

For example, Shotgun versus Rifle is a Shotgun win every time. Choosing a different weapon from the opponent therefore has no hidden win-rate calculation: you either selected the counter or you did not.

## Raid Tie Power and Respect

**Raid Tie Power** is the tie-breaking strength supplied by the temporary **Raid Tie Breaker** upgrade. It matters only when both players choose the same weapon.

1. Compare the active Raid Tie Breaker tier. The higher tier wins the weapon tie.
2. If the tiers are equal, compare Respect. The player with more Respect wins the tie.
3. If both the tier and Respect are exactly equal, the live settlement resolves the final result; do not treat an equal tie as a guaranteed win or assume a published percentage.

Raid Tie Breaker is currently available in Baltimore and lasts one hour. Its tier also adds bonus Respect to a successful raid:

| Tier | Tie Power | Bonus Respect on a raid win |
| --- | --- | ---: |
| I | Active | +0 |
| II | Stronger than Tier I | +1 |
| III | Stronger than Tier II | +2 |
| IV | Strongest | +3 |

Respect therefore has two jobs in player raids:

* It is the final player-side comparison when matching weapons have equal Tie Power.
* It is a reward that can be taken in a successful raid. A normal successful player raid transfers **1–5 Respect**, limited by what the losing player actually has; active Raid Tie Power adds the tier bonus shown above. A player can never lose more Respect than they hold.

Example: two players both select Pistol. A Tier III Raid Tie Breaker beats a Tier I Raid Tie Breaker. If both have Tier III, the player with more Respect wins the tie. A Tier III winner then receives the normal Respect transfer plus **2 bonus Respect**, subject to the loser's available Respect.

## What a player-raid win pays

A successful player raid settles the stake and can transfer WEED, DIRT, and Respect.

* Product can never exceed **half of the target's combined carried product** in a normal player raid.
* Product is also capped by your free carry capacity. Leave room before raiding; a full inventory limits what you can collect.
* Respect is capped at the losing player's available Respect.
* The player who wins the settled raid receives the stake. An expired raid is not a win; it follows the recovery path described above.

The exact split of product between WEED and DIRT comes from the target's available stash at settlement. A large-looking target does not guarantee a large payout if they have already sold, moved, or lost their product.

## The LockUp

The **LockUp** is the police vault at Vice Island. It is not a player-versus-player weapon contest: you make a lockpick attempt against the vault itself.

<figure><video src=".gitbook/assets/lockup-success.mp4" controls poster=".gitbook/assets/lockup-success-poster.jpg"></video><figcaption><p>A successful LockUp crack.</p></figcaption></figure>

### How the LockUp fills

The LockUp holds impounded product from busts. When a player is busted while carrying product, half of their WEED and half of their DIRT is confiscated. One half of that confiscated amount is sent to the LockUp—effectively **25% of each carried product before rounding**. The rest leaves the player's inventory without being added to the vault.

That means a more active and riskier world can create a richer LockUp target. The current normal-travel bust chance is 10%; Bust Protection removes that normal-travel risk while active.

### LockUp odds of winning

Each LockUp attempt has these current odds:

| Result | Chance per attempt |
| --- | ---: |
| Vault holds | 75% |
| Standard crack | 22.5% |
| Crack with jackpot | 2.5% |
| Any successful crack | **25%** |

A jackpot is **not** a separate 10% chance on every attempt. First, the vault must crack (25%). Then a successful crack has a 10% jackpot chance. That is why the overall jackpot chance is 2.5%: `25% × 10%`.

These are per-attempt probabilities, not a promise that one of every four consecutive attempts will crack. Each attempt is settled independently by the raid system.

### LockUp rewards and limits

On a successful crack, the LockUp can award impounded WEED and DIRT, plus **5–10 Respect** when the vault has sufficient Respect to pay it. A jackpot applies a **2× product-reward multiplier**.

The multiplier does not bypass inventory limits. The LockUp calculates its reward against your available carry capacity, so even a jackpot cannot overfill your normal capacity. It also cannot award product that is not in the vault.

Raid Tie Power, weapon selection, and player-versus-player Respect comparisons do **not** change the LockUp's 25% crack chance or its jackpot odds. Prepare for the LockUp by keeping capacity clear, rather than by trying to counter a weapon.

## Raid planning checklist

Before a player raid:

* Confirm you and the target are in the same district.
* Check that the target is not protected or hidden.
* Leave enough capacity for product you may win.
* Select the weapon that counters the target's likely choice.
* For a same-weapon matchup, compare Raid Tie Power and Respect rather than guessing at a percentage.
* Remember that attacking removes your own Raid Protection and Safe House.

Before hitting the LockUp:

* Know that the vault crack chance is 25%, with a 2.5% overall jackpot chance.
* Keep room for product—the jackpot multiplier still respects capacity.
* Treat the vault contents as variable: bust activity fills the LockUp, and earlier successful raiders can reduce it.

Game settings and balance values can be updated over time. The live raid screen and its final settlement are authoritative for an individual raid.
