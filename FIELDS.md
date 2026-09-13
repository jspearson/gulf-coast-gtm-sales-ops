# Fields

## Already on Opportunity

Region, Segment, Product Line, Forecast Risk, Next Step Last Updated, Quote Sent Date, Primary Quote Amount, Competitors.

Formulas: Days Open, Days Past Close, Has Next Step, Quote to Close Days, Is Stale.

## Worth adding next

| Thing | Why it matters |
|---|---|
| Tasks / emails / calls on the opp | Gives you Last Activity Date and “no touch in 14 days” |
| Notes (Content Note or Chatter) | Short context when a deal goes quiet |
| Loss Reason | Win/loss without guessing |
| Original Close Date + push count | Shows how often dates slip |
| Disqualified reason on Lead | Keeps the funnel honest |

## How email history usually works in Salesforce

Logged emails are Tasks (often TaskSubtype = Email) or EmailMessage. Call notes are Tasks. Longer writeups are Content Notes linked to the opportunity. I wouldn’t invent a custom “Email History” object unless the story is an integration.

## Stuck opps

Open opportunity where Close Date is today or earlier. Pair with Is Stale and blank Next Step on the hygiene board.
