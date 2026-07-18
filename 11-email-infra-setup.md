# Email Sending Infrastructure

## Step 1: Choose Your Sending Domain

Don't send from Gmail/Outlook — use a domain you own (yourbusiness.com).

- [ ] Buy a domain (or use existing)
- [ ] Create a subdomain for sending: `mail.yourbusiness.com` or `outreach.yourbusiness.com`

## Step 2: Email Service Provider (ESP)

Pick one:

| Tool | Cost | Best For |
|---|---|---|
| **Instantly** | $97/mo (starter) | Outreach at scale, built-in warmup |
| **Smartlead** | $39/mo | Multi-channel sequences, reasonable scale |
| **Apollo.io** | $99/mo | All-in-one: leads + email + sequences |
| **Mailshake** | $59/mo | Simple cold email campaigns |

## Step 3: Warmup (Critical)

Do NOT send cold emails from a fresh inbox — they'll go to spam.

- [ ] Use Instantly Warmup or Smartlead Warmup
- [ ] Warm for 2 weeks before first campaign
- [ ] Start at 2 emails/day, ramp to 20-30/day

## Step 4: DNS Setup

Add these records to your domain DNS:

```
Type  | Name                  | Value
TXT   | mail.yourdomain.com   | v=spf1 include:spf.[esp].com ~all
DKIM  | mail._domainkey       | [provided by your ESP]
MX    | mail.yourdomain.com   | [provided by your ESP]
```

## Step 5: Sending Limits

| Domain Age | Daily Limit | Per Inbox |
|---|---|---|
| New (< 30 days) | 10-20 emails/day | 1 inbox |
| 30-90 days | 30-50 emails/day | 2-3 inboxes |
| 90+ days | 50-100 emails/day | 3-5+ inboxes |

## Step 6: First Campaign Setup

- [ ] Upload prospects (from lead list CSV)
- [ ] Create sequence: Email 1 → 2-day gap → Email 2 → 3-day gap → Email 3 → 5-day gap → Email 4 → 7-day gap → Breakup
- [ ] Track opens/replies/clicks
- [ ] Pause for any reply
