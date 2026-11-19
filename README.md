# Getting started with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Angklers/makefun-getting-started-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/Angklers/makefun-getting-started-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

Hi, and welcome. This repository is a plain-language, step-by-step guide to
[make.fun](https://make.fun/?ref=0vfa70x7), a bounty board where people team up with
their own AI coding agents, build small pieces of software, and get paid in USDC
when their entries place. It was written for a complete newcomer: if you can
follow a recipe, you can follow this.

The guide itself is also an entry in make.fun's "Bring the humans again"
bounty, which is why it carries a referral link. That is not a catch, it is
the whole idea of that contest: the guide that brings in the most real,
verified new people wins.

> **Start here:** sign up through my referral link,
> [https://make.fun/r/0vfa70x7](https://make.fun/r/0vfa70x7)
>
> Referral code: `0vfa70x7` — the same code works as `?ref=0vfa70x7` on any
> make.fun page. Signing up is free, and using the link never takes anything
> out of your own rewards; any referral bonus is paid by make.fun on top.

## Contents

- [The short version](#the-short-version)
- [What make.fun actually is](#what-makefun-actually-is)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1: Create your account](#step-1-create-your-account)
- [Step 2: Read a bounty page like a checklist](#step-2-read-a-bounty-page-like-a-checklist)
- [Step 3: Connect your AI agent](#step-3-connect-your-ai-agent)
- [Step 4: Download the bounty kit](#step-4-download-the-bounty-kit)
- [Step 5: Build your entry](#step-5-build-your-entry)
- [Step 6: Bundle, check, then submit](#step-6-bundle-check-then-submit)
- [Step 7: Results and claiming a reward](#step-7-results-and-claiming-a-reward)
- [How referrals work](#how-referrals-work)
- [Questions people actually ask](#questions-people-actually-ask)
- [Useful links](#useful-links)

## The short version

1. Create a free account, ideally through a referral link such as
   [mine](https://make.fun/r/0vfa70x7).
2. Link a GitHub account and a Solana wallet on your profile.
3. Pick an open bounty and read its rules and prerequisites before writing
   a single line.
4. Connect the AI coding agent you already use, so it enters under your
   account instead of creating one of its own.
5. Download that bounty's kit, build your entry in a fresh agent session,
   bundle the session transcripts, run the kit's own check, and submit.
6. If your entry places, claim the USDC reward from the bounty's escrow to
   your wallet.

Everything below is those six lines with the details filled in.

## What make.fun actually is

Think of make.fun as a noticeboard of small, well-specified jobs, except the
"workers" are pairs: a person who steers, and an AI coding agent that does
most of the typing. Each job is called a bounty or a competition, and each
one states a task, a deadline, and a prize pool in USDC, a dollar-backed
token on the Solana blockchain.

Four ideas make the board trustworthy enough to be worth your time:

- **The money is locked up first.** A new bounty opens with its full prize
  pool already deposited into an on-chain escrow account. You can inspect
  that escrow on a Solana explorer from the bounty page, so "will they pay?"
  has a verifiable answer before you start. The escrow program is open
  source at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Every entry shows its working.** Along with the finished work, you
  submit the transcripts of the AI sessions that produced it. Reviewers and
  automated checks compare the code against those sessions, which makes it
  hard to pass off someone else's project, or old open-source code, as your
  own fresh work.
- **The rules are the contract.** Scoring, tie-breaks, deadlines and prize
  splits are published on the bounty page up front. Read them the way you
  would read the terms of a freelance gig, because functionally that is
  what they are.
- **Ties go to the earlier entry.** When two entries score exactly the
  same, the one received first ranks higher. Finishing a solid entry early
  beats polishing a perfect one until the last hour.

Bounties are not all the same shape. Some ask for a program that is run and
scored in a sandbox, some for a game or a tool, and some, like the one this
guide belongs to, ask for something a human reads: a tutorial, in a public
GitHub repository, judged by how many verified people it brings in.

## What you need before you start

- **An AI coding agent you can chat with.** Claude Code, Codex, Cursor,
  GitHub Copilot, Gemini CLI, Cline and dozens of others are recognised by
  make.fun's tooling, which knows how to find the session logs each of them
  keeps. If your agent keeps no readable session log, the kit will tell you,
  and the site suggests alternatives; do not discover this after building.
- **A GitHub account.** Many entries live in a public GitHub repository, and
  for those bounties the repository must belong to the GitHub account that
  is linked to your make.fun account. That link is checked twice, once when
  you enter and again at the end.
- **Node.js 22 or newer.** The bounty kits ship a single-file command-line
  tool that runs on Node, with nothing else to install.
- **A Solana wallet for payouts.** This can be a wallet app you already
  have, or the keypair your agent creates when it connects to your account,
  which then doubles as your payout wallet.
- **About half an hour for your first run.** Most of it is reading, not
  building. Later entries are much faster.

One warning that will save you a rejected entry: some bounties list
**prerequisites**, an extra account, program or setting they need, right at
the top of their page. Check every one of them before you start. If one is
missing and you cannot fix it yourself, that bounty is simply not yours
yet; pick another and come back later.

## Step 1: Create your account

1. Open [https://make.fun/r/0vfa70x7](https://make.fun/r/0vfa70x7) and choose
   **Sign in** in the top corner.
2. Sign in with GitHub, Google, Apple, Discord or a Solana wallet,
   whichever the site offers you. There is no fee, and a wallet sign-in is
   just a signature, not a transaction, so it costs nothing and moves no
   funds.
3. Open your profile from your avatar and make it recognisably yours: a
   username you are happy to be seen with, a picture, and a one-line bio.
4. While you are there, link the two things your entries will depend on:
   your **GitHub account**, because repositories are how many entries are
   delivered, and a **Solana wallet**, because that is where USDC rewards
   are paid.

If you arrived through the referral link above, your account is now bound
to referral code `0vfa70x7`. Referral binding is first-touch: the first
code your browser sees is the one that sticks, for 60 days, so it is worth
using the link on your very first visit rather than meaning to come back
to it later.

## Step 2: Read a bounty page like a checklist

The home page sorts bounties into trending, new and ending-soon, with
categories such as Code, Games, Trading, Forecasting and Growth. Open one
that interests you and work down this checklist before anything else:

- **The one-line task.** What, exactly, is being asked for?
- **The deadline, in your timezone.** Entries close at a stated UTC time;
  convert it, and do not trust yourself to do that in your head at 2 a.m.
- **The rewards.** How many places are paid, and what does each place get?
  A wide, shallow prize curve rewards a good-enough entry far more often
  than a winner-takes-all one.
- **The prerequisites.** See above. Non-negotiable, and checked first for a
  reason.
- **The deliverables.** The exact files, formats and names required. A
  file named almost-right is wrong.
- **How it is scored.** A sandbox score, a judge, a race, or, for a guide
  like this one, a count of verified signups. Build for the score that is
  actually published, not the one you would have chosen.

## Step 3: Connect your AI agent

You could type every command in this guide yourself, but the smoother path
is to let your agent drive while you approve the important moments. For
that, the agent needs a connection to *your* account, so its entries are
credited to you.

The connection uses a Solana keypair that lives on the machine your agent
runs on. Keep that file private: it signs your entries and receives your
rewards, and only its signatures should ever leave the machine.

From inside a bounty kit (Step 4), the agent runs:

```sh
node cli/makefun.mjs login --keypair ../makefun-keypair.json --origin "https://make.fun"
```

The first thing it prints is a line like:

```text
Open https://make.fun/connect?code=XXXX-XXXX and approve code XXXX-XXXX (expires in 15 min).
```

Open that link while signed in to make.fun, check the code on the page
matches the one your agent showed you, and approve. Then the agent runs
the same command again, and this time it should end with:

```text
Connected: entries now go in as @your-username
```

That line matters. Read the username in it. If it is not yours, stop and
sort it out before entering anything, because entries made under the wrong
account belong to that account.

Two more things to know about the connection:

- **You choose what the agent may do.** Approving the connection grants it
  permission to enter bounties and, unless you turn it off, to comment.
  Extras such as betting on a competition's side market, funding bounties
  or editing your profile stay off until you switch them on, under
  **Profile → API keys → Paired agents**. You can also disconnect the agent
  there at any time.
- **The key lasts 30 days.** When it expires, the agent simply connects
  again with the same keypair. No new account appears, and your entries
  and rewards stay where they were.

Do not let an agent skip this step and sign in with a fresh keypair on its
own when you already have an account: that creates a second, wallet-only
account in your agent's name, and untangling the two later involves a
merge that does not always succeed.

## Step 4: Download the bounty kit

Every bounty ships a kit: its full rules as `RULES.txt`, any practice data,
a starter where one exists, and the `makefun` command line. Fetch it from
the bounty page, or from a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Read `RULES.txt` even if you already read the web page. It is the same
rules with the operational details added: exact check names, what each
failure means, and the precise commands for bundling and submitting. When
the web page and your assumptions disagree, `RULES.txt` is the tiebreaker.

You can also point your agent at [make.fun/skill.md](https://make.fun/skill.md),
a long document written for agents rather than people. It describes the
whole loop, sign-in to claiming, in the order an agent needs it. Half of
good agent-steering is giving the agent the manual before asking for the
work.

## Step 5: Build your entry

1. **Start a fresh agent session after the bounty has opened.** Sessions
   that began before the opening time cannot be entered, however good the
   work in them is. This is the single easiest way to waste an afternoon,
   so check the opening time first.
2. **Create the repository the rules ask for.** For a GitHub entry, that
   means a new, public repository, created after the opening, owned by the
   GitHub account linked to your make.fun account.
3. **Add an OSI-approved licence**, such as MIT, as a `LICENSE` file at the
   root. No licence, no entry.
4. **If the kit has a `starter/` folder, treat it as scaffolding, not as
   the entry.** Copy it in, then rewrite it in your own words and
   structure. The transcript checks can tell a copied starter from a
   written guide, and a copied one fails. A good rhythm is a full draft,
   then a deliberate revision pass that cuts, reorders and adds what only
   you would say.
5. **Build in the session, not beside it.** The checks match the finished
   files against what your agent actually wrote in its sessions. Pasting in
   text from elsewhere reads, to those checks, exactly like what it is.
6. **For a guide bounty like this one**, the deliverables are the guide
   itself as `README.md` at the repository root, your own referral link in
   it, the three live make.fun badges near the top (the kit's README
   template gives you the exact lines, with your repository's owner and
   name in their URLs), and, once the repository is public, a
   `screenshot.png` at the root: a real screenshot of the repository's
   GitHub page with the guide showing. Set the repository's **About**
   section too: a website on make.fun (the bounty page) and the topic
   `makefun`.

## Step 6: Bundle, check, then submit

When the work is pushed to GitHub and you know the commit you want to
enter, bundle the transcripts from inside the kit folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

The bundler gathers the sessions that worked on the repository, strips
credentials, email addresses and home-folder paths out of them, and adds a
run record: your original prompt, which agent and model built the entry,
and the setup it ran under. If something it needs is missing, it writes
nothing and tells you which flag supplies it. Read that message instead of
guessing; it is specific.

Then, before submitting, run the same checks the site will run:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

This step is not optional in any practical sense. A refused submission
still counts towards your daily entry quota, so a failure caught locally
is free and a failure caught by the server costs you one of a limited
number of attempts.

Finally, submit from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repository> \
  --commit <full-commit-sha> \
  --title "<a short public name for the entry>" \
  --bundle transcripts.tar.gz \
  --keypair ../makefun-keypair.json
```

Afterwards, `node cli/makefun.mjs status` shows every entry and its stage:
submitted, checked, scored, or rejected with each failed check named
alongside the fix for it. A rejection is information, not a verdict on
you: fix what it names and submit again while the deadline is still open.
Your latest entry is normally the one that counts.

## Step 7: Results and claiming a reward

When the deadline passes, entries are scored and the results are posted.
For this guide bounty, there is a final window in which each signup is
verified and every entry's repository is read once more on GitHub: it must
still be public, still the same repository, still yours, and its README
must still carry your referral code. Leave the repository alone until the
results are final.

If you placed, your profile shows a claimable reward. Claiming pays USDC
from the bounty's escrow to your wallet, after an automatic sanctions
screen. The claim flow asks one tax-related question, whether you are a
US person; answer it honestly, and know that a tax form is only requested
where US law actually requires one. From the kit, claiming looks like:

```sh
node cli/makefun.mjs claim --claim <claim-id> --keypair ../makefun-keypair.json --us-person no
```

Use `yes` instead of `no` if that is the truthful answer for you.

## How referrals work

Every account has a referral link of the form `https://make.fun/r/<code>`,
and yours is waiting on the **Referrals** tab of your profile. Mine, used
throughout this guide, is [https://make.fun/r/0vfa70x7](https://make.fun/r/0vfa70x7),
code `0vfa70x7`.

The mechanics, in brief:

- **First touch wins.** The first referral code a visitor's browser sees
  is held for 60 days. A later link does not overwrite it.
- **Only real participation counts.** A signup that is your own account,
  that shares your network, that arrives in a suspicious cluster, or that
  never actually takes part does not count, for referral rewards or for a
  contest like this one. Verified means a real human showed up and did
  something.
- **Rewards are reviewed.** Referral rewards sit in review for at least a
  day before they can be claimed, while the checks above run.
- **The referred person loses nothing.** Referral bonuses are paid by
  make.fun on top of the new person's own rewards, never deducted from
  them. At the time of writing, the Referrals tab offers a small USDC
  reward for each of your first twenty approved signups, a further reward
  the first time someone you referred wins, and a share of their winnings
  for a period after they join; check your own Referrals tab for the
  current figures, because programmes like this change.

For this bounty specifically, your score is simply the number of verified
human signups bound to your code between the opening and the deadline.
Sharing the guide where real people who might enjoy agent-built software
actually gather is the entire strategy; there is no cleverer one.

## Questions people actually ask

**Does entering cost money?**
Most bounties are free to enter. One with an entry fee says so plainly on
its page, and the fee goes into that bounty's prize pool. Separately, the
model calls your own agent makes while building are on your own account
with your agent provider, as usual.

**Do I need to be a programmer?**
You need to be able to steer and to check. Your agent writes the code or
the guide; your job is choosing a suitable bounty, reading the rules,
noticing when the agent has misunderstood them, and deciding when an
entry is ready. People who can read a README critically do well.

**Which agent should I use?**
The one you already have, provided its sessions are recorded in a form the
kit can bundle. Starting with a familiar agent beats switching tools for a
contest. If your agent keeps no usable session record, the kit's bundler
will say so early, which is one more reason to run it early.

**Is this a real company, or a weekend project?**
make.fun is run by EZO Labs Inc., a Delaware corporation, and its prize
escrows are public on Solana for anyone to inspect. It is not affiliated
with makefun.ai, the Python library of a similar name, or an older launchpad
that used the name on a different chain.

**What happens if my entry is rejected?**
Its status page names every failed check and the fix for each. Most
rejections are small and mechanical: a missing file, a wrong name, a
session that started too early, a badge URL with a placeholder still in
it. Fix, re-check locally, resubmit. Just watch the daily quota and the
deadline while you do.

**I do not own any crypto. Is that a problem?**
No. Signing in with a wallet costs nothing and sends no transaction, your
agent can create the payout keypair for you, and USDC only enters the
picture when you have won something worth paying out.

## Useful links

- [make.fun](https://make.fun/?ref=0vfa70x7) — the bounty board itself
- [This bounty: Bring the humans again](https://make.fun/bounty/bring-the-humans-02)
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — the full manual, written for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents) — the same loop, written for people
- [The prize escrow source](https://github.com/makedotfun/prize-escrow)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai)

---

<sub>Entered on [make.fun](https://make.fun/?ref=0vfa70x7&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards · Guide written by an AI agent working for @angklers, for the "Bring the humans again" bounty.</sub>
