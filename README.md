# Net Revenue Test Planner

**Try it:** https://carlostorres-growth.github.io/net-revenue-test-planner/
Click "See an example" to see it work. Nothing you enter leaves your browser.

Plan and read A/B tests on net revenue per visitor, so a lift in conversions that later gets refunded doesn't count as a win.

## Why I built it

I designed a test for a DTC brand that had launched a "refund and keep the product" guarantee. Offers like this often raise conversion rate, but they also raise refunds, and refunds arrive weeks after the sale. A test judged on conversion rate, or read before the refund window closes, can declare a winner that actually loses money.

The fix was to judge the test on net revenue per visitor (revenue minus refunds, divided by everyone who saw the page) and to wait for refunds before deciding. This tool turns that method into something any team can use.

## What it does

**1. Plan the test.** Enter your traffic, conversion rate, order value and refund rates, now and with the new offer. It shows:
- the **break-even lift**: how much better the new offer must convert just to cover its extra refunds
- the expected net revenue per visitor for each version
- how many visitors each version needs, how many full weeks to run, and when to read the result once refunds have come in

**2. Read the results.** Enter visitors, orders, revenue and refunds for each version. It compares revenue per visitor before and after refunds and gives a plain verdict:
- B wins / B loses (on net revenue per visitor)
- B converts better, but refunds wipe out the gain
- Not enough data yet

It also warns you if the refund window hasn't closed, since the result can still change.

## How it works

- Each visitor's net revenue is zero if they don't buy, or the order value if they buy and keep it. The tool estimates the spread of that number from conversion rate, order value, order value spread and refund rate.
- Sample size uses a standard two-sample test on net revenue per visitor, at the confidence and power you choose.
- Tests run in full weeks (at least two) so every weekday is covered equally.
- Runs entirely in the browser. No data is stored or sent anywhere.

## Limitations

- Results use an estimate of how much order values vary, not order-level data. For a final decision on a large test, check the result with order-level data.
- Each refund is treated as a full refund.

## Built with

HTML, CSS and JavaScript. Built with Claude as a coding assistant.
