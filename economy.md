---
icon: earth-africa
---

# Economy

DopeRaider has a live, district-by-district economy. Every district keeps separate markets for **WEED** and **DIRT**, and their prices change as players buy, produce, travel, sell, raid, and get busted.

The Market screen is not a fixed price list. The price you see is a snapshot of the current district state. Other players can change it before you complete your next move.

<figure><img src=".gitbook/assets/screen-market-desktop.jpg" alt="DopeRaider market screen showing district product prices, supply, and pools" width="720"><figcaption><p>Each district has its own live WEED and DIRT market.</p></figcaption></figure>

## The two things behind every product price

Each district tracks two values for each finished product:

| Market value | What it means |
| --- | --- |
| **Supply** | The amount of that product currently counted in the district. Product carried by players in the district is part of this picture. |
| **Pool** | The Dinero available behind that product market—the liquidity that supports purchases and pays sales. |

The relationship between the pool and supply is the market's supply-and-demand signal:

* **More pool with less supply** means the product is relatively scarce against available buying power, so its quote rises.
* **More supply with less pool** means more product is competing for the available buying power, so its quote falls.
* WEED and DIRT have their own pools and supplies. A busy WEED market does not automatically set the DIRT price in the same district.

In simple terms, the base unit value comes from `product pool ÷ product supply`. The market adds the current buy spread to the buy quote; the current configuration uses a 5% spread. Sales use the current local pool-to-supply value. Price floors and settlement rounding protect the market from collapsing below its live configured minimums.

{% hint style="info" %}
In DopeRaider, “demand” is not a separate order-book number. It is expressed through the amount of Dinero in a product's pool relative to the product available in that district.
{% endhint %}

## How actions move the economy

Every action changes supply, a pool, or both. That is why prices can vary after players move around the map.

| Player action | What changes | What it can mean for future prices |
| --- | --- | --- |
| **Buy WEED or DIRT** | The purchased product is added to the buyer's inventory and the district's product supply. Most of the payment is routed into market liquidity, with the local share directed to that product's pool. | Both supply and pool move. The next quote is recalculated from the new balance, not copied from the old quote. |
| **Sell WEED or DIRT** | The sold product leaves the seller and the district supply; the matching product pool pays the seller. | The sale uses the quote at settlement. It changes the pool left for later sellers and the supply left in the district. A sale is not automatically a price pump or dump—check the new quote. |
| **Complete WEED growth or DIRT mining** | Finished output is added to the producer's inventory and home-district supply. | More product enters that district without an equal product-pool increase, which puts downward pressure on that product's local quote. |
| **Start production or buy SEEDS/EXPLOITS** | The player spends Dinero on inputs or production fees. These payments add liquidity through the revenue system. | The input or production cost can support market pools even before finished product is collected. |
| **Travel with product** | Your carried WEED and DIRT are removed from the district you leave and added to the district you enter. Travel fees also add liquidity. | The origin becomes relatively scarcer; the destination receives more supply. This is the main reason a route can change prices at both ends. |
| **Win or lose a raid** | Stolen product leaves the loser and follows the winner. | If the two players are in different districts when the raid settles, supply moves between markets. If they remain in the same district, the district's total product supply is largely unchanged. |
| **Get busted** | Confiscated product is removed from the player's current district. Part of it is impounded in the Vice Island LockUp. | The source district loses supply, while impounded product becomes part of the LockUp economy in Vice Island. |
| **Pay for travel, upgrades, raids, or other eligible actions** | The payment is distributed through the revenue system. | Spending can add liquidity to local and city-wide product pools even when no finished product is bought or sold. |

## Buying and selling: what the quotes mean

There are two useful numbers for every finished product:

| Quote | Meaning |
| --- | --- |
| **Buy price** | What you pay to add WEED or DIRT to your inventory in that district. It includes the market's buy spread. |
| **Sell price** | What the local product pool pays for product you sell there. |

The buy-and-sell difference is deliberate. Buying and immediately selling the same product in the same market is not a free profit loop. A profitable route must cover the buy spread, production costs, travel fees, possible boss tax, and the risks of holding product.

Sales can only happen outside your home district. That rule forces product into the travel network instead of letting players produce and cash out in one safe location.

