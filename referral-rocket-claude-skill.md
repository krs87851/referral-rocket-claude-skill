# Referral Rocket — Complete Platform Knowledge File

Upload this file to a Claude Project (claude.ai → Projects → Add knowledge) to get expert help with Referral Rocket. This file covers everything: getting started, campaign setup, rewards, integrations, widgets, account settings, and more.

**Website:** https://referralrocket.io  
**App:** https://app.referralrocket.io  
**Docs:** https://referral-rocket.gitbook.io/docs  
**Support:** support@referralrocket.io  

---

## What is Referral Rocket?

Referral Rocket is referral and affiliate marketing software for businesses. It lets you launch, manage, and track referral and affiliate programs — from simple "refer a friend" campaigns to multi-level affiliate networks. Participants share unique referral links; when their referred friends convert, Referral Rocket tracks the conversion and tells you who to reward.

**Best suited for:**
- E-commerce / Shopify stores
- SaaS / subscription businesses
- Newsletters and media publications
- Service businesses and agencies
- Startups pursuing rapid customer growth

---

## Pricing Plans

Pricing varies by region (USD for most countries, INR for India):

| Plan | Price (USD) | Price (INR) | Campaigns | Affiliates/Referrers | Referrals | Team Members |
|---|---|---|---|---|---|---|
| **Starter** | Free | Free | 1 | 5 | 100 | 1 |
| **Basic** | $19/mo | ₹1,499/mo | 3 | 50 | 1,000 | 3 |
| **Pro** | $39/mo | ₹2,499/mo | 10 | 250 | 10,000 | 10 |
| **Enterprise** | $99/mo | ₹4,999/mo | Unlimited | Unlimited | Unlimited | Unlimited |

**All plans include:** No transaction fees, dashboards, hosting, fraud detection, email notifications, affiliate hub/portal, Stripe integration, Tremendous integration, Cashfree integration, Razorpay integration, PayPal & Wise mass payouts, JavaScript SDK, chat & email support.

**Basic adds:** Priority & video support, access control, customizable design.

**Pro adds:** Custom email domain (custom SMTP), auto reward, REST APIs, white label (remove Referral Rocket branding), full widget customization suite.

Basic and Pro offer a 15-day free trial.

---

## Getting Started (5 Steps)

### Step 1 — Sign Up
Create an account at https://app.referralrocket.io. No credit card required for the free tier.

### Step 2 — Create a Campaign
From the dashboard click **New Campaign**. The campaign creation wizard walks you through up to 9 steps depending on campaign type:

| Step | Page | Shown for |
|---|---|---|
| Campaign Type | 0 | All |
| Campaign Sub-Type | 1 | Refer-a-Friend only |
| Campaign Info | 2 | All |
| Milestone Info | 3 | Milestone, Newsletter, Leadership Board only |
| Rewards Info (Join widget) | 4 | All |
| Share Info (Share widget) | 5 | All |
| Invitee Info | 6 | All |
| Invitee Complete | 7 | Only if Redirect = Yes |
| Affiliate Approval | 8 | Affiliate with manual approval only |
| Program Info (Save) | 9 | All |

**Campaign type cannot be changed after the campaign is saved.**

### Step 3 — Set Up Integrations (Optional)
Connect a payment or platform integration on the **Integration** tab so purchases and signups automatically trigger reward qualification. Without an integration you can qualify referrals manually or via the API.

### Step 4 — Install & Promote
Choose how to deploy (see Installation section). Share your campaign link, embed a widget on your website, or integrate the SDK into your app.

### Step 5 — Manage Rewards
When a referred user completes the qualifying event, the referring participant appears in **Rewards Due**. Pay them out via a connected payout integration or manually mark rewards as paid.

---

## Campaign Types

You choose the campaign type when creating a campaign. **This cannot be changed after the campaign is saved.**

### 1. Refer a Friend
Existing customers invite friends to purchase or sign up.

**Subtypes (chosen on step 1):**
- **Single-sided** — only the referrer receives a reward (e.g., "Refer a friend, earn $20")
- **Double-sided** — both referrer and referee receive rewards (e.g., "Give $20, Get $20")

Best for: e-commerce, SaaS, any product where existing customers bring in paying users.

### 2. Affiliate Program
Third-party publishers, creators, and partners earn commissions for driving sales or signups.

