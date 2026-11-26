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

**Pro adds:** Custom email domain (custom SMTP), auto reward, REST APIs, white label (remove Referral Rocket branding).

Basic and Pro offer a 15-day free trial.

---

## Getting Started (5 Steps)

### Step 1 — Sign Up
Create an account at https://app.referralrocket.io. No credit card required for the free tier.

### Step 2 — Create a Campaign
From the dashboard click **New Campaign**. The campaign creation wizard walks you through:
1. Campaign type
2. Campaign info (name, hosting, expiration)
3. Reward & widget setup
4. Share widget configuration
5. Invitee widget configuration
6. Customization (design)
7. Integrations (optional)
8. Email notifications

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

**Subtypes:**
- **Single-sided** — only the referrer receives a reward (e.g., "Refer a friend, earn $20")
- **Double-sided** — both referrer and referee receive rewards (e.g., "Give $20, Get $20" — the Uber model)

Best for: e-commerce, SaaS, any product where existing customers bring in paying users.

### 2. Affiliate Program
Third-party publishers, creators, and partners earn commissions for driving sales or signups.

Key affiliate-specific features:
- **Lifetime commission** — affiliate earns on every future purchase by their referred users
- **Maximum commissions per referral** — cap the number of payments per referred user (options: 1, 2, 3, 6, 9, 12)
- **Maximum commission period** — limit the earning window in months (options: 1, 2, 3, 6, 9, 12, 18, 24, 36 months)
- **Tiered rewards** — escalating commissions based on referral milestones, time active, or total revenue generated (up to 5 tiers, only available on lifetime commission)
- **Multi-Level Marketing (MLM)** — earn commissions from affiliates you recruit into the program (up to 5 levels deep, only on lifetime commission)
- **Network coupon** — give affiliates a discount code to share with their audience (creates a double-sided setup)
- **Welcome bonus** — a one-time bonus paid when an affiliate joins
- **Auto approve** — toggle whether new affiliates are approved instantly or require manual approval
- **Creative assets link** — provide a Google Drive or Dropbox link for affiliates to download promotional materials
- **Cookie duration** — 30, 60, 90, or 180 days (how long the referral cookie persists)
- **Cookie win model** — Last referrer (fixed, not configurable)
- **W-9 collection** — require affiliates to submit a W-9 form before accessing their referral link (for US tax compliance)
- **Approval widget** — shown to affiliates pending manual approval; customizable approval message (max 255 characters)

Best for: content creators, media partners, B2B referral networks.

### 3. Newsletter Referral
Current subscribers earn rewards for referring new subscribers to your newsletter. Uses milestone-style progression.

Best for: newsletters, media publications, Ghost blogs.

### 4. Milestone Giveaways
Participants unlock rewards when they hit specific referral thresholds (e.g., refer 5 friends → reward tier 1, refer 10 friends → reward tier 2). Configure individual milestones with their own reward values.

Best for: product launches, waitlists, pre-launch campaigns.

### 5. Leaderboard Program
Participants are ranked by referral volume on a live leaderboard. Top performers win prizes.

Best for: short-term contests, giveaways, competitions.

### 6. Shopify
Purpose-built for Shopify stores. When a referred friend makes their first purchase, both parties can receive exclusive perks (discounts or store credits). Shopify integration handles tracking and reward distribution automatically. Always self-hosted (embedded in your Shopify store).

Best for: Shopify merchants wanting a plug-and-play referral program.

---

## Campaign Setup Details

### Campaign Info Tab
- **Campaign name** — the internal name for your program
- **Expiration date** — optional; set a date when the campaign automatically ends
- **Campaign hosting:**
  - **Via My Website** (self_hosted) — you embed the widget or use the SDK on your own site. Requires a Share URL — the page participants will share (e.g., `https://myapp.com/referral`). Referral Rocket appends `?referralCode=XXXXX` automatically.
  - **Via Referral Rocket** (referral_rocket_hosted) — Referral Rocket hosts a campaign page at `https://referralrocket.io/campaign?id=YOUR-CAMPAIGN-ID`. Not available for Shopify campaigns.
- **Is the share URL where users sign up?** — if yes, Referral Rocket can auto-detect signups from that URL