### Why one sale does not have one simple price effect

A sale takes both product and Dinero from the same local market at the current sell quote. That means a small sale can reduce the pool and supply in roughly the same proportion. The quote may stay close to where it was, or it may move after rounding, price floors, other player actions, and later liquidity changes.

Do not assume “selling always makes the remaining product more valuable” or “selling always crashes the price.” Read the live Market screen again after important activity settles.

## Moving product changes two markets

Product is counted where the carrier is, not where it was originally bought or produced.

For example:

1. You collect WEED in your home district. That adds WEED supply there.
2. You travel with it to another district. Your WEED is removed from the home district's supply and added to the destination's supply.
3. You sell it. The destination's WEED pool pays you, and the product leaves that destination's supply.

That is the supply-and-demand loop in action. A crowded destination can lose its price advantage as traders arrive with the same product. Meanwhile, removing product from the origin can make it relatively scarcer there.

Travel itself also matters: normal and Fast Travel fees add revenue to the destination-side market flow. At the current configuration, eligible net revenue is split **80% locally** and **20% across the city pools**, after the platform-fee allocation. Local action therefore has its biggest effect where it happens, while still contributing some liquidity across the wider world.

## Production creates supply; spending creates liquidity

SEEDS and EXPLOITS are production inputs. Their local purchase prices are shown on the Market screen, but the live pool-and-supply price formula applies to the finished products: WEED and DIRT.

Production affects the economy in two stages:

1. **Start the job:** input purchases and production fees are paid into the revenue flow, adding liquidity to product pools.
2. **Collect the output:** finished WEED or DIRT enters the home district's supply.

The two stages matter because a district can gain liquidity before it gains product supply. Once a wave of players collect output, that added supply can change the local product quote. Grow Power and Mining Power can increase and accelerate output, so widespread use of those upgrades can make a production district change faster.

## Raids, busts, and the LockUp

Raids and busts do not create market prices by themselves; they move or remove the product that the market counts.

* A **raid** transfers product from the loser to the winner. Its market effect depends on the players' locations when the raid settles.
* A **bust** confiscates half of a player's carried WEED and DIRT when the player has enough product to be affected. Half of that confiscated amount is impounded in the LockUp—effectively one quarter of the original carried product before rounding.
* The confiscated product is removed from the district where the bust happens. The impounded portion is added to the LockUp at Vice Island, giving later LockUp activity something to fight for.

This makes route risk part of price discovery. Product that never reaches its selling district cannot be sold there, and a successful or failed route can change what future traders find on the Market screen.

## How player spending supports markets

DopeRaider's economy does not depend only on selling. Eligible spending—including finished-product purchases, input purchases, production fees, travel, upgrades, and the non-stake part of raid entry—feeds the revenue system.

The current system routes revenue into product pools:

* **Product buys** direct the local share to the pool for the product purchased.
* **Input purchases, production, travel, upgrades, and raid fees** split the local share across WEED and DIRT pools.
* A city-wide share is distributed across district product pools, so activity outside your district can still contribute to its liquidity.
* Where a district boss applies to a product purchase, the current boss tax is paid to that boss. That portion is not routed into the product's market pool.

This is why active players matter even when they are not selling the same product you carry: their spending can change the liquidity side of the market.

## Read a route before you commit

Use this checklist before moving value:

1. Compare the **current** buy price at the origin and sell price at the destination.
2. Check both product supply and pool, not just the headline price.
3. Add SEED/EXPLOIT costs, production fees, travel fees, and the buy spread.
4. Consider whether other traders are likely to bring the same product to the destination.
5. Leave capacity and Dinero for the route itself.
6. Factor in normal-travel bust risk, raid exposure, and any protection you plan to use.
7. Re-check prices immediately before buying and selling. Live markets can move while you travel.

```text
route result = destination sell payout
             − origin buy cost
             − input and production costs
             − travel and protection costs
             − losses from busts, raids, or price movement
```

There is no guaranteed profitable route. The edge comes from understanding how player activity is changing both supply and liquidity before the rest of the market reacts.

{% hint style="warning" %}
Market values, fees, floors, and revenue splits are live game settings and can change by season or deployment. The Market screen and the final transaction settlement are authoritative for a specific action.
{% endhint %}