Key affiliate-specific features:
- **Lifetime commission** — affiliate earns on every future purchase by their referred users (required for tiered rewards and MLM)
- **Maximum commissions per referral** — cap the number of payments per referred user (options: 1, 2, 3, 6, 9, 12)
- **Maximum commission period** — limit the earning window in months (options: 1, 2, 3, 6, 9, 12, 18, 24, 36 months)
- **Tiered rewards** — escalating commissions based on referral count, time active, or total revenue (up to 5 tiers; Lifetime commission only; mutually exclusive with MLM)
- **Multi-Level Marketing (MLM)** — earn commissions from affiliates you recruit, up to 5 levels deep (Lifetime commission only; mutually exclusive with tiered rewards)
- **Network coupon** — give affiliates a discount code to share (creates double-sided setup)
- **Welcome bonus** — one-time bonus paid when an affiliate joins
- **Auto approve** — toggle whether new affiliates are approved instantly or require manual approval
- **Creative assets link** — Google Drive or Dropbox link for affiliates to download promotional materials
- **Cookie duration** — 30, 60, 90, or 180 days (default: 60 days)
- **Cookie win model** — Last referrer (fixed, not configurable)
- **W-9 collection** — require affiliates to submit a W-9 form before accessing their referral link
- **Approval widget** — shown to affiliates pending manual approval; customizable message (max 255 characters)

Best for: content creators, media partners, B2B referral networks.

### 3. Newsletter Referral
Current subscribers earn rewards for referring new subscribers. Uses milestone-style progression.

Best for: newsletters, media publications, Ghost blogs.

### 4. Milestone Giveaways
Participants unlock rewards when they hit specific referral thresholds. Each milestone has its own reward.

Best for: product launches, waitlists, pre-launch campaigns.

### 5. Leaderboard Program
Participants are ranked by referral volume on a live leaderboard. Top performers win prizes. Ranking can be by Total Referrals, Total Successful Referrals, or Total Revenue.

Best for: short-term contests, giveaways, competitions.

### 6. Shopify
Purpose-built for Shopify stores. Always self-hosted. Always double-sided by default. Shopify integration handles tracking and reward distribution automatically.

Best for: Shopify merchants wanting a plug-and-play referral program.

---

## Campaign Setup — Step by Step

### Step 2: Campaign Info

All campaign types:
- **Campaign name** — required
- **Does this campaign expire?** Yes/No; if Yes, date picker (minimum today)
- **Where will affiliates/users join?**
  - **Via My Website** (`self_hosted`) — you host the join page; requires a Share URL
  - **Via Referral Rocket** (`referral_rocket_hosted`) — Referral Rocket hosts the page; not available for Shopify
- **Share URL** (when self-hosted) — http/https prefix + URL input; required; Referral Rocket appends `?referralCode=XXXXX` automatically
- **Is the above URL where users sign up?** Yes/No — required when self-hosted; not shown for Shopify

Affiliate-specific additional fields:
- **Auto approve affiliates?** Yes/No (default: Yes)
- **Creative assets link** — URL to your Google Drive or Dropbox folder
- **Cookie Duration** — dropdown: 30, 60, 90, 180 Days (default: 60)
- **Cookie Win Model** — read-only, always "Last referrer"

Shopify campaigns automatically set self_hosted = true and signupUrlFlag = true (not configurable).

---

### Step 4: Rewards Info (Join Widget)

This step has three collapsible sections: **Program Details**, **Reward Details**, and **Form**.

#### Program Details Section

- **Program title** — heading displayed in the join widget
- **Program subtitle** — description; max 255 characters
- For **affiliate and refer-a-friend** only:
  - **Program details** — rich text (Quill editor), max 1000 characters, Show/Hide toggle
  - **Reward info** — rich text, max 1000 characters, Show/Hide toggle
  - **Program terms** — rich text, max 1000 characters, Show/Hide toggle
  - **Important:** if Show is enabled but the content is empty, a red border warning appears and you cannot proceed

#### Reward Details Section

**"Set Affiliate/Referrer Reward" button** — opens the reward configuration modal (see Reward Configuration section for all modal fields).

**"Set Referee Reward" button** — appears for refer-a-friend (double-sided) and Shopify campaigns.

**Affiliate Welcome Bonus Value** — number input, minimum 0, default 0. One-time bonus paid when an affiliate joins.

**Recurring commission** (affiliate only):
- **Life-time** (`no_limit`) — affiliate earns on every qualifying purchase indefinitely. Required for tiered rewards or MLM.
- **Set maximum commissions per referral** (`payment_limit`) — dropdown: 1, 2, 3, 6, 9, 12 payments
- **Set maximum commissions period** (`month_limit`) — dropdown: 1, 2, 3, 6, 9, 12, 18, 24, 36 months

**Enable Tiered Reward** checkbox — only appears when Recurring = Life-time. Enabling it disables MLM (mutually exclusive). See full Tiered Rewards section below.

**Enable Multi-Level Marketing** checkbox — only appears when Recurring = Life-time. Enabling it disables tiered rewards (mutually exclusive). See full MLM section below.

**Enable Club Reward** checkbox (affiliate/refer-a-friend/Shopify) — when enabled, all rewards for a referred user go to the first referrer, even if another referrer later claimed credit.

