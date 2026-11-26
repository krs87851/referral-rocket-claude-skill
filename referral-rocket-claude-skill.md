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

**Basic adds:** Priority & video support, access control, customizable design. Also unlocks: min payment count per referral (Stripe), assign reward to referee via integration.

**Pro adds:** Custom email domain (custom SMTP), auto reward, REST APIs, white label (remove Referral Rocket branding), full widget customization suite, creative assets upload, webhooks detail view.

Basic and Pro offer a 15-day free trial.

Internal tier numbers: Starter = 0, Basic = 1, Pro = 2, Enterprise = 3+. Feature gates use `company.tier >= N`.

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

## Widgets — What They Are and How They Work

Referral Rocket uses four distinct widgets, each is a separate UI state:

### 1. Join Widget
Shown to people coming to sign up / join the program. Contains: program logo, invitee header/desc (when someone arrives via a referral link with variable substitution: `$referrerFirstName`, `$referrerLastName`, `$referrerCode`, `$referrerEmail`) or program title/subtitle, signup form (first name, last name optional/hideable; email required; phone with international country selector optional), terms checkbox, and join button.

After joining:
- If affiliate + manual approval required: transitions to "pause" (approval widget)
- If W-9 required but not submitted: transitions to "pause" (W-9 message with Login button)
- If invitee flow with redirect configured: `window.location.href` to redirect URL with variable substitution

Widget reads participant data from div element attributes: `email`, `first-name`, `last-name` — if present, the form fields are pre-populated and may be hidden.

### 2. Share Widget
Shown to participants after they've joined. Displays their unique referral URL in a copy-able input. Social icons shown unless disabled in campaign settings (Facebook, WhatsApp, X/Twitter, Instagram, LinkedIn, Mail — the campaign field is set to `true` to HIDE that icon, so they're shown by default).

Additional elements:
- **WhatsApp** link uses the `whatsappMessage` campaign field
- **LinkedIn** uses a generated share URL
- **Mail**: if `shareWidgetEmail` is configured, opens SendMailModal with customizable template + subject; otherwise opens native `mailto:` link
- **RewardDetails** (non-leadership campaigns) or **LeadershipProgressDetails** (leadership board)
- **MilestoneInfo** for milestone/newsletter/leadership campaigns
- **ReferralsList** when `showReferralsList = true`
- **Sign-up link** when `showSignUp === 'yes'` or affiliate campaign where showSignUp is not 'no'

Widget caches participant state in `localStorage` using campaignId as key. Refreshes after 60 days for non-affiliate campaigns. For affiliate with manual approval, re-fetches on every load.

### 3. Invitee / Pause Widget
Used for two distinct states:
- **Campaign ended/paused/deleted**: shows `infoMessage`
- **Affiliate pending approval**: shows `approvalMessage`
- **W-9 not submitted**: shows W-9 message with a Login button (links to `app.referralrocket.io`)
- **Invitee completion** (invitee flow, campaign active): shows completion message
  - If `wantRedirect === "yes"` + campaign active: shows Continue button linking to redirect URL with variables

### 4. Shopify Discount Popup
A special popup for Shopify campaigns only. Configured via HTML attributes on the script tag, NOT in the campaign settings. Script attributes:
- `campaign-id` — required
- `background-color` — popup background color
- `button-color` — button color
- `popup-header` — custom header text (if omitted, auto-generates "Here's a {reward} discount" from campaign data)
- `button-value` — text on the "Shop Now" button

Triggered **only** when `?referralCode=` is in the URL. Shows the referral code (which IS the discount code for Shopify) + Copy button + "Shop Now" button (which removes `referralCode` from the URL and redirects to the store).

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

The 16 available font families: Arial, Calibri, Cursive, Courier New, Comic Sans MS, Georgia, Helvetica, Impact, Lucida Sans Unicode, Roboto, System Default (system-ui), Times, Times New Roman, Tahoma, Trebuchet MS, Verdana.

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

Set up from the **Integration** tab on each campaign. Connected integrations are displayed with a green "Connected" badge; disconnected show "Not Connected". Connected integrations can be **Edited** (non-Stripe/Shopify), **Disconnected**, or **Managed** (settings).

### Stripe
- Connect via OAuth (redirects to Stripe)
- Supports **live mode** and **test mode** (a "TEST" badge shows when test mode is active)
- Automatically qualifies referrals when a Stripe payment is received
- Also used to issue coupon/discount codes as payout

**Manage Settings (Stripe):**
- **Minimum payment amount referee should spend** — minimum qualifying purchase amount (all plans)
- **Minimum payment count before referrer is rewarded** — how many payments the referee must make before the referrer is eligible for a reward; options 1–12 (requires Basic plan tier 1+; shown but locked on Starter)
- **Assign reward to referee when referrer is rewarded** — toggle for referee reward via Stripe; available only on Basic+ for double-sided refer-a-friend campaigns with Monetary reward type
- **Auto reward participants** — automatically disburse rewards; requires Pro (tier 2+). See Auto Reward section.

