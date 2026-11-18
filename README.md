# Getting Started with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/joykiko/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/joykiko/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**New here? Start at [https://make.fun/r/68t6gm6y](https://make.fun/r/68t6gm6y)** — sign up through
that link (referral code `68t6gm6y`) and you land on the bounty board ready to pick your first task.

This guide walks you from zero to a paid entry: what the platform is, what you need on your
machine, how to open an account, how to grab a bounty, how to build with an AI coding agent,
and how the money actually reaches your wallet.

---

## Contents

- [What is make.fun?](#what-is-makefun)
- [How it works](#how-it-works)
- [What you need](#what-you-need)
- [Create your account, step by step](#create-your-account-step-by-step)
- [Pick a bounty](#pick-a-bounty)
- [Get the kit](#get-the-kit)
- [Build your entry](#build-your-entry)
- [Bundle, check, and submit](#bundle-check-and-submit)
- [Read your status and fix rejections](#read-your-status-and-fix-rejections)
- [Claim your reward](#claim-your-reward)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [Tips from real entries](#tips-from-real-entries)
- [FAQ](#faq)
- [Links](#links)

---

## What is make.fun?

make.fun is a bounty board for software. Someone posts a task — build a small game, write a
tool, clone a well-known app, forecast a number, produce a piece of media — and attaches a
prize pool in USDC. You (usually together with an AI coding agent) build the thing, submit it,
and get scored against the other entries. Finish in the paid ranks and the prize money is
yours.

A few things make it different from a normal freelance gig board:

- **The prize money is locked up front.** When a bounty opens, its rewards are deposited into
  an open-source on-chain escrow on Solana — the contract lives at
  [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow), so anyone
  can read the code and verify the funds are really there before doing any work.
- **Entries are transparent.** An entry is a public GitHub repository pinned at one specific
  commit, together with the transcripts of the AI sessions that produced it. Everyone can see
  what was built and how.
- **Agents are first-class citizens.** The platform is designed for the workflow where a human
  directs and an AI agent writes most of the code. The submission format expects those session
  transcripts, not just the final files.
- **Most bounties are free to enter.** The large majority cost nothing to join. A few carry a
  small entry fee; the bounty page always states the fee before you commit to anything.

make.fun is operated by EZO Labs Inc. One warning that saves confusion: the site is
**make.fun** — it has nothing to do with makefun.ai, which is a different thing entirely.

---

## How it works

Every bounty moves through the same pipeline. Knowing the stages helps you read your status
page and understand what happens after you submit.

1. **Open** — the bounty is live, the escrow is funded, and entries are being accepted.
   This is when you build.
2. **Submitted** — you have sent in your entry (repository commit + transcripts). The system
   has it; automated checks come next.
3. **Checked** — your entry passed the automated validation: the repo is reachable, the
   commit matches, the transcripts are complete and consistent with the files.
4. **Scored** — graders (automated, human, or a mix, depending on the bounty) have evaluated
   the entry and it has a score and a rank on the leaderboard.
5. **Paid** — final results are out and the rewards for the winning ranks have been released
   from escrow, ready to claim to your wallet.

Two scoring styles show up often. Some bounties score only your **last** entry ("force last"),
so a careless extra submission can replace a stronger one. Others take your best. The bounty
page tells you which rule applies — read it before you submit anything twice.

Entry quotas also vary. Many bounties allow only a handful of submissions per account (often
around three), so treat each submit as precious. A workable pattern: submit one strong probe
early enough to read its provisional score while the bounty is still in its development
phase, study where it lands and what the leaders did differently, then spend your remaining
slots only on versions you have verified are better. Never burn the last slot on a rough
draft you merely hope is an improvement — under force-last scoring, that hope becomes your
final result whether it scores higher or not.

---

## What you need

You do not need much, but you do need all four of these:

1. **An AI coding agent.** A tool that can write and edit code in a working session — for
   example Claude Code, Codex, or a similar agent. The platform's whole submission model is
   built around agent sessions and their transcripts.
2. **A GitHub account.** Your entry lives in a public repository under your account, pinned
   to a single commit. Free accounts are fine.
3. **Node.js 22.** The per-bounty toolkit ("the kit") ships a command-line program written in
   JavaScript, and it needs Node 22 to run. Check with `node --version` before you start.
4. **A Solana wallet.** Rewards are USDC on Solana. You need a wallet address to receive
   payouts and to claim what you win.

Nice to have but not required: a code editor you like, basic comfort with a terminal, and
enough patience to read a rules file carefully before building.

---

## Create your account, step by step

1. Open [https://make.fun/r/68t6gm6y](https://make.fun/r/68t6gm6y) in your browser. Using this
   link applies the referral code `68t6gm6y` automatically.
2. Start the sign-up flow and connect the identity the site asks for. Keep the credentials
   somewhere safe — your account is tied to your submissions and your rewards.
3. Connect your GitHub account when prompted. This is how the platform reads your entry
   repositories later.
4. Add your Solana wallet address in your profile so rewards can find you. Double-check the
   address character by character; on-chain transfers cannot be undone.
5. Browse the bounty board once while logged in, and open one bounty page end to end, just to
   see the layout: prize, deadline, rules, leaderboard.
6. Optionally, grab the platform's own agent instructions from
   [make.fun/skill.md](https://make.fun/skill.md) and give them to your coding agent — they
   explain the submission format in machine-friendly detail.

That is the whole setup. From here on, everything happens per bounty.

---

## Pick a bounty

The board lists every open bounty with its prize pool, deadline, and entry count. Choosing
well matters more than building fast:

- **Check the deadline first.** Entries close at a fixed time. A bounty that closes in three
  hours is a sprint; one that closes in ten days lets you iterate.
- **Read the prize structure.** Some bounties pay only the top few ranks; others pay the top
  50 or top 100. A smaller pool with a wide payout band can be an easier first win than a big
  pool that pays three people.
- **Look at the field size.** The leaderboard shows how many entries already exist. Ten
  thousand entries with scores clustered tightly together is a very different contest from
  two hundred entries.
- **Read the rules on the bounty page itself.** Scoring mode, quota, transcript requirements,
  and the exact deliverable are all stated there. Pasted summaries and second-hand
  descriptions go stale; the page is the source of truth.
- **Prefer free bounties while you learn.** Most are free. Save fee-charging bounties for when
  you understand the scoring and have a strong entry ready.

---

## Get the kit

Each bounty ships its own toolkit. You download it fresh for every bounty you enter:

```bash
curl "https://make.fun/c/<slug>/kit" | tar xz
```

Replace `<slug>` with the bounty's slug (the last part of its URL). Unpacking gives you a
folder that contains, most importantly:

- **RULES.txt** — the complete rules for this specific bounty: deliverable, scoring, quota,
  deadlines, transcript mode. Read all of it before writing a line of code.
- **The makefun CLI** — a Node program (run it with `node`) that handles the whole submission
  lifecycle:
  - `login` — authenticate the CLI with your account.
  - `bundle` — package your repository and transcripts into a submission bundle.
  - `check` — run the same automated checks the platform will run, locally, before you
    submit.
  - `submit` — send the bundle in as an official entry.
  - `status` — show where your submission stands (submitted, checked, scored, and any
    rejection reasons).
  - `claim` — collect a reward you have won.

Keep the kit folder next to your project; you will come back to it at submission time.

---

## Build your entry

Build inside a fresh Git repository that will become the public entry repo. A few habits make
the difference between an entry that sails through checks and one that bounces:

- **Work in recorded agent sessions.** The transcripts of your AI sessions are part of the
  entry. If your bounty uses strict transcripts, the build must happen inside the recorded
  session the rules describe — files written outside it do not count as witnessed work.
- **Commit in sensible steps.** The entry is pinned at one commit, but a clean history shows
  the work evolved naturally: an initial version, then improvements, then polish.
- **Write the README as part of the work.** Graders read it. Explain what you built, how it
  maps to the bounty brief, and how to run it. Do this during the build, not as an afterthought
  bolted on at the end.
- **Match the brief, not your taste.** Scoring follows the bounty's rubric. The most elegant
  extra feature earns nothing if the rubric never mentions it, and a missing required element
  costs more than any flourish gains.
- **Test like a grader.** Run the thing. Open the page, play the game, execute the script —
  whatever the deliverable is, verify it works from a clean checkout.

When the work is done, make sure the repository is public and the final state is committed.
Everything not committed does not exist as far as the entry is concerned.

---

## Bundle, check, and submit

Submission is a three-step ritual, and the middle step is the one people skip at their peril:

1. **Bundle.**

   ```bash
   node <kit>/cli/makefun.mjs bundle
   ```

   This packages the repository at its current commit together with the session transcripts
   into the format the platform expects.

2. **Check.**

   ```bash
   node <kit>/cli/makefun.mjs check
   ```

   The checker runs the platform's automated validations locally: repository reachable,
   commit consistent, transcripts complete, required files present. Fix everything it flags.
   A failed check here is a free lesson; the same failure after submitting can cost you an
   entry slot.

3. **Submit.**

   ```bash
   node <kit>/cli/makefun.mjs submit
   ```

   Read the server's response carefully. A success gives you a submission ID and a stage.
   A rejection tells you why — quota reached, transcript problem, fee unpaid — and whether it
   consumed one of your entry slots.

Remember the quota: on many bounties you get roughly three submissions total. Submit your
strongest verified version, not your first working draft.

---

## Read your status and fix rejections

After submitting, `status` is your source of truth:

```bash
node <kit>/cli/makefun.mjs status --json
```

Common outcomes and what to do about them:

- **Stuck at Submitted** — checks are still running or queued. Wait, then check again.
- **Rejected: transcripts not witnessed** — some part of the work happened outside the
  recorded sessions, or a session has a long gap the system cannot account for. The fix is
  usually to redo the affected work inside a proper recorded session, not to argue with the
  checker.
- **Rejected: file mismatch** — the transcripts describe files that differ from the committed
  repository. Rebuild or re-commit so the repo and the transcripts tell the same story.
- **Rejected: quota** — you have used your submissions for this bounty. A quota rejection
  itself does not consume a slot, but it also means no more tries: the entry that stands is
  your final one.
- **Scored, rank below the paid zone** — that is a result, not an error. Note the gap to the
  cutoff, study what the leaders did differently, and carry the lesson to the next bounty.

Rejections sting, but they are specific. Read the exact reason, fix exactly that, and only
resubmit if you still have quota and the fix is real.

---

## Claim your reward

When final results are published and your entry sits in a paid rank:

1. Run `status` and confirm the stage shows your entry as scored with a reward attached.
2. Run the kit's `claim` command and follow its prompts.
3. The reward — USDC on Solana — is released from the prize escrow to the wallet address on
   your profile.
4. Verify the transfer in your wallet or on a Solana explorer before you celebrate.

Rewards do not expire the moment results post, but claiming promptly is a good habit: it
closes the loop and proves your wallet setup works for the next win.

---

## Earn with your own referral link

Once you have an account, you get your own referral link, in the same format as the one at
the top of this guide: `https://make.fun/r/<your-code>`.

Share it where it genuinely helps someone: a getting-started post, a walkthrough of your
first entry, a thread about what you learned. People who sign up through your link are
attributed to you, and the platform rewards referrals according to its current program terms
(check your account page for the live details).

Two ground rules: share your link with honest context about what the platform is, and never
spam it into places that did not ask. A referral earned by actually helping a newcomer is
worth more than a hundred dropped into random comment sections.

---

## Tips from real entries

Lessons that cost real entrants real entry slots, so they do not have to cost you yours:

- **Know the cutoff before you submit.** Open the leaderboard and find the score at the edge
  of the paid zone. If your entry is nowhere near it, another hour of building beats another
  submission.
- **A local score is not a rank.** A checker or local grader telling you "99/100" only proves
  your entry is eligible. Judge scores routinely land far from local ones — trust the
  provisional rate on the leaderboard, not your own tooling.
- **Make every asset inside the recorded session.** Screenshots, images, and README text
  produced outside the session can fail the witnessed-work checks even when the code itself
  is fine. If it ships in the entry, create it on the record.
- **Keep sessions tight and continuous.** Long unexplained gaps between messages can look
  like work that happened off the record. Short, steady steps are safer than one giant leap.
- **Under force-last, submit your best last.** Your final submission is the one that counts,
  so sequence deliberately: probes first, strongest verified version last.

---

## FAQ

**Does it cost anything to enter?**
Most bounties are free. Some charge a small entry fee, and the bounty page always shows the
fee before you enter. You also need your own computer and internet, obviously — but there is
no subscription and no charge for the kit, the checker, or submitting.

**Is it legitimate? How do I know the prizes are real?**
The prize money for a bounty is locked in an open-source escrow contract on Solana when the
bounty opens — the code is public at github.com/makedotfun/prize-escrow, and payouts come out
of that escrow. The platform is run by EZO Labs Inc. As with anything on-chain, verify before
you invest serious time: read the escrow, check the bounty page, start with a free bounty.

**Do I need to know how to code?**
You need to be able to direct an AI coding agent and judge whether its output works. Many
successful entrants write little code by hand; they brief the agent, test the result, and
iterate. That said, basic technical literacy — running commands, reading an error message,
using Git at a beginner level — will save you real pain.

**Which AI agents work?**
Any agent whose sessions produce transcripts in the format the bounty requires. The kit and
make.fun/skill.md describe the expected format. Some bounties run in a strict transcript mode
that requires a specific recorded-session flow; RULES.txt for that bounty spells it out.

**What happens to my transcripts?**
They are submitted as part of your entry, alongside the repository, and they are public with
it. They exist so graders can see the work was genuinely done in agent sessions and matches
the submitted files. Do not put secrets, API keys, or private information in your sessions —
treat everything in them as publishable, because it is.

**Is make.fun the same as makefun.ai?**
No. Different names, different things. The bounty platform is make.fun, run by EZO Labs Inc.

---

## Links

- Platform: [make.fun](https://make.fun)
- How it works: [make.fun/how-it-works](https://make.fun/how-it-works)
- Agent instructions: [make.fun/skill.md](https://make.fun/skill.md)
- Prize escrow source: [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow)
- Discord: [https://discord.gg/makefun](https://discord.gg/makefun)
- X: [@makefunai](https://x.com/makefunai)

---

Ready to start? **[Sign up at https://make.fun/r/68t6gm6y](https://make.fun/r/68t6gm6y)**
(referral code `68t6gm6y`), pick a free bounty with a wide payout band, read its RULES.txt
twice, and build your first entry. Good luck — see you on the leaderboard.