**Limit on referrals** checkbox — if enabled, number input to cap the maximum qualifying referrals per participant.

**Network coupon toggle** (affiliate only) — "Create a coupon/discount code affiliate can share with their network." When enabled, the "Set Network Coupon" button appears (opens the referee reward modal). This sets the campaign subtype to double-sided.

#### Form Section

- **Terms and conditions** checkbox → URL input (must be http/https)
- **Hide First Name** checkbox
- **Hide Last Name** checkbox
- **Collect phone number** checkbox
- **Button text** — max 30 characters, default "Submit" (live character counter shown)
- **Collect W9** toggle (affiliate only) — requires affiliates to submit a W-9 before accessing their referral link. If your Payer Information is not filled in, a warning with a link to fill it is shown.

---

### Step 5: Share Info (Share Widget)

- **Share widget title** — text input
- **Share widget subtitle** — max 255 characters. Hint: use `$referrerCode` to insert the affiliate's actual code.

Customization sub-section (collapsible):
- **Show affiliate/referrer portal sign-up link?** Yes/No (default: Yes for affiliate, No for others)
- **Share Option** — multi-select: Instagram, WhatsApp, X (Twitter), Facebook, LinkedIn, Mail
- **WhatsApp message** — max 250 characters (shown when WhatsApp is enabled)
- **LinkedIn message** — max 250 characters (shown when LinkedIn is enabled)

---

### Step 6: Invitee Info (Invitee Widget)

- **Invitee header** — default: "You've been referred by $referrerFirstName"
  - Supported variables: `$referrerFirstName`, `$referrerLastName`, `$referrerCode`, `$referrerEmail`
- **Invitee description** — max 255 characters; same variables available
- **Redirect to your sign-up page?** Yes/No
  - If Yes: http/https prefix + URL input
  - Redirect URL supports variables: `$refereeFirstName`, `$refereeLastName`, `$refereeEmail`, `$referrerCode`

Form sub-section (collapsible):
- **Collect phone number** checkbox
- **Hide First Name** checkbox
- **Hide Last Name** checkbox
- **Button text** — max 30 characters, default "Continue"

---

### Step 8: Affiliate Approval Widget (Affiliate campaigns, manual approval only)

- **Approval message** — max 255 characters. Default: "Thank you for submitting an application. You will receive an email once your affiliate application has been reviewed."

---

## Reward Configuration (The Modal)

Clicking **"Set Affiliate/Referrer Reward"**, **"Set Referee Reward"**, or **"Set Network Coupon"** opens the reward configuration modal.

### Reward Type (radio buttons)
- **Monetary** — fixed cash amount (e.g., $20.00). Minimum value: 1.
- **Percentage** — percentage of sale value (e.g., 10%). Must be less than 100 (maximum: 99). Cannot be 100 or above.

### Reward Currency
Currency selector. Multi-currency supported. For Shopify campaigns, use your store's currency.

### Issue Reward As (Coupon or Credit)
- **Coupon** — generates a coupon/discount code with an optional expiry
- **Credit** — tracked in Referral Rocket; paid out via manual or integration payout

**This selector is hidden (forced to Credit) when:**
- Tiered rewards are enabled
- MLM is enabled
- Campaign type is Shopify

So: enabling tiers or MLM forces the payout method to Credit, but it does **not** change your Percentage or Monetary reward type. You can still have a 10% tiered commission — the % values in each tier are set by you.

### Reward Valid For (months)
Appears when Issue Reward As = Coupon, or for referee in affiliate campaigns.
Options: 1, 3, 6, 9, 12, 18, 24 months, or **Forever** (value: 999).
"Forever" is only available when Reward Type = Percentage.

---

## Tiered Rewards — Complete Guide

Tiered rewards let you escalate an affiliate's commission rate based on performance milestones.

**Prerequisites:**
1. Campaign type must be **Affiliate**
2. Recurring commission must be set to **Life-time**
3. MLM must be **disabled** (tiers and MLM are mutually exclusive — enabling one turns off the other)

**What enabling tiers does automatically:**
- Forces "Issue Reward As" to **Credit** (the selector is hidden)
- Creates one default starting tier (threshold = 3, reward = your current reward value)
- The reward TYPE (Percentage or Monetary) you set in "Set Affiliate Reward" is preserved and determines the suffix (% or currency) shown in each tier's Reward field

### Tiered Reward Type Options

| Option | Label in UI | Threshold Unit |
|---|---|---|
| `referral_based` | Number of Successful Referrals | Referrals |
| `time_based` | Time Based | Months |
| `revenue_based` | Total Revenue Based | Currency (e.g., $) |

### Tier Card Fields

