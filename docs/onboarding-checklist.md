# Chaplins Barbers — onboarding checklist

This is the list of things we need from Sam before the website goes fully live and starts pulling people through Google.

The site itself is already built and ready. What follows is the wiring: getting it on a real domain, claimed in Google, connected to his socials, and protected so nothing breaks when he's not paying attention.

---

## 1. Domain — own or register?

**What we need to know first:** does Sam already own a domain like `chaplinsbarbers.co.uk`?

| Scenario | Action |
|---|---|
| Yes, he owns one | We need login to the registrar (GoDaddy, Namecheap, 123-reg, etc.) so we can point it at the site. |
| No, he doesn't | We register `chaplinsbarbers.co.uk` (or similar — `chaplinsbarbers-sevenoaks.co.uk` if the first is taken) on Porkbun. About £8 a year. Sam's name on the registration. |
| He doesn't want a custom domain right now | The site stays at `tokelomogorosi-ctrl.github.io/chaplins-barbers-website/` — works fine but harder to remember. |

**Decision Sam makes:** which domain. We do the rest.

---

## 2. Google Business Profile — claim and verify

He almost certainly already has one (the JSON-LD shows 24 reviews, voice profile mentions 153 — depends which platform that count came from). The question is whether **he** has admin access.

What to confirm with Sam:
- The Google account email he uses for the shop (or his personal Google if there's no shop email yet).
- Whether he's the verified owner. If not, we go through the claim process — Google sends a postcard to the shop with a code.
- Once claimed: we'll add his correct opening hours, services, prices, photos, and the website link. He approves before anything goes live.

If he doesn't have a shop email yet, we set up `info@chaplinsbarbers.co.uk` (mail forwarding to his personal — free with most registrars).

---

## 3. Google Search Console — verification

This is what tells us how the site is doing on Google.

We need to verify the site in GSC against the same Google account as the Business Profile (cleaner that way).

Verification methods, easiest first:
- **DNS TXT record** — we add one line to the domain's DNS. Sam doesn't see anything change.
- **HTML file upload** — we add a file to the repo. Auto-deploys.
- **Google Tag Manager** — heavier, only if we're using GTM anyway.

We'll handle the verification. Sam just needs to confirm we can use the same Google account.

---

## 4. Social account access

The site links out to:
- WhatsApp: `wa.me/447383449899` — that's Sam's number. No access needed from us.
- Instagram: `@chap1ins` — we may want admin or business-account collaborator access for posting.
- Facebook: `facebook.com/share/1KijnQff8t` — same, page admin or editor role.
- TikTok: `@chap1ins` — usually one login, Sam holds it.
- Snapchat: `t/sfwvVejs` — usually one login, Sam holds it.

What we need from Sam, per platform:
- **Instagram** — switch to a business account if not already. Add Conversion Forge as a collaborator (his preferred email or our agency Instagram).
- **Facebook page** — add us as Editor or Admin (Settings → Page Roles).
- **TikTok / Snapchat** — Sam keeps the logins. We'll send him the post copy and assets; he posts.

If Sam wants us to handle social posting, we need full passwords (saved in his password manager, shared via secure link). If he just wants the website live and he handles socials himself, none of this matters.

---

## 5. Google Analytics

Optional but cheap to add. Useful for "how many people opened the site this week" and "which page they looked at."

If Sam wants this:
- We create a Google Analytics 4 property under his Google account.
- We add the tracking script to the site (one tag, automatic).
- Sam gets a monthly summary email.

If Sam doesn't want this — fine, leave it off. Privacy-respectful.

---

## 6. Photo asset access — for the weekly cut-photo sync

The script `chaplins-cut-sync` is already built. It pulls new cut photos from a Google Drive folder, optimises them (web-sized webp), and adds them to the website's gallery. Runs every Sunday night.

For this to work:
- Sam creates a Google Drive folder called `Chaplins Cuts` (or similar).
- He shares it with our service account email (we'll provide the address).
- He drops in any new photos he takes during the week.
- Sunday night, they appear on the site.

If he doesn't take many photos, this can wait. We'll set it up dormant.

---

## 7. The phone number on the site

Currently displayed: `+44 1732 712861` (the shop landline).

Sam to confirm:
- Is this still the right number?
- Does he want the shop landline, his mobile, or WhatsApp shown as primary contact?
- Is he OK with the JSON-LD telephone field being public (it appears in Google's knowledge panel)?

---

## 8. Email forwarding (recommended if we register a domain)

If Sam gets a custom domain, we set up:
- `info@chaplinsbarbers.co.uk` → forwards to Sam's personal email
- Optionally `book@chaplinsbarbers.co.uk` → also forwards to Sam (or to WhatsApp Business)

Both free with the registrar. Useful for "I prefer email" customers.

---

## 9. Payment / booking system

Not currently on the site. Booking is via WhatsApp.

Question for Sam:
- Does he want an online booking system added later? (e.g. Booksy, Fresha, Square Appointments — most have free tiers for one-chair shops.)
- Or does WhatsApp work fine and he doesn't want the friction of another system?

If yes, that's a phase 2 build. If no, leave WhatsApp as the booking channel.

---

## 10. Anything Sam wants changed

The site has Sam's voice profile committed to the repo. Before we go live, he should look through the live preview at:
**`https://tokelomogorosi-ctrl.github.io/chaplins-barbers-website/`**

And tell us:
- Anything that doesn't sound like him.
- Anything that's wrong (price, opening hours, service description).
- Anything missing he'd like added (a service he offers, a photo of the chair, a sound clip).
- Whether the music tracks playing in the gallery section feel right.

Once he's signed off, we propagate to the real domain and submit to Google.

---

## What happens after sign-off

1. Domain pointed at the site (DNS propagation takes a few hours).
2. GSC verified, sitemap submitted.
3. GBP updated with opening hours, services, photos, website link.
4. Aftercare handover document delivered to Sam — explains how to update content, how to reach us, what runs automatically.
5. Site is live. We tell Sam where to send people.

Total turnaround once the items above are answered: about a week (mostly waiting on Google to crawl and propagate).

---

## Where Sam should send replies

Single thread, single channel. Director's preference, not Sam's choice.

Once Sam has gone through this list, he replies in one message and we wire it all up in one go.
