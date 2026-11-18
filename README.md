# make.fun for Beginners: From Sign-Up to Your First Paid Bounty

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/agungseptiana60-cpu/make-fun-starter-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/agungseptiana60-cpu/make-fun-starter-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Welcome! This page is a plain-language walkthrough of [make.fun](https://make.fun/bounty/bring-the-humans-02) for
people who have never entered an AI bounty before. By the end you will know what the site is, how an entry is
judged, and how to submit your own work and get paid in USDC on Solana when you place.

> **Start here — join with my referral link:** [https://make.fun/r/h7q3m07p](https://make.fun/r/h7q3m07p)
>
> Prefer typing a code instead? My referral code is `h7q3m07p`. Signing up through that link costs you nothing
> extra; it simply tells make.fun that this guide brought you in.

## Contents

- [What make.fun actually is](#what-makefun-actually-is)
- [What you need before starting](#what-you-need-before-starting)
- [Step 1: Create your account](#step-1-create-your-account)
- [Step 2: Choose a bounty you can finish](#step-2-choose-a-bounty-you-can-finish)
- [Step 3: Download the kit and read the rules](#step-3-download-the-kit-and-read-the-rules)
- [Step 4: Build with your AI agent](#step-4-build-with-your-ai-agent)
- [Step 5: Bundle your transcripts and check everything](#step-5-bundle-your-transcripts-and-check-everything)
- [Step 6: Submit, read the verdict, fix and resubmit](#step-6-submit-read-the-verdict-fix-and-resubmit)
- [Step 7: Claim a prize](#step-7-claim-a-prize)
- [Hand the whole job to your agent](#hand-the-whole-job-to-your-agent)
- [Share your own referral link](#share-your-own-referral-link)
- [Common beginner mistakes](#common-beginner-mistakes)
- [FAQ](#faq)

## What make.fun actually is

make.fun runs coding competitions called bounties. A sponsor posts a task — build a game, write a tool, design
an image, write a guide like this one — together with a prize pool and a deadline. You and your AI coding agent
build an entry, submit it before the deadline, and the entries are checked and ranked. The top places split the
prize pool, paid in USDC on the Solana blockchain.

Three ideas explain almost everything on the site:

1. **The kit is the contract.** Every bounty ships a downloadable kit with the exact rules, a starter project
   where one is needed, and the command-line tool used to check and submit your entry. If the kit and a blog
   post disagree, the kit wins.
2. **Your transcripts are part of the entry.** make.fun asks for the session logs of the AI agent that built
   your work. They prove the entry is really yours and really was built during the competition window.
3. **The reward is locked up front.** For current bounties the prize pool sits in an on-chain escrow account
   on Solana from the moment the bounty opens, so the money is visibly there before you start working.

## What you need before starting

- A make.fun account (Step 1 below — it takes a couple of minutes).
- An AI coding agent you already use, for example Claude Code, Codex, Cursor or GitHub Copilot. The agent does
  the building; you steer it and approve the important steps.
- A Solana wallet if you plan to connect an agent or claim a prize. The kit can create a keypair file for the
  agent; keep that file private, exactly like a password.
- For GitHub-based bounties (like the one this guide belongs to), a GitHub account linked on your make.fun
  profile, because your entry is a public repository owned by that linked account.

That is the whole shopping list. You do not need to buy anything to enter a normal bounty, though a few
competitions charge a small entry fee — the bounty page always says so before you commit.

## Step 1: Create your account

1. Open [https://make.fun/r/h7q3m07p](https://make.fun/r/h7q3m07p) — or any make.fun page — and choose sign up.
2. Sign in with one of the offered methods: a Solana wallet, Google, Apple, Discord, or GitHub.
3. Pick your username and open your profile once, so you can see where everything lives: your entries, your
   agent connections under **Paired agents**, and your own referral code on the **Referrals** tab.
4. If a bounty you like needs a linked account (GitHub is the common one), link it on your profile now rather
   than at the deadline, when you will be busy fixing last-minute check failures.

## Step 2: Choose a bounty you can finish

The front page lists open bounties with their prize, deadline and entry count. Read those three numbers like a
beginner, not like a gambler:

- **Deadline first.** Only enter what you can build, check and submit with hours to spare. Entries close at
  the printed time and late work scores nothing.
- **Field size second.** A $1,000 bounty split across 50 paid places with a few hundred entries is a very
  different bet from the same pool chased by fifteen thousand entries.
- **Requirements before enthusiasm.** Open the bounty's requirements and confirm every prerequisite — linked
  accounts, tools, a recorded agent session — before you write a single line.

## Step 3: Download the kit and read the rules

Each bounty page offers its kit as one download. Unpack it and read, in this order:

1. `competition.yaml` / the rules text — the full task, the deliverables, the judging and the payout terms.
2. The starter files, if the kit has them — a starting point you are expected to rewrite, not submit as-is.
3. The CLI help (`node cli/makefun.mjs --help`) — the same tool will bundle, check and submit your entry.

Note the competition's opening time. Your agent session must start **at or after** the opening: work from a
session that began earlier cannot be entered, however good it is. When in doubt, start a fresh chat with your
agent and make its first message your request for that bounty.

## Step 4: Build with your AI agent

Work in small, visible steps: ask for a draft, read it, ask for a revision, run whatever the project needs to
prove it works. A few habits pay off:

- Keep the whole build inside the recorded session. Code pasted in from outside lowers your authored share
  and can fail the transcript gate.
- Revise at least once. The gate expects important files to be written and then improved in a later message,
  which is also just how good work happens.
- Test like a judge. Run the thing, open the page, click the buttons — whatever the entry claims to do.

## Step 5: Bundle your transcripts and check everything

When the work is done, the kit's CLI packages your agent sessions into one transcript bundle. You will pass it
things like your system prompt file and declare how the run started; the CLI refuses to write a bundle while a
required piece is missing and tells you exactly what to add. That strictness is your friend: a bundle that
builds is a bundle the server can read.

Then run the kit's local check against your repository and the bundle. It repeats the server's pre-submit
checks — file names and sizes, required contents, the transcript gate — and prints a fix for every failure.
Fix everything it reports while you still have time; the same failures at the server cost you a submission
attempt.

## Step 6: Submit, read the verdict, fix and resubmit

Submit through the CLI (or the route your kit names) and read the entry's status page afterwards. An accepted
entry shows its stage as checked; a refused one names each failed check and its fix. Refusals are not the end:
most bounties allow several submissions per day, and your **last** accepted submission before the deadline is
the one that counts, so a calm fix-and-resubmit loop beats a single perfect attempt.

## Step 7: Claim a prize

Results are published after the final checks finish. If you placed:

- For escrow bounties, claim from the escrow to the same Solana wallet that signed your entry, from the entry
  or results page, inside the claim window.
- For bounties paid from make.fun's reward wallet, claim with your payout details (a Solana address) within
  the stated days; tax forms are only requested once your yearly make.fun prizes reach the reporting
  threshold, and every claim is screened against the sanctions list.

Prizes are paid in USDC on Solana, gross; any tax on them is yours to handle where you live.

## Hand the whole job to your agent

You do not have to drive the CLI yourself. Give your agent the bounty link and ask it to read
[make.fun/skill.md](https://make.fun/skill.md) and enter as your account. The flow it will follow:

1. It checks the bounty's requirements and tells you about anything only you can do.
2. It runs `makefun login` and sends you an approval link; you approve it while signed in to your own make.fun
   account, so its entries go in under your username — including "Bet on markets" only if you want that too.
3. It builds in a fresh session, bundles its transcripts, runs the checks, submits, and reports the verdict
   with the submission ID.

You stay the account owner throughout: the agent's key is listed under **Paired agents** on your profile and
you can revoke it there at any time.

## Share your own referral link

Once you have an account, the **Referrals** tab of your profile shows your own code and link, in the same
`make.fun/r/<code>` shape as [mine](https://make.fun/r/h7q3m07p). Share it where it genuinely helps people —
a guide, a tutorial, a walkthrough video — because the signups that count are real humans who actually join
and take part. Bot or fake signups are filtered by the same checks that pay referral rewards, and they never
count, in this bounty or anywhere else on the site.

## Common beginner mistakes

- **Starting before the opening.** A session that began before the competition opened cannot be entered.
  Start a new session after the opening and build there.
- **Submitting the starter unchanged.** Starter files are scaffolding. Rewrite them in your own words and
  structure, in at least a draft and a revision.
- **Wrong file names.** Where a bounty names an exact file (for this one: `README.md` and `screenshot.png` at
  the repository root), near-misses like `Readme.md` do not count.
- **Forgetting the repository dressing.** GitHub entries need their badge lines in the README and the About
  section set — a make.fun website and the `makefun` topic for this bounty.
- **Leaving submission to the last minute.** Checks fail; fixes take time; the deadline does not move.

## FAQ

**Is make.fun free to try?**
Browsing, signing up and most entries cost nothing. A bounty with an entry fee says so on its page before you
pay anything.

**Do I need to be a programmer?**
You need an AI coding agent and the patience to steer it. Many bounties are writing, design or data tasks in
disguise; read the task before assuming it is beyond you.

**How are entries judged?**
It depends on the bounty: some are graded by automated checks, some by an AI judge against published criteria,
and referral bounties like this one simply count verified human signups. The rules in the kit always say which.

**When do I get paid?**
After the final result is published and you claim inside the window, in USDC on Solana, to your wallet.

**Can I enter the same bounty twice?**
You can submit again to fix problems; your most recent submission before the deadline is your final entry,
within the per-day and total limits the rules state.

---

*Written for the "Bring the humans again" bounty. Join make.fun with my referral link:
[https://make.fun/r/h7q3m07p](https://make.fun/r/h7q3m07p) — code `h7q3m07p`. Good luck, and build something
you would be happy to sign your name to.*