Each tier shows:
- **Reward** — number input + suffix (% if Percentage type, currency symbol if Monetary)
- **From** — read-only; shows the previous tier's threshold (only shown for tiers after the first)
- **Upto** — number input + unit label (Months / Referrals / currency amount)
- **Last tier note:** "If an affiliate exceeds [threshold] [unit], they will be awarded [reward][suffix]" — this confirms the last tier is the permanent fallback once the highest threshold is exceeded

### Adding and Removing Tiers
- **Maximum 5 tiers**. The + button is hidden once you have 5.
- **Only the last tier can be removed** (trash icon only on the last card)
- **Default for new tiers:** threshold = previous tier's threshold + 3, reward = previous tier's reward

### Tier Validation Rules
- Each tier must have reward > 0 and threshold > 0
- Thresholds must be strictly ascending (each must be greater than the previous)
- At least 1 tier is required

### How the Tier Calculation Works (Time-Based — Exact Server Logic)

The server calculates which tier applies at commission time using:

```
months = ChronoUnit.MONTHS.between(affiliate.joinDate, today)
achieved = months + 1
```

It then checks tiers in order: a tier matches when `previousThreshold < achieved ≤ tierThreshold`.

If `achieved` exceeds ALL tier thresholds, the **last tier's reward is used** as a permanent fallback.

**What "active" means:** `joinDate` = the date the affiliate joined (submitted their application), **not** the approval date. Time counts from join, even if they were pending approval for a while.

**Practical example for 10% before 12 months → 20% at and after 12 months:**

| State | months value | achieved value | Which tier matches |
|---|---|---|---|
| Just joined | 0 | 1 | Tier 1 (1 ≤ 12) → 10% |
| 11 months in | 11 | 12 | Tier 1 (12 ≤ 12) → 10% |
| Exactly 12 complete months | 12 | 13 | No tier matches (13 > 12); falls to last tier → 20% |
| 24 months in | 24 | 25 | Exceeds last tier; fallback → 20% |

**20% starts after 12 complete calendar months have elapsed — i.e., from the beginning of month 13.**

### Step-by-Step: Set Up 10% → 20% at 12 Months

1. Create or edit an **Affiliate Program** campaign
2. In Rewards Info (Step 4), set Recurring commission to **Life-time**
3. Click **"Set Affiliate Reward"**
   - Set Reward Type to **Percentage**
   - Set a starting value (e.g., 10)
   - Leave Issue Reward As as Credit (or Coupon; it will be forced to Credit anyway once tiers are enabled)
   - Save/confirm the modal
4. Check **"Enable Tiered Reward"** — the initial tier is created with threshold = 3, reward = 10
5. Set Tiered Reward Type to **"Time Based"**
6. Edit Tier 1: set **Upto = 12** Months, **Reward = 10** %
7. Click **+** to add Tier 2: set **Upto = 999** Months (or any number greater than 12), **Reward = 20** %
8. The last tier card will confirm: "If an affiliate exceeds 999 Months, they will be awarded 20%"
9. Continue and save the campaign

**Note on past sales:** When a commission is processed, the tier active at that moment applies. Existing past commissions that have already been issued are NOT retroactively changed — the new rate applies to new qualifying transactions going forward.

---

## Multi-Level Marketing (MLM) — Complete Guide

MLM lets affiliates earn commissions from affiliates they recruit, up to 5 levels deep.

**Prerequisites:**
1. Campaign type must be **Affiliate**
2. Recurring commission must be **Life-time**
3. Tiered rewards must be **disabled** (MLM and tiers are mutually exclusive)

**What enabling MLM does:**
- Forces "Issue Reward As" to **Credit**
- Disables tiered rewards

### MLM Level Cards
- **Reward** field — number input + suffix (% if Percentage, currency if Monetary)
- Levels are ordered by position (Level 1, Level 2, etc.)
- Maximum 5 levels; + button hidden at 5
- Only the last level can be removed

### MLM Reward Calculation Type
Only shown when Reward Type = Percentage:
- **Total Sales** (`total_payment`) — each level's percentage is applied to the total sale amount
- **Program Commission** (`program_commission`) — each level's percentage is applied to the previous level's commission

For Monetary type, this field is not shown (not relevant).

### Validation
- Each level must have reward > 0
- If Reward Type = Percentage and MLM is enabled, Calculation Type must be selected

---

## Widgets — What They Are

Referral Rocket uses four distinct widgets:

### 1. Join Widget
Shown to people coming to sign up / join the program. Contains: program title, subtitle, signup form (name, email, phone if enabled), and the join button. Also displays program details, reward info, and terms if configured and shown.

### 2. Share Widget
Shown to participants after they've joined. Displays their unique referral link, social sharing buttons, and copy options. For affiliate campaigns, also shows their commission details.

### 3. Invitee Widget
Shown to people who click a referral link before signing up. Presents the offer to the referred friend. If redirect is configured, clicking the CTA button sends them to your sign-up page (with optional pre-filled data via URL variables).