### Shopify
- Connect via OAuth — enter your store domain in the format `storename.myshopify.com` (you enter the store slug, the `.myshopify.com` suffix is added automatically)
- Automatically qualifies referrals and distributes rewards (gift cards, discount codes)
- Disconnecting Shopify removes data from Referral Rocket but does NOT uninstall the app from your Shopify store; you must remove it in Shopify before reinstalling

**Manage Settings (Shopify):**
- **Auto reward participants** — requires Pro (tier 2+)

### Cashfree
- Provide your **API Secret Key** from Cashfree
- Add the webhook URL in your Cashfree dashboard:  
  `https://app.referralrocket.io/api/public/cashfree/webhook`
- Automatically qualifies referrals on successful payments

**Manage Settings (Cashfree):**
- **Minimum payment amount referee should spend**

### Razorpay
- Provide your **Webhook Secret Key** and **Account ID** (enter Account ID without the `acc_` prefix — the app prepends it automatically)
- Add the webhook URL in your Razorpay dashboard:  
  `https://app.referralrocket.io/api/public/razorpay/webhook`
- **RazorpayX (optional payout):** additionally provide Customer Identifier, API Key ID, and API Secret Key to enable automated payouts via RazorpayX (enable the toggle, then fill in the extra fields)

**Manage Settings (Razorpay):**
- **Minimum payment amount referee should spend**
- **Assign reward to referee when referrer is rewarded** — Basic+ only, double-sided Monetary only
- **Auto reward participants** — requires Pro (tier 2+), only available when RazorpayX is active

### Tremendous
- Provide your **API Key** (click Validate to verify)
- Toggle **Test API Key** checkbox for sandbox payouts
- Select a **Campaign Template** from your Tremendous account (dropdown loads from your Tremendous account after validation)
- Displays your available Tremendous balance for the selected template
- Used to send gift cards, Visa cards, ACH, and PayPal to 100+ countries
- **Edit** (connected): change the selected Campaign Template without re-entering API key

**Manage Settings (Tremendous):**
- **Auto reward participants** — requires Pro (tier 2+)
- **Minimum amount before reward is sent** — when auto-reward is on
- **Payout Day** — when auto-reward is on (see Auto Reward section)
- Tremendous is locked/disabled for Starter (tier 0)

### Ghost
- Provide your **Webhook Secret Key** from Ghost
- Add the webhook URL in your Ghost settings:  
  `https://app.referralrocket.io/api/public/ghost/webhook`
- Checkbox: **"Qualify referrer for reward on referred user signup?"** — when checked, referrals qualify on signup; when unchecked, only on payment

### PayPal
- Provide your **Client ID** and **Client Secret**
- Toggle **Test API Key** checkbox for sandbox payouts
- Used for mass payouts to affiliates

**Manage Settings (PayPal):**
- **Auto reward participants** — requires Pro (tier 2+)
- **Minimum amount before reward is sent** — when auto-reward is on
- **Payout Day** — when auto-reward is on

---

## Auto Reward (Pro Feature)

Auto reward automatically disburses rewards to participants without manual action. Available on **Pro plan (tier 2+)** only. Starter and Basic see a locked preview with an "Upgrade to Pro plan" prompt.

**Supported integrations:** Stripe, Tremendous, PayPal, Razorpay (when RazorpayX is active), Shopify.

**Only one integration can have auto reward enabled at a time.** If you enable auto reward on a second integration, the first must be disabled first (the toggle is greyed out with an error: "You cannot turn on auto reward for this integration because another integration is turned on for auto reward").

**Auto reward settings (when enabled):**
- **Minimum amount before reward is sent** — rewards below this amount are not auto-disbursed; set to 0 for no minimum
  - For Razorpay: minimum is enforced at ≥100 (Razorpay API requirement)
- **Payout Day** — when to disburse:
  - **Immediate** — reward is sent as soon as the participant becomes eligible
  - **15th of every month** — rewards issued in a given month are disbursed on the 15th of the following month (e.g., rewards earned in December → disbursed on January 15th)
  - **30th of every month** — rewards issued in a given month are disbursed on the 30th of the following month

---

## Payout Methods

Referral Rocket does not fund rewards. You distribute them via:

| Method | Description |
|---|---|
| **Stripe** | Issue coupons/discount codes directly in Stripe |
| **Shopify** | Issue gift cards or discount codes to Shopify customers |
| **Tremendous** | Send gift cards (2,000+ options), Visa cards, ACH, PayPal to 100+ countries |
| **PayPal** | Automated or manual mass payouts to affiliates |
| **Razorpay** | Payout via Razorpay or RazorpayX (India) |
| **PayPal Mass Payments** | Download participant list, process bulk payouts via PayPal |
| **Wise Batch Payments** | Download participant list, process bulk payouts via Wise |
| **Manual** | Issue rewards outside the platform; mark as paid in Referral Rocket |

When issuing from the **Rewards Due** tab, you select a payout method from a dropdown that shows your connected integrations. Issuing via Stripe, Tremendous, Shopify, or Razorpay is irreversible once confirmed.

---

## Reward Statuses

Rewards move through these statuses:
- **Due** — earned, not yet paid
- **Paid** — marked as paid (issuedOn timestamp set)
- **Ignored** — manually skipped (issuedOn set)
- **Refunded** — reversed/refunded (can be resolved to RefundCompleted)
- **RefundCompleted** — final state after a Refunded reward is resolved; has a `refundAction` field set to either `"Marked Done"` or `"Reward Reversed"`

A reward has two monetary fields: `rewardValue` (the rate as configured, e.g., 10 for 10%) and `totalRewardValue` (the actual calculated dollar/currency amount paid out).

---

## How Referrals Qualify for a Reward

A participant appears in **Rewards Due** when their qualifying event is marked complete. This happens three ways:
1. **Manual** — navigate to Participant Details and mark the qualifying event complete
2. **API** — your backend calls the Referral Rocket API when the qualifying event (purchase, signup) occurs
3. **Automated integration** — Stripe, Shopify, Cashfree, Razorpay, or Ghost automatically notifies Referral Rocket when a transaction or signup is completed

---

## Individual Reward Customization Per Affiliate

From the **Participant Details** page, you can set a custom reward override for a specific affiliate that overrides the campaign-level reward.

Fields in the "Customize Individual Reward Details" modal:
- **Individual Reward** checkbox — activate or deactivate the individual reward override
- **Affiliate Reward Value** — numeric; for Percentage type, capped at 100 (must be < 100 to save)
- **Reward Type** — Monetary or Percentage (radio buttons)
- **Reward Currency** — currency selector
- **Issue Reward As** — Coupon or Credit. This selector is **hidden** (not shown) when: tieredRewardActive, mlmActive, or Shopify campaign type
- **Reward Valid For (months)** — shown when Issue Type = Coupon: 1, 3, 6, 9, 12, 18, 24, Forever (999)
- **Recurring commission** (affiliate campaigns only) — Life-time, Per Payment, Per Month
  - For Per Payment: "Number of payments per referral affiliate gets commission for" — 1, 2, 3, 6, 9, 12
  - For Per Month: "Period of months referral affiliate gets commission for" — 1, 2, 3, 6, 9, 12, 18, 24, 36

This individual reward takes precedence over the campaign-level reward for that specific affiliate.

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

**Add to `<head>` or before closing `</body>`:**
```html
<script
  type="text/javascript"
  campaign-id="YOUR-CAMPAIGN-ID"
  defer
  src="https://app.referralrocket.io/widget/widgetIndex.js"></script>
```

**Add where the widget should appear:**
```html
<div id="referral-rocket-widget"></div>
```

Verify installation: open browser console and type `window.Rocket`.

Best for: affiliate programs, marketing pages, higher conversion.

### Option 4 — In-App Integration (JavaScript SDK)

The SDK is available as `window.Rocket` once the script is loaded.

```javascript
// Get a campaign instance (pass campaignId to target a specific campaign)
const campaign = window.Rocket.getCampaign();           // auto-detects from cookie or script attribute
const campaign = window.Rocket.getCampaign('ABC123');   // explicit campaign ID

// Add a participant (register a new user to the campaign)
campaign.addParticipant({
  email: 'john@example.com',
  fName: 'John',
  lName: 'Smith',
  referredByCode: 'OPTIONAL_CODE',    // omit to auto-detect from rr_referral_code cookie
  referredByEmail: 'friend@example.com'  // optional
});

// Get a participant's details
campaign.getParticipantDetail({
  email: 'john@example.com'
  // or: code: 'REFERRAL_CODE'
});

// Qualify a participant (triggers reward eligibility)
campaign.qualifyParticipant({
  email: 'jane@example.com',
  amountPaid: 99.00,         // defaults to 0.0 if omitted
  referredByCode: 'CODE',    // omit to auto-detect from cookie
  rewardReferee: false       // true to also reward the referee (double-sided)
});

// Issue a direct reward to a participant (bypasses qualification flow)
campaign.issueDirectReward({
  email: 'john@example.com',
  rewardAmount: 50.00        // defaults to 0.0 if omitted
});

// Get the referral code stored in the visitor's cookie
campaign.getReferralCode();   // returns null if no cookie set

// Check if a referral code is valid
campaign.validateCode('SOME_CODE');

// Get full campaign configuration details
campaign.getCampaignDetail();

// Store a referral code in the cookie (cookie name: rr_referral_code)
// Cookie duration is fetched from the campaign's cookieDuration setting
window.Rocket.storeReferralCodeInCookie('CODE');

// Ensure SDK is initialized before making calls
await window.Rocket.ensureInitialized();
```