### Program Details Section
On the reward/widget setup step, you can configure:
- **Program title** — the main heading displayed in the join widget
- **Program subtitle** — description of the program (max 255 characters)
- **Program details** (affiliate & refer-a-friend only) — rich text, max 1000 characters, show/hide toggle
- **Reward info** (affiliate & refer-a-friend only) — rich text explaining commission structure, max 1000 characters, show/hide toggle
- **Program terms** (affiliate & refer-a-friend only) — rich text, max 1000 characters, show/hide toggle

### Form Configuration
On the reward/widget setup step:
- **Terms and conditions** — optional checkbox; if enabled, provide a URL to your T&C page
- **Hide first name** — remove first name field from the join form
- **Hide last name** — remove last name field from the join form
- **Collect phone number** — add a phone field to the join form
- **Button text** — customize the form submit button text (max 30 characters)
- **Collect W9** (affiliate only) — require affiliates to submit a W-9 before accessing their link

---

## Reward Configuration

### Reward Types (set via "Set Referrer Reward" / "Set Affiliate Reward" button)
- **Monetary** — fixed cash amount (e.g., $20)
- **Percentage** — percentage of sale value (e.g., 10%)
- **Credit** — used automatically when tiered rewards or MLM are enabled

### Reward Currency
Multi-currency supported. Currency is set on the reward configuration. For Shopify campaigns, rewards are processed in your store's designated currency.

### Tiered Rewards (Affiliate campaigns, lifetime commission only)
Enable escalating commission rates based on performance milestones:
- **Referral-based** — based on number of successful referrals
- **Time-based** — based on months the affiliate has been active
- **Revenue-based** — based on total revenue generated

Configure up to 5 tiers. Each tier has a threshold value and reward amount. Affiliates exceeding the highest tier threshold earn the highest tier reward.

### Multi-Level Marketing / MLM (Affiliate campaigns, lifetime commission only)
Affiliates earn commissions from affiliates they recruit into your program, up to 5 levels deep.

When using Percentage reward type, choose the MLM calculation method:
- **Total Sales** — each level's percentage is applied to the total sale amount
- **Program Commission** — each level's percentage is applied to the previous level's commission

### Club Reward
Available for affiliate, refer-a-friend, and Shopify campaigns. When enabled, all rewards for a given referred user go to the first referrer who referred them, even if another referrer later claimed credit.

### Referral Limits
Toggle **Limit on referrer/affiliate referrals** to cap how many qualifying referrals a single participant can make.

### Welcome Bonus (Affiliate only)
A one-time bonus paid to an affiliate when they join the campaign.

### Network Coupon (Affiliate only)
Toggle "Create a coupon/discount code affiliate can share with their network" to give affiliates a discount code (double-sided setup). Configure the discount value via "Set Network Coupon."

### How Referrals Qualify for a Reward
A participant appears in **Rewards Due** when their qualifying event is marked complete. This happens three ways:
1. **Manual** — navigate to Participant Details and mark the qualifying event complete
2. **API** — your backend calls the Referral Rocket API when the qualifying event (purchase, signup) occurs
3. **Automated integration** — Stripe, Shopify, Cashfree, Razorpay, or Ghost automatically notifies Referral Rocket when a transaction or signup is completed

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

## Installation Options

### Option 1 — Hosted Campaign Page (No Code)
Share a Referral Rocket-hosted URL. No code required.

**URL format:**
```
https://referralrocket.io/campaign?id=YOUR-CAMPAIGN-ID
```

A QR code is also generated and downloadable from the campaign's **Install** tab.

**User flow:** User visits link → enters email & joins → receives personal referral link → shares it → new user clicks link → tracked automatically.

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

Best for: affiliate programs, marketing pages, higher conversion focus.

### Option 4 — In-App Integration (JavaScript SDK)
Integrate the referral program inside your web app for logged-in users.

**Install the script once (same as Option 3), then use the SDK:**

```javascript
// Get campaign info
window.Rocket.getCampaign().then(campaign => {
  console.log(campaign);
});

// Add a participant (referrer or new user)
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

**Authentication:** API key — available on Pro plan (tier 2+). Manage API keys under Account → API Keys. Generating a new key immediately invalidates the old one.

Best for: mobile apps, headless builds, complex custom flows.

### Shopify Discount Modal (Shopify-Specific Install)
Add this script to your Shopify theme to show referred visitors a discount code popup at checkout:

```html
<script
  type="text/javascript"
  campaign-id="YOUR-CAMPAIGN-ID"
  defer
  src="https://app.referralrocket.io/widget/DiscountModal.js">