### 4. Approval Widget
Shown to affiliates whose application is pending manual approval. Displays a customizable message explaining what to expect.

---

## Widget Customization

Widget customization is split into two tiers:

**Available on ALL plans (Branding section):**
- Logo upload (company logo)

**Available on Pro plan and above (tier 2+) only:**
Full customization suite (tiers 0 and 1 see a locked/greyed-out preview):
- Company image upload
- Company background image upload
- **Label Language** — changes the language of all widget UI labels (not content you write). 15 supported languages: English, Hindi, Spanish, French, German, Italian, Portuguese, Russian, Chinese, Japanese, Korean, Arabic, Turkish, Dutch, Polish. This translates labels like "Submit", "Copy", "Sign Up", "Terms and Conditions", etc.
- **White label** — removes "Powered by Referral Rocket" branding (requires Pro/Enterprise — tier 2+)

**Layout & Colors (Pro+):**
- Page background color — toggle on/off + hex color picker
- Widget background color — toggle + color picker
- Box shadow — toggle
- Widget alignment (vertical)
- Border radius — +/− controls (px)
- Widget width — +/− controls (px)
  - Join widget minimum: 600px standard; 700px for affiliate or ≤3 milestones; 1000px for 4–5 milestones
  - Share widget minimum: 700px; 1000px for 4–5 milestones

**Typography (Pro+):**
For Header, Description, and Sign Up Link (when showSignUp=Yes):
- Font family dropdown
- Font size dropdown
- Bold / italic / underline
- Text alignment
- Color picker

**Fields (Pro+):**
- Field text color — color picker
- Field background color — color picker

**Buttons (Pro+):**
- Button text: font family, size, bold/italic/underline
- Button radius — +/− controls
- Button color — color picker

**Affiliate Program Details section (affiliate campaigns, Pro+):**
- Header: font family, size, bold/italic/underline, color
- Text: font family, color

**Share widget specific (Pro+):**
- Reward Progress Customization
- Referrals List Customization
- Leadership Progress Customization (leadership board campaigns only)

**Invitee widget specific (Pro+):**
- Invitee Image Upload

**Milestone Customization (Pro+):**
Available for milestone/newsletter/leadership board campaigns only.

---

## Integrations (Campaign-Level)

Set up from the **Integration** tab on each campaign.

### Stripe
- Connect via OAuth (redirects to Stripe)
- Supports live mode and test mode
- Automatically qualifies referrals when a Stripe payment is received
- Also used to issue coupon/discount codes as payout

### Shopify
- Connect via OAuth — enter your store domain in the format `storename.myshopify.com`
- Automatically qualifies referrals and distributes rewards (gift cards, discount codes)

### Cashfree
- Provide your **API Secret Key** from Cashfree
- Add the webhook URL in your Cashfree dashboard:  
  `https://app.referralrocket.io/api/public/cashfree/webhook`
- Automatically qualifies referrals on successful payments

### Razorpay
- Provide your **Webhook Secret Key** and **Account ID**
- Add the webhook URL in your Razorpay dashboard:  
  `https://app.referralrocket.io/api/public/razorpay/webhook`
- **RazorpayX (optional payout):** additionally provide Customer Identifier, API Key ID, and API Secret Key to enable automated payouts via RazorpayX

### Tremendous
- Provide your **API Key** (click Validate to verify)
- Toggle **Test Mode** for sandbox payouts
- Select a **Campaign Template** from your Tremendous account
- Displays your available Tremendous balance
- Used to send gift cards, Visa cards, ACH, and PayPal to 100+ countries

### Ghost
- Provide your **Webhook Secret Key** from Ghost
- Add the webhook URL in your Ghost settings:  
  `https://app.referralrocket.io/api/public/ghost/webhook`
- Optional: **Qualify on signup** — automatically qualify referrals when the referred user signs up (not on payment)

### PayPal
- Provide your **Client ID** and **Client Secret**
- Toggle **Test Mode** for sandbox payouts
- Used for mass payouts to affiliates

---

## Payout Methods

Referral Rocket does not fund rewards. You distribute them via:

| Method | Description |
|---|---|
| **Stripe** | Issue coupons/discount codes directly in Stripe |
| **Shopify** | Issue gift cards or discount codes to Shopify customers |
| **Tremendous** | Send gift cards (2,000+ options), Visa cards, ACH, PayPal to 100+ countries |
| **PayPal Mass Payments** | Download participant list, process bulk payouts via PayPal |
| **Wise Batch Payments** | Download participant list, process bulk payouts via Wise |
| **RazorPayX** | Payout via RazorPayX (India) — requires Customer Identifier, API Key ID, API Secret Key |
| **Manual** | Issue rewards outside the platform; mark as paid in Referral Rocket |