**Cookie behavior:**
- Cookie name: `rr_referral_code`
- Duration: fetched from campaign's `cookieDuration` field (set during campaign creation)
- If a different referral code is in the cookie, it is replaced with the new one
- The SDK automatically reads `?referralCode=` from the URL on page load and stores it

**Campaign ID resolution order:**
1. Explicit ID passed to `getCampaign('id')`
2. Resolved from `rr_referral_code` cookie via API lookup
3. Fallback to `campaign-id` attribute on script tag

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
  background-color="#ffffff"
  button-color="#093345"
  popup-header="Here's your discount!"
  button-value="Shop Now"
  defer
  src="https://app.referralrocket.io/widget/DiscountModal.js"></script>
```

All attributes except `campaign-id` are optional. The popup appears only when `?referralCode=` is present in the URL.

---

## Campaign Management

### Campaign Dashboard
Per-campaign analytics showing:
- Campaign duration, total participants, total referrals, total rewards (due + paid), revenue generated
- Monthly area chart: Participants, Referrers, Referees over 12 months
- For milestone campaigns: donut chart of completions per milestone
- For non-leadership campaigns: reward breakdown donut chart (paid vs. due)
- Recent referrals table with participant names, referral dates, and status

### Participants Tab
Shows everyone who has joined the campaign with status, referral count, and reward history. Sub-tabs:
- **All** — all participants
- **Direct** — participants who joined without being referred
- **Referred** — participants who joined via a referral link

You can:
- View individual participant details (referrals, rewards, team for MLM)
- Manually mark qualifying events
- Add participants manually (Add Participant button)
- Edit a participant's referral code
- Set individual reward overrides (affiliate campaigns)
- Export to Excel / CSV (download icon)

**Participant fraud scores:** Low (green), Medium (orange), High (red) — based on IP, device fingerprint, and behavior detection.

### Affiliates Tab (Affiliate Campaigns)
Two sub-tabs:
- **Active** — approved affiliates with their performance, referrals, and commission
- **Pending** — affiliates awaiting manual approval; approve or reject from here

### Rewards Section
Four sub-tabs:
- **Rewards Due** — earned but unpaid; select one or more and choose a payout method
- **Rewards Paid** — historical paid rewards
- **Rewards Ignored** — manually ignored rewards with reverse option
- **Rewards Refunded** — reversed/refunded rewards; can be marked done or reversed

### Campaign Assets (Creative Assets)

**For business owners (Pro plan tier 2+):**
- Upload promotional materials (images, PDFs, any file type) for affiliates to download
- Maximum 10 assets per campaign
- Maximum file size: 5MB per file
- Files can be drag-and-drop or file-browser uploaded
- Each asset requires a title

**For affiliates (all plans):**
- Access the asset library uploaded by the business
- View their personal "Assets Page Link" (a shareable URL to the asset gallery)

Business owners on Starter or Basic see a lock icon with "Upgrade to Pro plan to unlock this feature".

### Pausing / Ending a Campaign
Campaigns can be paused at any time without losing data. Campaigns with an expiration date end automatically.

---

## Email Notifications

Configure per-campaign from the **Email Notifications** tab. All emails have:
- Toggle (on/off) per email type
- Customizable subject line
- Rich-text email body (powered by ReactQuill) — most emails
- **Test** button — sends a preview to your account email

### For You (Business Owner Notifications)

| Email | Default | When Sent | Plan |
|---|---|---|---|
| New affiliate/referrer joins your program | **ON** | Every time someone signs up | All |
| A referral is made | OFF | When a participant refers someone | All |
| Participant eligible for reward | OFF | When a qualifying event is detected | All |
| Monthly reward report | OFF | First of each month | Basic+ (tier 1+) |

**Subject/body variables for "new affiliate joins":**
`$firstName`, `$lastName`, `$email`, `$referralLink`, `$companyName`

### For Affiliate / Referrer

| Email | Default | When Sent | Notes |
|---|---|---|---|
| Affiliate is approved | **ON** | When you manually approve | Only shown when manual approval is ON |
| Welcome email (joins program) | OFF | When affiliate joins (auto-approve) | Shown when auto-approve is ON, replaces approval email |
| Referrer earns a reward | OFF | When their referral qualifies | Non-affiliate campaigns only |
| Payout sent | OFF | When you mark a reward as paid | All campaigns |
| Share widget email | OFF | Allow participants to send referral emails | Includes "Include referee data in referrer referral link" toggle |

**Share widget email toggle — "Include referee data in referrer referral link"**: when checked, referee's email/name is encoded in the referral link the email sends, allowing the signup form to be pre-populated.

**Subject/body variables:**
- `$firstName`, `$lastName`, `$email`, `$referralLink`, `$companyName` — most emails
- `$reward`, `$totalRewardsDue`, `$totalRewards`, `$friendName`, `$referrerCode` — reward email
- `$referrerFirstName`, `$referrerLastName`, `$referrerEmail`, `$refereeFirstName`, `$refereeLastName`, `$refereeEmail`, `$referralLink`, `$referrerCode` — share widget email

### For Referee (Referred User)

| Email | Default | When Sent |
|---|---|---|
| Referred user joins via a referral link | OFF | When a referred user joins the program |

**Subject variables:** `$referrerFirstName`, `$referrerLastName`  
**Body variables:** `$firstName`, `$lastName`, `$email`, `$referrerFirstName`, `$referrerLastName`, `$referrerEmail`, `$referrerCode`

### Available Email Variables Summary

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

Account settings are under `/app/account/`. Navigation tabs differ by user type:

**Business owners (Admins):** Profile, Members, Email Settings, Payer Information, API Key, Webhooks  
**Non-Admin business users:** Profile + (Editor: API Key, Webhooks) or (Viewer: none)  
**Affiliates:** Profile, Tax (W-9 form), Tax Documents

### Profile
**Business fields (required):** First name, Last name, Company name, Company website, Company country. Optional: Country, Phone, Role.  
Email is read-only (cannot be changed in profile).

**Affiliate additional fields:**
- Profile picture (PNG/JPG, max 3MB)
- Bio (minimum 50 characters, maximum 255 characters)
- Audience metrics (dropdowns): Website Visitors (monthly), Total Followers, Email Subscribers — options: Less than 1,000 / 1,001–10,000 / 10,001–50,000 / 50,001–100,000 / 100,001–500,000 / 500,000–1M / 1M+
- Preferred categories (multi-select, up to 10)
- Social links: Instagram, TikTok, YouTube, X/Twitter, LinkedIn
- Up to 3 website URLs

**Affiliate badges** (shown on profile and in Find Affiliates) — based on the highest audience metric range:
| Badge | Range value | Meaning |
|---|---|---|
| Super Affiliate | "1000001-plus" | 1M+ reach |
| Top Affiliate | "500001-1000000" | 500K–1M reach |
| Strong Affiliate | "100001-500000" | 100K–500K reach |
| Emerging Affiliate | (all others) | under 100K |

### Team Management
Invite team members. Roles:
- **Admin** — full access
- **Editor** — can edit campaigns but not billing/account settings
- **Viewer** — read-only access

Team member limits by tier:
- Starter (tier 0): 1 user (owner only)
- Basic (tier 1): 3 users
- Pro (tier 2): 10 users
- Enterprise: Unlimited

Invite form: email address + role dropdown (Admin/Editor/Viewer).

### API Keys (Pro Plan — tier 2+)
Under **Account → API Keys**. Generate, reveal (Show/Hide), copy, and regenerate your API key. Regenerating immediately invalidates the previous key. Required for REST API access.

### Custom SMTP / Email Domain (Pro Plan — tier 2+)
Under **Account → Email Settings**. Configure your own SMTP server.

Required fields:
- From email address
- SMTP password (show/hide toggle)
- SMTP server hostname
- Port

Flow: fill all fields → click **Test Connection** → if successful, a success banner appears + **Save** button becomes available. Delete option available if config exists.

### Webhooks (Account-Level — Pro Plan — tier 2+)
Under **Account → Webhooks**. Add endpoints that receive event notifications for all campaigns in your account.

**Webhook form fields:**
- Status toggle (on/off) — only shown in edit mode
- Name
- URL (must include protocol: `https://`)
- Secret key (auto-generated, read-only, cannot be changed)
- Events — checkboxes for each available event type

