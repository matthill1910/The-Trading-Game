## Hello Traders
Hello Traders, this game is perfect if you are interested in a career in Market-Making. Popularised by Gary Stevenson in the book 'The Trading Game'.
This style of market-making exercise is commonly used in interviews and internship assessments at a range of trading and financial firms. It helps test numerical intuition, speed, and an ability to manage risk while making two-way prices.

**How the Game Works:**
ou act as a market-maker in a simple pricing game. There are several hidden cards, each containing a random number within a known range (for example, 1–9). The total of all cards represents the fair value of the market. Before any cards are revealed, each unseen card is assumed to be worth its expected value, so you can estimate the overall theoretical fair price at every stage of the game.

As the game progresses, cards are turned over one by one. Each reveal gives you new information and changes the fair value. Your job is to:

1. Estimate the updated expected value (EV) after each reveal
2. Provide bid/offer quotes that respect allowed spread widths
3. Ensure your prices are skewed correctly depending on your current position
4. Stay active and quote three markets per reveal
5. Finish by predicting the final true value on the last card

You will be asked to **quote prices** in the form:

BID-OFFER  (e.g., 24–25)

**QUICK DEFINITION** 

WHEN YOUR QUOTING
- The BID is what your willing to buy at.
- The OFFER is what your willing to sell at.

WHEN SOMEONE ELSE QUOTES
- The BID is what you can sell at.
- The OFFER is what you can buy at. 


### Correct Width

Certain clip sizes (10 lots, 20 lots, … up to 100 lots) have allowed bid-offer widths. Intuitively if you have more risk that you're market making on you need to widen your spread. 

**Spread** is the difference between your BID-OFFER (e.g. BID/OFFER = 24-25, spread = 1 point wide)

In this game the program has specific recommended spreads for lots quoted:
- 10 lots: spread must be exactly 1 point wide
- 20 lots: spread must be between 1 and 2 points wide
- 30 lots: spread must be between 2 and 3 points wide
- 40 lots: spread must be between 3 and 4 points wide
- 50–60 lots: spread must be between 4 and 5 points wide
- 70–80 lots: spread must be between 5 and 6 points wide
- 90–100 lots: spread must be between 5 and 7 points wide

### EV Must Lie Inside Your Quote

You must quote around the fair value, not away from it.

### Skew Based on Position

Your “position” changes each round.

Long (positive) → you want to sell → your ask should be relatively more attractive to your BID against the EV (i.e. higher)

Short (negative) → you want to buy → your bid should be relatively more attractive to your OFFER against the EV. (i.e. lower)

Flat (zero) → your bid and ask should be roughly balanced around EV

The program checks these conditions automatically and gives live feedback.

EXAMPLE SKEW:

**QUICK DEFINTITION:** Lots is a fictional unit of the asset you are market-making on. e.g. if it was equities --> lots = a single stock)

You have a long position of +30 lots and the **EV is 20**.
You are asked to quote 10 lots.

From the width rules, for 10 lots you must quote 1 point wide.
So a natural question is: Do you quote 19–20 or 20–21?

Because you are long, you want people to buy from you (so you can reduce your position). That means:
Your offer should be attractive (close to or below EV).
Your bid should be less attractive (further from EV), so people are not incentivised to sell to you.
So you **should quote 19–20**, not 20–21.

At 19–20,
EV = 20

Bid = 19 → EV − bid = 1
Offer = 20 → offer − EV = 0

Here, EV − bid > offer − EV, which matches the rule for being long:
the offer (20) is closer to EV than the bid (19), so players are more likely to buy from you at 20 than to sell to you at 19.
If you instead quoted 20–21, Bid = 20, Offer = 21 EV − bid = 0, offer − EV = 1. Now your bid is closer to EV than your offer, which is the behaviour of a short position (you’d be encouraging people to sell to you, which is the opposite of what you want when you’re long).