---

## Reward Statuses

Rewards move through these statuses:
- **Due** — earned, not yet paid
- **Paid** — marked as paid
- **Ignored** — manually ignored (skipped)
- **Refunded** — reversed/refunded

---

## How Referrals Qualify for a Reward

A participant appears in **Rewards Due** when their qualifying event is marked complete. This happens three ways:
1. **Manual** — navigate to Participant Details and mark the qualifying event complete
2. **API** — your backend calls the Referral Rocket API when the qualifying event (purchase, signup) occurs
3. **Automated integration** — Stripe, Shopify, Cashfree, Razorpay, or Ghost automatically notifies Referral Rocket when a transaction or signup is completed

---

## Installation Options

### Option 1 — Hosted Campaign Page (No Code)
Share a Referral Rocket-hosted URL. No code required.

```
https://referralrocket.io/campaign?id=YOUR-CAMPAIGN-ID
```

A QR code is also generated and downloadable from the campaign's **Install** tab.

Best for: fastest launch, non-technical teams, any campaign type.

### Option 2 — Redirect to Hosted Page
Build your own marketing page. Add a button that redirects to the Referral Rocket hosted URL.

Best for: affiliate programs with branded recruitment pages.

### Option 3 — Embed Widget on Your Website
Embed the widget directly on your site using a script tag.

**Add to `<head>`:**
```html
<script
  type="text/javascript"
  campaign-id="YOUR-CAMPAIGN-ID"
  defer
  src="https://app.referralrocket.io/widget/widgetIndex.js">
</script>
```

**Add where the widget should appear:**
```html
<div id="referral-rocket-widget"></div>
```

Verify installation: open browser console and type `window.Rocket`.

Best for: affiliate programs, marketing pages, higher conversion.

### Option 4 — In-App Integration (JavaScript SDK)

```javascript
// Get campaign info
window.Rocket.getCampaign().then(campaign => {
  console.log(campaign);
});

// Add a participant
window.Rocket.getCampaign().addParticipant({
  email: 'john@example.com',
  fName: 'John',
  lName: 'Smith',
  referredByCode: 'OPTIONAL_CODE'   // omit to auto-detect from cookie
});

// Get a participant's details
window.Rocket.getCampaign().getParticipant({
  email: 'john@example.com'
  // or: code: 'REFERRAL_CODE'
});

// Qualify a participant (triggers reward eligibility)
window.Rocket.getCampaign().qualifyParticipant({
  email: 'jane@example.com',
  amountPaid: 99.00,
  rewardReferee: false
});

// Get the referral code stored in the visitor's cookie
window.Rocket.getReferralCode();

// Check if a referral code is valid (returns boolean)
window.Rocket.validateCode('SOME_CODE');
```

For multiple campaigns on the same page, pass the campaign ID explicitly:
```javascript
window.Rocket.getCampaign('YOUR-CAMPAIGN-ID').addParticipant({...});
```

Best for: refer-a-friend programs inside a logged-in product.

### Option 5 — REST API (Fully Custom)
Build a completely custom flow using the Referral Rocket REST API.

API documentation: https://referral-rocket.gitbook.io/docs/developer-tools/rest-api

**Authentication:** API key — available on Pro plan. Manage API keys under Account → API Keys. Generating a new key immediately invalidates the old one.

Best for: mobile apps, headless builds, complex custom flows.

### Shopify Discount Modal (Shopify-Specific Install)
Add this script to show referred visitors a discount code popup at checkout:

```html
<script
  type="text/javascript"
  campaign-id="YOUR-CAMPAIGN-ID"
  defer
  src="https://app.referralrocket.io/widget/DiscountModal.js">
</script>
```

---

## Campaign Management

### Participants Tab
Shows everyone who has joined the campaign with status, referral count, and reward history. You can:
- View individual participant details
- See who each participant referred
- Manually mark qualifying events
- Add participants manually
- Export to Excel

### Affiliates Tab (Affiliate Campaigns)
Shows affiliate performance, pending applications (if manual approval is on), and commission earned. You can approve or reject pending affiliates.

### Rewards Section
- **Rewards Due** — earned but unpaid
- **Rewards Paid** — historical paid rewards
- **Rewards Ignored** — manually ignored rewards
- **Rewards Refunded** — reversed/refunded rewards

### Campaign Dashboard
Per-campaign analytics: clicks, joins, referrals, conversions, and reward totals.

### Campaign Assets (Creative Assets)
Upload and manage images and creative materials affiliates can download. Also set a link to an external asset folder.

### Pausing / Ending a Campaign
Campaigns can be paused at any time without losing data. Campaigns with an expiration date end automatically.

---

## Affiliate Program Hub (Marketplace)