**Webhook Detail view:**
- Shows the webhook configuration card
- Paginated notification log (10 per page, "Load More" button)
- Each log entry shows: event type, timestamp, status badge (200 = success, other = failed), HTTP status code, pretty-printed JSON payload

Full webhook guide: https://referral-rocket.gitbook.io/docs/developer-tools/webhooks

### Payer Information (for 1099-NEC)
Under **Account → Payer Information**. Required before enabling W-9 collection.

**All fields are required:**
- Full name (business owner or company name)
- Telephone number
- TIN — SSN format `XXX-XX-XXXX` or EIN format `XX-XXXXXXX` (format validated, **not verified against IRS/SSA records**)
- Street address, City, State, Country, ZIP code / foreign postal code

After saving, TIN is masked: last 4 digits shown as `***-**-XXXX` (SSN) or `**-***XXXX` (EIN).

### Tax Page (Affiliates Only)
Under **Account → Tax** (affiliates only). Affiliates fill in their own tax information / W-9 details here.

### Tax Documents (1099-NEC) — Affiliates Only
Under **Account → Tax Documents**. Download 1099-NEC Copy B forms.

Forms are auto-generated each January for the prior calendar year once paid rewards for an affiliate reach $600. Filter by tax year. Downloaded as `1099-NEC-{year}-CopyB.pdf`.

