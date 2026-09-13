# Common fields worth adding next

## Already in this org (Opportunity)
Region, Segment, Product Line, Forecast Risk, Next Step Last Updated, Quote Sent Date, Primary Quote Amount, Competitors, Days Open, Days Past Close, Has Next Step, Quote to Close Days, Is Stale

## High-value next (Director / RevOps)
| Field / object | Why |
|---|---|
| **Tasks / Emails / Events** on Opp | Real “motion”; powers LastActivityDate + stuck-without-touch reports |
| **Content Note** or Chatter | Qualitative context (“champion went dark”) |
| **Loss_Reason__c** (picklist) | Win/loss analysis |
| **Original_Close_Date__c** + Push_Count__c | Forecast integrity / sandbagging |
| **Next_Step_Owner__c** | Accountability |
| **MEDDICC-lite** (Champion, Economic Buyer checkboxes) | Enterprise motion without full methodology bloat |
| **Lead.Disqualified_Reason__c** | Funnel honesty |
| Standard **Forecast Category** discipline | Align with how AEs commit |

## Emails / notes — how Salesforce stores them
- Logged emails are usually **Tasks** (TaskSubtype = Email) or **EmailMessage** (Email-to-Salesforce)
- Call notes → Task
- Longer narrative → **ContentNote** linked to Opp, or Chatter post
- Don’t invent a custom “Email History” object unless you’re showing integration architecture

## Stuck definition used here
Open opportunity where **CloseDate ≤ TODAY** (includes today). Pair with Is_Stale__c and missing Next Step for the hygiene board.