### For Businesses: List Your Program
List on the Referral Rocket Affiliate Program Hub — a directory where affiliates can discover and apply. Configure from **Marketplace** in the app.

### For Businesses: Find Affiliates
Browse a database of affiliates and reach out directly (paid plans, feature activation required).

Affiliate performance badges:
- **Super Affiliate** — 1M+ reach
- **Top Affiliate** — 500K–1M reach
- **Strong Affiliate** — 100K–500K reach
- **Emerging Affiliate** — under 100K reach

Filter by: Category, Location, Badge level. Send invite emails directly (rate-limited: 30-day wait between invites; after 3 invites, the system suggests letting the affiliate come to you).

### For Affiliates: Set Up Your Profile
Set up a discoverable profile:
- Profile photo, bio, country/location
- Preferred categories (up to 10)
- Audience data: monthly website visitors, total followers, email subscribers
- Social media links: X/Twitter, Instagram, YouTube, LinkedIn, TikTok, up to 3 website URLs

---

## Email Notifications

Configure per-campaign from the **Email Notifications** tab. All emails have customizable subject lines and rich-text bodies (powered by ReactQuill). A **Test** button lets you send a test email.

### For You (Business Owner Notifications)

| Email | When Sent | Plan Restriction |
|---|---|---|
| New affiliate/referrer joins | Every time someone joins | All plans |
| A referral is made | When a participant refers someone | All plans |
| Participant eligible for reward | When a qualifying event is detected | All plans |
| Monthly reward report | First of each month | Basic+ (tier 1+) |

### For Affiliate / Referrer

| Email | When Sent | Notes |
|---|---|---|
| Affiliate is approved | When you manually approve | Manual approval only |
| Welcome email | When affiliate joins (auto-approve) | Auto-approve mode |
| Referrer earns a reward | When their referral qualifies | Non-affiliate campaigns only |
| Payout sent | When you mark a reward as paid | All campaigns |
| Share widget email | Allow participants to send referral emails | Toggle "include referee data" option available |

### For Referee (Referred User)

| Email | When Sent |
|---|---|
| Joined via referral link | When a referred user joins the program |

### Available Email Variables

| Variable | Description |
|---|---|
| `$firstName` | Participant's first name |
| `$lastName` | Participant's last name |
| `$email` | Participant's email |
| `$referralLink` | The participant's unique referral link |
| `$companyName` | Your company name |
| `$reward` | Reward value |
| `$totalRewardsDue` | Total rewards owed |
| `$totalRewards` | Total rewards earned all-time |
| `$friendName` | Name of the referred friend |
| `$referrerCode` | The referral code |
| `$month` | Current month (for monthly report email) |
| `$referrerFirstName` | Referrer's first name |
| `$referrerLastName` | Referrer's last name |
| `$referrerEmail` | Referrer's email |
| `$refereeFirstName` | Referee's first name |
| `$refereeLastName` | Referee's last name |
| `$refereeEmail` | Referee's email |

---

## Account Settings

### Team Management
Invite team members. Roles:
- **Admin** — full access
- **Editor** — can edit campaigns but not billing/account settings
- **Viewer** — read-only access

Team member limits: Starter: 1, Basic: 3, Pro: 10, Enterprise: Unlimited.

### API Keys (Pro Plan)
Under **Account → API Keys**. Generate, reveal, copy, and regenerate your API key. Regenerating immediately invalidates the previous key. Required for REST API access.

### Custom SMTP / Email Domain (Pro Plan)
Under **Account → Email Settings**. Configure your own SMTP server.

Required fields:
- From email address
- SMTP password
- SMTP server hostname
- Port

Click **Test Connection** to verify before saving.

### Webhooks (Account-Level)
Under **Account → Webhooks**. Add endpoints that receive event notifications for all campaigns in your account. You can add multiple endpoints, view event history, and edit existing webhooks.

Full webhook guide: https://referral-rocket.gitbook.io/docs/developer-tools/webhooks

### Payer Information (for 1099-NEC)
Under **Account → Payer Information**. Required before enabling W-9 collection.

Fields:
- Full name (business owner or company name)
- Telephone number
- TIN — SSN format `XXX-XX-XXXX` or EIN format `XX-XXXXXXX` (format validated, not IRS-verified)
- Street address, City, State, Country, ZIP code / foreign postal code

### Tax Documents (1099-NEC)
Under **Account → Tax Documents**. Download 1099-NEC Copy B forms for your affiliates.

Forms are auto-generated each January for the prior calendar year once paid rewards for an affiliate reach $600. Filter by tax year.

---

## Tax and Compliance (W-9 / 1099-NEC)