---

## Tax and Compliance (W-9 / 1099-NEC)

1. **Enable W-9 collection** on affiliate campaigns → affiliates must submit W-9 before accessing their referral link
2. **Configure Payer Information** in account settings with your business's legal name, TIN, and address
3. When total paid rewards to an affiliate reach **$600 in a calendar year**, Referral Rocket automatically generates a **1099-NEC Copy B** form in January of the following year
4. Affiliates download their form from their portal (Account → Tax Documents); you download from the same tab

---

## Affiliate Program Hub (Marketplace)

### For Businesses: List Your Program
List on the Referral Rocket Affiliate Program Hub — a directory where affiliates can discover and apply. Configure from **Marketplace** in the app.

**Marketplace listing limits by plan:**
- Starter (tier 0): 1 listing
- Basic (tier 1): 3 listings
- Pro (tier 2): 10 listings

**Listing status:**
- **Pending (0)** — submitted, awaiting review (24–48 hours)
- **Active (1)** — approved and live
- **Paused (2)** — requires a "Refresh" action to reactivate; the Refresh button updates the `refreshedOn` timestamp

**Marketplace listing fields:**
- Logo (image upload)
- Company Name (required)
- Country (required, dropdown)
- Affiliate/Referral URL (required, `https://` prefix auto-added; must be a valid URL)
- Commission (number, min 1)
- Commission Type: Monetary or Percentage
- Cookie Duration: 10, 15, 30, 60, or 90 days
- Category (required, single select from industry list)
- Contact (email/phone/URL, optional)
- Description (required, rich text, max 1000 characters)
- Reward Details (optional, rich text, max 1000 characters; default template provided)
- Program Terms (optional, rich text, max 1000 characters)

### For Businesses: Find Affiliates
Browse a database of affiliates and reach out directly. Requires:
1. Plan tier > 0 (Basic or higher)
2. The **Find Affiliates feature must be activated** on your account (activation is separate from plan level — if the feature is not activated even with a paid plan, users see a "Coming Soon" message)

**Filters:** Category, Location (country), Badge level.  
**Send invite emails** directly (rate-limited: 30-day wait between invites; after 3+ invites, the system notes "You have reached out several times now. Wait for affiliate to get back").

Affiliate performance badges:
- **Super Affiliate** — 1M+ reach (audience metric range "1000001-plus")
- **Top Affiliate** — 500K–1M reach (range "500001-1000000")
- **Strong Affiliate** — 100K–500K reach (range "100001-500000")
- **Emerging Affiliate** — under 100K (all others)

### For Affiliates: Set Up Your Profile
Set up a discoverable profile:
- Profile photo, bio, country/location
- Preferred categories (up to 10)
- Audience data: monthly website visitors, total followers, email subscribers
- Social media links: X/Twitter, Instagram, YouTube, LinkedIn, TikTok, up to 3 website URLs

---

## Campaign Management — Full Reference

### Campaigns List Page

Displays all campaigns in a sortable table. Columns:
- **Campaign ID**, **Name**, **Type**, **Status** (Active / Paused / Ended), **Participants**, **Impressions**, **Revenue**, **Rewards Pending**

Row actions (Admin/Editor only, not Viewer):
- **View Details** — opens the campaign
- **Edit** — opens the campaign in the edit wizard (disabled if campaign is being deleted)
- **Clone** — creates an exact copy with a new Campaign ID; participants, referrals, and rewards data are **not** copied

Campaign limit enforcement (enforced in the UI):
- Tier 0 (Starter): max 1 campaign
- Tier 1 (Basic): max 3 campaigns
- Tier 2 (Pro): max 10 campaigns
- Tier 3 (Enterprise): unlimited

If the limit is reached, the "Create New Campaign" button is disabled and an upgrade prompt is shown.

**Affiliate view (when logged in as an affiliate):** Different columns — Campaign Name, Referral Link, Approval Status, Impressions, Referrals, Revenue, Commission Earned, Commission Due. Referral Link is only shown when approval status = Approved AND campaign is Active AND W-9 is submitted (if required). Otherwise shows "Waiting for approval", "W-9 tax form is required", or "Campaign [status]".

---

### Campaign Details Page

