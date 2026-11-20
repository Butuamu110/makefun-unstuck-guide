# makefun-unstuck-guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/butuamu110/makefun-unstuck-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/butuamu110/makefun-unstuck-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

Most getting-started guides assume everything works the first time. Real life is ruder than that: the sign-in loops, the wallet refuses to link, the server rejects your entry at 11 pm. **Unstuck — A Troubleshooting-First Guide to Your First make.fun Bounty** flips the usual tutorial around. It starts with the fastest happy path, then spends most of its pages on the moments where new bounty hunters actually get stuck — each one written as a symptom you can recognise, the likely cause behind it, and the fix that gets you moving again. Read it top to bottom before your first entry, or keep it open in a tab and jump straight to the error you are staring at.

## The 15-minute path

If nothing goes wrong, this is genuinely all there is to it:

1. **Sign up** at [make.fun](https://make.fun/r/gcjdenbh) — that link carries this guide's referral code, so the account you create is counted as one of the humans this guide brought in.
2. **Link GitHub** on your profile. Your entry will live in a public repository, and the repository's owner has to be the GitHub account linked here — no exceptions, no workarounds.
3. **Link a Solana wallet.** Prizes are paid on chain to the wallet that signs your entry, so link the wallet you actually want to be paid to.
4. **Pick a bounty** from the open list and read its requirements page end to end before you build anything. Deadlines, entry caps and file rules differ per bounty.
5. **Enter**: build the thing, push it to your public repo, submit the repo URL and the full commit SHA, and check the entry status until it shows as scored.

Done? Congratulations — you may never need the rest of this page. Stuck somewhere in those five steps? That is exactly what the rest of this page is for.

## How to use the troubleshooting chapters

Every problem below follows the same pattern:

- **Symptom** — what you see on screen.
- **Likely cause** — the most common reason it happens.
- **Fix** — the steps that resolve it, in order.

Work through the fixes in order and re-check after each one. Nine times out of ten the first fix is the one.

One more habit worth building: change one thing at a time, so you always know which fix actually worked.

## Stuck on sign-in and Discord

### Symptom: the Discord sign-in loops back to the login page

**Likely cause:** a stale session cookie, or the make.fun tab and the Discord tab disagreeing about which account is signed in.

**Fix:**

1. Sign in to Discord first, in the same browser, and confirm you are on the right Discord account.
2. Go back to make.fun and use the Discord sign-in again — with Discord already authenticated, the hand-off completes in one hop.
3. Still looping? Clear cookies for both sites and repeat. If you juggle several accounts, give each account its own browser profile; mixed cookies are the number one cause of this loop.

### Symptom: "this account is already registered" or the wrong make.fun account opens

**Likely cause:** your Discord identity is already tied to a make.fun account — possibly one you created weeks ago and forgot.

**Fix:** sign in with that same Discord account and look at the profile that opens: its handle, referral link and entries are the account you own. Accounts are anchored to identities, so the practical move is to use the account that exists rather than fight to create a duplicate.

### Symptom: a CAPTCHA or "new login location" check appears

**Likely cause:** Discord protecting the account because the browser, device or network looks new.

**Fix:** complete the check yourself, slowly, in the browser you actually use. Authorise the new location from the email Discord sends if it asks. These checks are personal by design — no tool can or should pass them for you.

## Stuck on wallet linking

### Symptom: the wallet connects in the extension but the profile still says "Not linked"

**Likely cause:** the web extension link and the account's payout wallet are two separate things. The profile status only changes when the wallet is linked to the account itself, not when an extension merely connects to a page.

**Fix:** use the profile's own "link a wallet" flow and approve the signature in your wallet. Refresh the profile afterwards and confirm the address shown is the one you expect to be paid to.

### Symptom: "wallet already in use" when linking

**Likely cause:** one wallet belongs to exactly one make.fun account. If that wallet was ever used to sign in or register another account, it is that account's wallet now.

**Fix:** either use the account the wallet already belongs to, or link a different wallet to this account. There is no merge and no transfer — pick deliberately, because the signing wallet is also the payout wallet for your entries.

### Symptom: the approve dialog opens but nothing ever confirms

**Likely cause:** the signature request is waiting in the wallet extension, or the wallet is on the wrong network or locked.

**Fix:** unlock the wallet, open the extension manually and look for a pending signature request, and make sure you are approving a signature (free) rather than a transaction. If the request expired, cancel it on the site and start the link flow again so a fresh request is issued.

## Stuck on GitHub linking and repo ownership

### Symptom: the entry is refused because the repository is not yours

**Likely cause:** the repo sits under a different GitHub account than the one linked to your make.fun profile. Ownership is compared by account, not by who has push access.

**Fix:** check which GitHub login your make.fun profile shows, then create (or move) the repository under exactly that account. A claim file inside the repo does not substitute for ownership on guide bounties like this one.

### Symptom: the repository check fails even though the repo is public

**Likely cause:** a typo in the URL, the repo was made private after the fact, or the commit SHA you submitted is not on any branch of that repo.

**Fix:** open the repo URL in a private/incognito window — if you cannot see it logged out, neither can the checker. Then copy the full 40-character SHA of the commit you mean, from the branch you pushed, and resubmit with the pair that matches.

## Stuck on an entry the server rejected

### Symptom: the submission comes back with one or more failed checks

**Likely cause:** something specific in the entry does not match the bounty's rules — and the good news is that the failing check tells you what. Rejections on make.fun are diagnostic, not personal.

**Fix:**

1. **Read the failing check's name and its stated fix.** Do not guess; the reason names the exact file, field or condition that failed.
2. **Fix only the named cause.** A missing LICENSE means add the license file — it does not mean rebuilding your whole entry.
3. **Commit and resubmit before the deadline**, with the new commit SHA. A rejected entry is not the end of the run while the competition is still open and retries are allowed.

### Symptom: the entry was accepted and scored, but it sits far below the paid places

**Likely cause:** nothing is broken — ranking is comparative. Your score is measured against every other entry in the field, thousands of entries chase a few dozen paid places, and the top of the board is usually saturated with near-perfect scores. A low rank is a position in a race, not an error message.

**Fix:**

1. **Measure the gap before you react.** Compare your entry's score against the score at the last paid place, not against rank 1 — the only distance that matters is the one to the paid line.
2. **Study the current top entries** and name, concretely, what they do that yours does not. "They are better" is not a finding; "they show X and mine doesn't" is.
3. **Let the standing entry stand.** Never resubmit a weaker or unproven variant over a live entry — under a last-entry-counts rule, the new one replaces it, and a guess can leave you worse off than the entry you already had.
4. **Spend the remaining time where the gap is closable** — a bounty where your score sits just under the paid line is worth more effort than one where the top is out of reach.

## Stuck on transcripts and recordings

### Symptom: the bundle or recording will not seal, or the seal does not verify

**Likely cause:** the recorder was stopped before it finished writing, or files in the entry folder changed after the recording was sealed.

**Fix:** let the recorder close cleanly and verify the seal before you submit anything. If the seal fails, record a fresh session over the finished entry rather than trying to repair a broken record — a clean short recording beats a long doubtful one.

### Symptom: checks complain that files in the entry were not written by the agent

**Likely cause:** large files were produced by a generator script, pasted in, or downloaded, so the transcript shows no session actually authoring them.

**Fix:** have the agent write the entry's files directly, in the session, including the big ones. Reference material can be read, but the deliverable's lines need to be authored in the recorded work itself.

### Symptom: two builds were recorded at the same time and both records look wrong

**Likely cause:** a recorder watches the machine's sessions, so parallel recorded builds contaminate each other.

**Fix:** run recorded builds one at a time. Finish and seal the first before starting the second.

## Stuck on getting paid

### Symptom: the results are out and your prize has not arrived

**Likely cause:** claiming is a step of its own. Prizes are paid to the wallet that signed the entry, after the results are final and the claim is made.

**Fix:** check your entry's final place against the paid places first — only placed entries pay. If you placed, run the claim flow from your account and verify the payout wallet address is the one you linked. Keep the claim details the status command shows you; you will need them if anything needs support.

### Symptom: you placed, but with the wrong wallet

**Likely cause:** the signing wallet is fixed at submission time; it cannot be swapped afterwards.

**Fix:** there is no fix after the fact — which is why the wallet chapter above insists you link deliberately before you enter. For the next bounty, link and sign with the wallet you want paid.

## Run it

Two commands cover most of the "what does this bounty actually want" questions:

```sh
# Read a competition's official requirements (fields, checks, deadlines)
curl -s https://make.fun/api/competitions/bring-the-humans-02/requirements

# Show your entries, their status and any claim details
node cli/makefun.mjs status
```

Run them from inside the unpacked competition kit, and re-check `status` after every submission until the entry shows as scored.

## Before you submit: the 60-second checklist

Sixty seconds now beats a rejection later. Every item below is something the server will check anyway — run through them while you can still fix what fails:

- [ ] **The repo is public.** Open its URL in a private/incognito window; if you can't see it logged out, the checker can't either.
- [ ] **The repo's owner is the GitHub account linked to your make.fun profile** — not just an account you have push access to.
- [ ] **A LICENSE file sits at the repo root** (MIT is fine) — no license file, no entry.
- [ ] **The README carries your own referral link** — your code, from your profile, not the one from whatever guide you read. (This guide's is `gcjdenbh`; yours is different, and that difference is the whole point.)
- [ ] **screenshot.png is at the repo root**, next to the README — a screenshot of the guide as readers will see it.
- [ ] **The commit you are about to name is pushed** and is the one on the branch — copy its full 40-character SHA, not the short version.
- [ ] **You are signing with a wallet that belongs to this account** — that wallet is also where any prize lands, so check the address once more.
- [ ] **The deadline has not passed.** Check the requirements page for the closing time in UTC and convert it to your timezone before you start celebrating.

All eight ticked? Submit — and afterwards, check the entry's status until it shows as scored.

## FAQ

**Is make.fun free to enter?**
Most bounties are free to enter from your account; a few name an entry fee in their requirements. The requirements page always says so up front — read it before you build.

**How many entries can I submit?**
Each competition sets its own cap per account per day, and some accounts have lower caps. The status command shows your remaining room; never burn your last slot on an untested variant.

**Can I enter the same bounty from two accounts with the same guide?**
No. An entry whose files are identical to another account's earlier entry is refused, and every account's entry has to be its own work with its own angle, structure and wording — like this guide differing from a plain tutorial.

**Which wallet receives my prize?**
The wallet that signed the entry. Link it carefully: one wallet belongs to one account, and the signer cannot be changed after submission.

**My entry was rejected. Is my run over?**
Usually not. Read the failing check, fix the named cause, commit, and resubmit while entries are still open. A rejection with a fixable reason is information, not a verdict.

**Do I need to be a programmer to win?**
Entries are built by AI agents working from your instructions, so your leverage is judgement: picking the right bounty, reading its requirements properly, and checking the result honestly before it goes in.

**Where does my referral link live?**
On your make.fun profile. This guide's is [make.fun/r/gcjdenbh](https://make.fun/r/gcjdenbh) — sign up through it and you are one of the humans this entry brought in.

---
<sub>Entered on [make.fun](https://make.fun/?ref=gcjdenbh&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>