1. **Enable W-9 collection** on affiliate campaigns → affiliates must submit W-9 before accessing their referral link
2. **Configure Payer Information** in account settings with your business's legal name, TIN, and address
3. When total paid rewards to an affiliate reach **$600 in a calendar year**, Referral Rocket automatically generates a **1099-NEC Copy B** form in January of the following year
4. Affiliates download their form from their portal; you download from Account → Tax Documents

---

## Finding Your Campaign ID

Your Campaign ID is visible:
1. In the URL when viewing a campaign: `.../campaign/YOUR_CAMPAIGN_ID/...`
2. In campaign settings under **Campaign Details**
3. On the campaign **Install** tab

---

## Common Questions

**Do participants need to sign up for Referral Rocket separately?**
No. Participants sign up for *your* referral program through your widget or hosted page.

**Can I white-label the widget?**
Yes, on Pro plan (tier 2+). Toggle "Remove Referral Rocket branding" in widget customization.

**Do I need coding experience?**
No coding needed for the hosted campaign page (Option 1). Option 3 requires basic HTML. Options 4 and 5 require a developer.

**Does Referral Rocket fund the rewards?**
No. You fund and distribute rewards. Referral Rocket tracks who has earned what and helps you disburse.

**Can I reward both the referrer and the referred friend?**
Yes. Enable **double-sided** (refer-a-friend or Shopify) or use the Network Coupon toggle (affiliate).

**Can I limit how much a single person can earn?**
Yes. Toggle **Limit on referrer/affiliate referrals** to cap qualifying referrals per participant.

**How does cookie tracking work for affiliates?**
Cookie duration: 30, 60, 90, or 180 days (configurable). The **last referrer** gets credit if multiple affiliates refer the same person (Last Referrer win model, fixed).

**When does 20% start in a time-based tier with threshold = 12?**
After 12 complete calendar months from the affiliate's join date. At exactly 12 complete months (start of month 13), the system calculates achieved = 13, which exceeds tier 1's threshold of 12 and uses the next tier (20%).

**Does "active" mean from join date or approval date?**
Join date — the date they submitted their application to your affiliate program, regardless of when they were approved.

**Do existing paid commissions change when I update tiers?**
No. Already-issued commissions are not changed. The new tier rate applies to new qualifying transactions going forward.

**Can I use percentage-based tiers?**
Yes. Set Reward Type to Percentage in "Set Affiliate Reward" before enabling tiers. The tier cards will then show % as the reward suffix. The % symbol is based on the reward type you configured — it is NOT changed by enabling tiers.

**What is the difference between Credit and Coupon?**
Coupon = generates a discount/coupon code with an expiry (useful for Stripe/Shopify discounts). Credit = tracked in Referral Rocket and paid out via manual or integration payout. Tiers and MLM always use Credit.

**Can I run multiple campaigns simultaneously?**
Yes, up to your plan limit. Use `window.Rocket.getCampaign('campaign-id')` to target a specific campaign.

**What happens if an affiliate's referral exceeds the highest tier threshold?**
They earn the highest tier's reward permanently. The last tier is always the fallback.

**Can I collect phone numbers and hide name fields simultaneously?**
Yes, all form fields are independently configurable.

**How do I add participants who didn't use a referral link?**
Use the **Add Participant** button on the Participants tab.

**Is there a free trial for paid plans?**
Yes — Basic and Pro plans include a 15-day free trial.

**What social media platforms can participants share on?**
Instagram, WhatsApp (custom message), Twitter/X, Facebook, LinkedIn (custom message), and email/mail. Each platform can be individually enabled or disabled.

**What languages are supported for the widget UI?**
15 languages: English, Hindi, Spanish, French, German, Italian, Portuguese, Russian, Chinese, Japanese, Korean, Arabic, Turkish, Dutch, Polish.

**Where do I find the installation script?**
Navigate to your campaign → **Install** tab. The script tag is pre-filled with your Campaign ID.

**When are 1099-NEC forms generated?**
Automatically each January for the prior calendar year, for any affiliate who received $600 or more in paid rewards. Requires Payer Information in account settings and W-9 collection enabled on your campaign.

**What is the maximum percentage value I can set for a commission?**
99%. The system rejects values of 100 or above.

---

## Key URLs

| Resource | URL |
|---|---|
| App | https://app.referralrocket.io |
| Marketing site | https://referralrocket.io |
| Documentation | https://referral-rocket.gitbook.io/docs |
| Pricing | https://referralrocket.io/pricing |
| REST API docs | https://referral-rocket.gitbook.io/docs/developer-tools/rest-api |
| Webhooks docs | https://referral-rocket.gitbook.io/docs/developer-tools/webhooks |
| Shopify integration guide | https://referral-rocket.gitbook.io/docs/integrations/shopify |
| Referral program examples | https://referralrocket.io/referral-program-examples/refer-a-friend |
| Contact / support | support@referralrocket.io |
| Book a demo | https://referralrocket.io/book-a-demo |