Shows the **Campaign Link** (`https://referralrocket.io/campaign?id=YOUR-CAMPAIGN-ID`) with a copy button, then navigation tabs (NavCampaign).

**NavCampaign tabs** (vary by campaign type):
- Dashboard
- Participants (or Affiliates for affiliate campaigns)
- Rewards
- Program Details
- Integration
- Email Notifications
- Install
- Assets
- Webhooks
- Tax Reports (affiliate campaigns only)
- Settings / Edit

---

### Campaign Dashboard

Metrics cards shown (campaign-level):
- **Campaign Duration** — number of days since campaign creation
- **Total Participants** — everyone who has joined
- **Total Referrals** — total referrals made
- **Revenue Generated** — total revenue tracked from referred users
- **Reward Due** — total unpaid reward amount
- **Reward Paid** — total paid reward amount
- **Total Impressions** — total link impressions

Charts:
- **12-month area chart** — Participants, Referrers, and Referees per month (rolling last 12 months)
- **Reward donut chart** — Total Paid vs Total Due (shows "No data" placeholder when both = 0)
- **Milestone donut chart** (milestone/newsletter campaigns only) — participants who completed each milestone

Recent activity table toggles between:
- **Recent Referrals** — referred users with name/email, Referred By, joined date, amount spent, event status
- **Top Promoters** — top referring participants

Event status values: **Pending** (signed up, no payment yet), **Ongoing** (payments started, not yet complete), **Completed** (qualified for reward).

---

### Participants Tab

For non-affiliate campaigns. Shows all participants in a searchable, paginated table.

**Columns:** Participant (name + email + avatar), Code (monospace chip), Referred By (name + email), Impressions, Referrals, Revenue, Reward Due, Reward Paid, Fraud Score, Joined On.

A sticky note icon appears on the participant row if the participant has notes attached.

**Actions:**
- Click any row → Participant Details
- **Export** button — sends a CSV to the campaign owner's email (for large datasets)
- **Add Participant** — manually add a single participant
- Search bar with 1-second debounce

Sorted by Joined On (newest first) by default. Server-side pagination (page size 10).

---

### Affiliates Tab (Affiliate Campaigns)

Two sub-tabs:

**Active affiliates** — same columns as Participants table above. Additional actions:
- **Add Affiliate** (single)
- **Bulk Add Affiliates** (CSV upload)
- **Export** CSV

**Pending affiliates** — same columns minus Revenue/Impressions. Additional capabilities:
- **Row selection** (checkboxes) — select one or multiple
- **Approve/Reject** selected via ApproveModal (can approve/reject multiple at once)
- **Add Affiliate** (single)
- **Bulk Add Affiliates**
- **Export** CSV

---

### Participant Details Page

Stats row (5 cards): **Impressions**, **Referrals**, **Revenue Generated**, **Reward Due**, **Reward Paid**.

Profile section shows:
- Avatar, full name, email, phone (if collected)
- Fraud risk badge (Low / Medium / High) with color coding (green / orange / red)
- Joined date badge
- **Referral Link** (full URL) with copy button
- **Referral Code** with copy button and **edit button** — opens "Edit Referral Code" modal; new code must be 4–8 alphanumeric characters, unique; validates format before allowing save
- **Referred By** — clickable link to navigate to the referrer's details page
- **Amount Spent** — total revenue attributed to this participant

Reward Details section (refer-a-friend and Shopify):
- **Event Status** — Pending / Ongoing / Completed / Not Applicable
- For double-sided campaigns: **Referee Reward**, Referee Reward Redeemed, Referee Reward Balance
- **Referrer Reward**, Referrer Reward Redeemed, Referrer Reward Balance

Tax Documents section (shown when campaign has Collect W9 enabled):
- **W-9 Document** — Submitted (with download link) or Not Submitted
- **Tax Information** — Submitted (with masked TIN) or Not Submitted

**Notes section** — free-text textarea, max 255 characters. Notes are saved per-participant and shown as a tooltip icon on the participants table. Save button appears only when notes differ from saved value.

**Individual Reward Override** — accessible from the page header; opens "Customize Individual Reward Details" modal to set a per-participant commission that overrides the campaign default.

Sub-tabs (NavParticipantsDetails):
1. **Referrals** — list of people this participant referred; columns: Referral (name/email), Referred On, Amount Spent, Commission Earned, Event Status; Qualify button per row (opens QualifyModal); Add Referral button
2. **Rewards** — all reward records for this participant; columns: Referred User (with MLM level badge if applicable), Amount Spent, Reward Value, Total Reward, Issued On, Status; also shows "Direct reward" label for directly issued rewards
3. **Team** (MLM campaigns only) — sub-affiliates recruited by this participant; columns: Affiliate (name/email), Joined On, Revenue Generated, Reward Due, Reward Paid, Fraud Score