</script>
```

---

## Widgets

Referral Rocket uses four distinct widgets:

### 1. Join Widget
Shown to people who come to sign up / join the referral program. Includes the program title, subtitle, signup form, and join button. Displays program details, reward info, and terms if configured.

**Form fields (configurable):** First name, last name (both optional to hide), email (required), phone (optional).

### 2. Share Widget
Shown to participants after they've joined. Displays their unique referral link, social sharing buttons, and copy-to-clipboard options.

**Configuration options (Share Widget tab):**
- Share widget title and subtitle
- Social media platforms to show: Instagram, WhatsApp, Twitter/X, Facebook, LinkedIn, Mail
- Custom WhatsApp message (max 250 characters) — shared when participants click WhatsApp
- Custom LinkedIn message (max 250 characters)
- Show/hide sign-up link (lets new referrers sign up from the share widget)
- "Include referee data in referral link" option (for email sharing)

### 3. Invitee Widget
Shown to people who click a referral link before joining. Presents the offer to the referred friend.

**Configuration options (Invitee Widget tab):**
- Header and description — support variable substitution: `$referrerFirstName`, `$referrerLastName`, `$referrerCode`, `$referrerEmail`
- Redirect URL — where to send the invitee after they click the CTA button. Supports variables: `$refereeFirstName`, `$refereeLastName`, `$refereeEmail`, `$referrerCode`
- Collect phone number — add phone field to invitee form
- Hide first/last name — optional fields for invitee form
- Invitee button text — customize the CTA button

### 4. Approval Widget (Affiliate Campaigns with Manual Approval)
Shown to affiliates whose application is pending approval. Displays a customizable message (max 255 characters) explaining what to expect.

---

## Widget Customization

Full widget customization is available on **Basic plan and above**. Starter plan (tier 0) cannot access customization settings.

**Available customization options:**

**Branding:**
- Logo upload (company logo)
- White-label toggle — removes "Powered by Referral Rocket" branding (requires Pro plan / tier 2+)
- Company image upload
- Company background image upload

**Layout & Colors:**
- Page background color
- Widget background color
- Box shadow toggle
- Widget alignment (vertical)
- Border radius controls
- Widget width controls

**Typography:**
- Font family dropdown
- Font size dropdown
- Bold / italic / underline for: Header, Description, Sign Up Link, Button Text

**Buttons & Fields:**
- Button color
- Button border radius
- Field text color
- Field background color

**Label Language:**
- Multilingual widget labels — change the language of all widget UI labels (not content you write, just UI text like "Submit", "Copy Link", etc.)

**Social Media Sharing:**
- Toggle individual platforms: Instagram, WhatsApp, Twitter/X, Facebook, LinkedIn, Mail
- Custom WhatsApp message (max 250 chars)
- Custom LinkedIn message (max 250 chars)

**Advanced (per-widget):**
- Reward progress bar customization
- Referrals list display customization
- Leadership board progress customization
- Milestone widget customization (Pro only)
- Affiliate program details section styling (font, color)
- Invitee widget image upload (Pro only)

---

## Integrations (Campaign-Level)

Set up integrations from the **Integration** tab on each campaign.

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

## Webhooks (Account-Level)

Account-level webhooks let Referral Rocket send event notifications to your server when key actions occur (participant joins, referral qualifies, reward is due, etc.).

Manage webhooks under **Account → Webhooks**. You can add multiple webhook endpoints, view event history, and edit existing webhooks. This is a tiered feature — availability depends on your plan.

Full webhook guide: https://referral-rocket.gitbook.io/docs/developer-tools/webhooks

---

## Email Notifications

Configure per-campaign from the **Email Notifications** tab. All emails have customizable subject lines and rich-text bodies (powered by ReactQuill). A **Test** button lets you send a test email.

### For You (Business Owner Notifications)

| Email | When Sent | Plan Restriction |
|---|---|---|
| New affiliate/referrer joins | Every time someone joins your program | All plans |
| A referral is made | When a participant refers someone | All plans |
| Participant eligible for reward | When a qualifying event is detected | All plans |
| Monthly reward report | First of each month | Basic+ (tier 1+) |

### For Affiliate / Referrer

| Email | When Sent | Notes |
|---|---|---|
| Affiliate is approved | When you manually approve a pending affiliate | Manual approval only |
| Welcome email | When affiliate/referrer joins (auto-approve) | Auto-approve mode |
| Referrer earns a reward | When their referral qualifies | Non-affiliate campaigns only |
| Payout sent | When you mark a reward as paid | All campaigns |
| Share widget email | Allow participants to send email via share widget | Toggle "include referee data" option available |

### For Referee (Referred User)

| Email | When Sent |
|---|---|
| Joined via referral link | When a referred user joins the program |

### Available Email Variables

Use these in subject lines and body content:

| Variable | Description |
|---|---|
| `$firstName` | Participant's first name |
| `$lastName` | Participant's last name |
| `$email` | Participant's email |
| `$referralLink` | The participant's unique referral link |
| `$companyName` | Your company name |
| `$reward` | Reward value |
| `$totalRewardsDue` | Total rewards owed to the participant |
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
- **Rewards Due** — participants who qualify for a reward but haven't been paid yet
- **Rewards Paid** — historical paid rewards
- **Rewards Ignored** — rewards that were manually ignored
- **Rewards Refunded** — rewards that were reversed/refunded

### Campaign Dashboard
Per-campaign analytics: clicks, joins, referrals, conversions, and reward totals.

### Campaign Assets (Creative Assets)
Upload and manage images and creative materials that affiliates can download to promote your program. Also set a link to an external asset folder (Google Drive, Dropbox) in campaign settings.

### Pausing / Ending a Campaign
Campaigns can be paused at any time from campaign settings without losing data. Campaigns with an expiration date end automatically.

---

## Affiliate Program Hub (Marketplace)

### For Businesses: List Your Program
List your affiliate program on the Referral Rocket Affiliate Program Hub — a directory where affiliates can discover and apply to programs. Configure from **Marketplace** in the app.

### For Businesses: Find Affiliates
The **Find Affiliates** feature (paid plans, with feature activation) lets you browse a database of affiliates and reach out to them directly.

**Affiliate database features:**
- Browse affiliate profiles with performance badges:
  - **Super Affiliate** — 1M+ reach (subscribers, visitors, or followers)
  - **Top Affiliate** — 500K–1M reach
  - **Strong Affiliate** — 100K–500K reach
  - **Emerging Affiliate** — under 100K reach
- Filter by: **Category** (niche), **Location** (country), **Badge level**
- View each affiliate's bio, preferred categories, website visitors (monthly), total followers, email subscribers
- View social profiles: X/Twitter, Instagram, YouTube, LinkedIn, TikTok, Website(s)
- **Send invite emails** directly from the platform (rate-limited: wait 30 days between invites; after 3 invites the system suggests letting the affiliate come to you)

### For Affiliates: Set Up Your Profile
Affiliates can set up their public profile on Referral Rocket to be discoverable by businesses:
- Profile photo
- Bio
- Country / location
- Preferred categories (up to 10)
- Audience data: monthly website visitors, total followers, email subscribers
- Social media links: X/Twitter, Instagram, YouTube, LinkedIn, TikTok, up to 3 website URLs

---

## Account Settings

### Team Management
Invite team members to collaborate. Roles:
- **Admin** — full access
- **Editor** — can edit campaigns but not billing/account settings
- **Viewer** — read-only access

Team member limits by plan:
- Starter: 1 user
- Basic: 3 users
- Pro: 10 users
- Enterprise: Unlimited

### API Keys (Pro Plan)
Under **Account → API Keys**. Generate, reveal, copy, and regenerate your API key. Regenerating immediately invalidates the previous key. Required for REST API access.

### Custom SMTP / Email Domain (Pro Plan)
Under **Account → Email Settings**. Configure your own SMTP server to send notification emails from your own domain.

Required fields:
- From email address
- SMTP password
- SMTP server hostname
- Port

Click **Test Connection** to verify before saving.

### Webhooks (Account-Level)
Under **Account → Webhooks**. Add webhook endpoints that receive event notifications for all campaigns in your account.

### Payer Information (for 1099-NEC)
Under **Account → Payer Information**. Required before enabling W-9 collection on affiliate campaigns.

Fields:
- Full name (business owner or company name)
- Telephone number
- TIN — Taxpayer Identification Number (SSN format: `XXX-XX-XXXX` or EIN format: `XX-XXXXXXX`). Format is validated only — not verified against IRS/SSA records.
- Street address
- City
- State
- Country
- ZIP code / foreign postal code

### Tax Documents (1099-NEC)
Under **Account → Tax Documents**. Download 1099-NEC Copy B forms for your affiliates.

Forms are generated automatically each January for the prior calendar year once paid rewards for an affiliate reach the IRS $600 reporting threshold. Filter by tax year.

**To enable 1099-NEC generation:**
1. Set up Payer Information in account settings
2. Enable "Collect W9" on your affiliate campaigns
3. Affiliates submit their W-9 form before accessing their referral link
4. Forms are auto-generated each January

---

## Tax and Compliance (W-9 / 1099-NEC)

Referral Rocket supports US tax compliance for affiliate programs:

1. **Enable W-9 collection** in affiliate campaign settings → affiliates must submit a W-9 before accessing their referral link
2. **Configure Payer Information** in account settings with your business's legal name, TIN (SSN or EIN), and address
3. When total paid rewards to an affiliate reach **$600 in a calendar year**, Referral Rocket automatically generates a **1099-NEC Copy B** form in January of the following year
4. Affiliates can download their 1099-NEC from their portal; you can download them from Account → Tax Documents

---

## Finding Your Campaign ID

Your Campaign ID is visible:
1. In the URL when viewing a campaign: `.../campaign/YOUR_CAMPAIGN_ID/...`
2. In campaign settings under **Campaign Details**
3. On the campaign **Install** tab

---

## Common Questions

**Do participants need to sign up for Referral Rocket separately?**
No. Participants sign up for *your* referral program through your widget or hosted page. They interact with your brand, not Referral Rocket's (unless you share the hosted URL directly, in which case they see the Referral Rocket campaign page).

**Can I white-label the widget?**
Yes, on Pro plan (tier 2+). Toggle "Remove Referral Rocket branding" in widget customization to remove the "Powered by Referral Rocket" footer.

**Do I need coding experience?**
No coding needed for the hosted campaign page (Option 1). For the embed widget (Option 3) you need basic HTML. For the in-app SDK (Option 4) or REST API (Option 5) you need a developer.

**Does Referral Rocket fund the rewards?**
No. You fund and distribute rewards. Referral Rocket tracks who has earned what and helps you disburse via integrations (Tremendous, Stripe, PayPal, Wise, RazorPayX, Shopify).

**Can I reward both the referrer and the referred friend?**
Yes. Enable **double-sided** when setting up a Refer-a-Friend or Shopify campaign, then configure both a referrer reward and a referee reward.

**Can I limit how much a single person can earn?**
Yes. Toggle **Limit on referrer/affiliate referrals** in campaign settings to cap the number of qualifying referrals per participant.

**How does cookie tracking work for affiliates?**
Referral Rocket sets a cookie when someone clicks a referral link. Cookie duration is configurable: 30, 60, 90, or 180 days. If multiple affiliates refer the same person, the **last referrer** gets credit (Last Referrer win model, fixed).

**Can I run multiple campaigns simultaneously?**
Yes, up to your plan limit. Use `window.Rocket.getCampaign('campaign-id')` to target a specific campaign when multiple are active on the same page.

**What happens if an affiliate's referral exceeds the highest tier threshold in a tiered reward setup?**
They continue earning at the highest tier's reward rate.

**Can I collect both phone numbers and hide name fields?**
Yes, the join form fields are independently configurable. You can collect phone number while hiding first and/or last name fields.

**How do I add participants who didn't use a referral link?**
Use the **Add Participant** button on the Participants tab to manually add someone to a campaign.

**Is there a free trial for paid plans?**
Yes — Basic and Pro plans include a 15-day free trial.

**What social media platforms can participants share on?**
Instagram, WhatsApp (with custom message), Twitter/X, Facebook, LinkedIn (with custom message), and email/mail. Each platform can be individually enabled or disabled in campaign customization.

**What languages are supported for the widget UI?**
The Label Language option in widget customization lets you change the language of all widget UI labels. The specific languages available are configurable from the platform.

**Where do I find the installation script?**
Navigate to your campaign → **Install** tab. The script tag is pre-filled with your Campaign ID.

**How do I integrate with Ghost for a newsletter referral program?**
Create a newsletter or any campaign type, go to the Integration tab, select Ghost, provide your webhook secret key, and add the Referral Rocket webhook URL to your Ghost settings: `https://app.referralrocket.io/api/public/ghost/webhook`. Optionally enable "qualify on signup" to qualify referrals when the referred user signs up.

**When are 1099-NEC forms generated?**
Automatically each January for the prior calendar year, for any affiliate who received $600 or more in paid rewards. You must have Payer Information set up in your account settings and W-9 collection enabled on your campaign.

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