---

### QualifyModal

Opened from the Referrals sub-tab on Participant Details. Fields:
- **Amount Paid** — numeric input for the transaction amount
- **Reward Referee** — checkbox (whether to also reward the referred user, for double-sided campaigns)

---

### Campaign Email Notifications Tab

All emails have a toggle (on/off), subject line input, rich-text body editor (ReactQuill), and a **Test** button to send a test email to your own address.

**Default on/off states:**
| Email | Default |
|---|---|
| Affiliate Approved | ON |
| New affiliate/referrer joined (to business) | ON |
| Welcome email (affiliate joined program, to affiliate) | OFF |
| Participant earns a reward | OFF |
| Payout sent | OFF |
| New referral made (to business) | OFF |
| Referee joined via referral | OFF |
| Monthly reward report | OFF |
| Share widget email | OFF |

**Share widget email** has an extra toggle: **Include referee data in referral link** — when enabled, the referral link in the shared email pre-fills the invitee's data.

---

### Campaign Install Tab

Three-step guide:
1. Set up integrations
2. Configure rewards
3. Install & promote

For **referral_rocket_hosted** campaigns: shows the hosted Campaign Link with copy button and a downloadable QR code (PNG).

For **self_hosted** campaigns: shows the embed script tag + `<div id="referral-rocket-widget">` + SDK code examples.

For **Shopify** campaigns: additionally shows the Discount Modal script.

The script tag and all code blocks have a copy button. The Campaign ID is pre-filled in all code examples.

---

### Global Dashboard

Top metrics cards (account-wide):
- **Total Campaigns** (links to create campaign if 0)
- **Total Participants**
- **Total Referrals**
- **Revenue Generated**
- **Pending Rewards** (links to /app/rewards)
- **Total Affiliates**
- **Pending Affiliates** (links to /app/pending-affiliates)

Charts:
- **12-month area chart** — Participants, Referrers, Referrals (selectable month range)
- **Campaign type donut** — breakdown by campaign type
- **Campaign ratio** — distribution across active campaigns

Activity tables toggle between **Recent Referrals** and **Top Promoters**.

**Affiliate dashboard** (shown when logged in as an affiliate): different metrics — their own impressions, referrals, commission earned, campaigns joined.

---

### Global Rewards Page (/app/rewards)

Cross-campaign view of all Rewards Due across all campaigns. Allows processing payouts without navigating into each campaign individually.

---

### Global Pending Affiliates Page (/app/pending-affiliates)

Cross-campaign view of all pending affiliate applications across all campaigns. Allows bulk approval/rejection without navigating into each campaign.

---

### Billing Page

Embeds a Stripe Pricing Table component. Shows different pricing tables based on company country:
- India → INR pricing table
- All other countries → USD pricing table

The pricing table is pre-filled with the user's email for Stripe Checkout.

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
Cookie duration: 30, 60, 90, or 180 days (configurable per campaign). The **last referrer** gets credit if multiple affiliates refer the same person (Last Referrer win model, fixed). Cookie name: `rr_referral_code`.

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

**Can I set a custom reward for a specific affiliate that differs from the campaign's default?**
Yes. From the Participant Details page, click the individual reward option to open the "Customize Individual Reward Details" modal. This sets a per-participant override with its own reward type, value, currency, and issue settings.

**What is the Auto Reward feature?**
Auto Reward (Pro plan only) automatically distributes rewards when participants become eligible, without manual action. Available for Stripe, Tremendous, PayPal, Razorpay (with RazorpayX), and Shopify. Configure payout timing: Immediate, 15th of every month, or 30th of every month. Only one integration can have auto reward enabled at a time.

**What is issueDirectReward in the SDK?**
`campaign.issueDirectReward({ email, rewardAmount })` issues a reward directly to a participant without going through the standard qualification flow. It bypasses the usual referral tracking. Useful for manually triggering a one-time reward from your backend logic.

**What file types can I upload to Campaign Assets?**
Images (shown as preview), PDFs (shown as iframe preview), or any file type (shown as a document icon). Maximum size is 5MB per file. Up to 10 assets per campaign. Requires Pro plan.

**Why can't I access Find Affiliates even on a paid plan?**
The "Find Affiliates" feature requires both a paid plan (Basic or higher) AND the feature must be specifically activated on your account. If not activated, even paid plans see "Coming Soon" instead of the affiliate directory.

**What are the cookie duration options in the Marketplace listing?**
10, 15, 30, 60, or 90 days (these are independent from campaign cookie duration which uses 30/60/90/180 days).

**Can a Stripe integration require multiple payments before rewarding the referrer?**
Yes. In the Manage settings for a connected Stripe integration, you can set "minimum payment count before referrer is eligible for reward" to 1–12. This requires a Basic plan or higher.

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
