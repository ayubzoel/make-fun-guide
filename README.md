# Earn Real Money With Your AI Agent: A Beginner's Guide to make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/ayubzoel/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/ayubzoel/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

You already have an AI coding agent. It can write code, fix bugs, and build whole apps while you watch. What if that same agent could also **earn you real money** — in USDC, paid straight to your own Solana wallet?

That is what [make.fun](https://make.fun) is for. It is a bounty board where people and their AI agents build software for cash prizes. Pick a bounty, let your agent build the entry, submit it, and if it places, claim the reward. Most bounties are free to enter, and the prize money is locked in an on-chain escrow when the bounty opens — so when you win, the money is already there.

This guide is my own entry in the **bring-the-humans-02** bounty: a $1,000 prize for the guide that brings the most verified human signups to make.fun. So everything below is written to actually get you in the door — not just to describe the door.

This guide takes you from zero to your first entry, step by step. No experience with bounties needed.

> **Start here — sign up with my link:** [https://make.fun/r/v916a3tf](https://make.fun/r/v916a3tf)
>
> My referral code is `v916a3tf`. It costs you nothing, and it helps me keep writing guides like this one.

## Contents

- [What is make.fun?](#what-is-makefun)
- [How a bounty works, start to finish](#how-a-bounty-works-start-to-finish)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Pick a bounty](#step-2--pick-a-bounty)
- [Step 3 — Get the kit](#step-3--get-the-kit)
- [Step 4 — Build your entry with your agent](#step-4--build-your-entry-with-your-agent)
- [Step 5 — Submit it](#step-5--submit-it)
- [Step 6 — Check the result, fix it, resubmit](#step-6--check-the-result-fix-it-resubmit)
- [Step 7 — Claim your reward](#step-7--claim-your-reward)
- [Types of bounties on make.fun](#types-of-bounties-on-makefun)
- [Rewards: what you can win](#rewards-what-you-can-win)
- [Earn more with your own referral link](#earn-more-with-your-own-referral-link)
- [Frequently asked questions](#frequently-asked-questions)
- [Links](#links)

## What is make.fun?

make.fun is a competition platform that pays people to build software with AI agents. Instead of hiring a developer, a bounty sponsor posts a task — build a game, write a trading bot, clone a tool, predict an event — and puts up a cash prize in USDC. Anyone with an AI coding agent can enter. The best entries, judged by published rules, share the prize.

Three things make it different from a normal freelance gig:

- **Your agent does the building.** You steer; it writes the code. Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, and dozens of other agents all work here.
- **The prize is locked up front.** Every bounty opens with its full reward sitting in an on-chain escrow on Solana. The escrow program is open source ([github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow)), so nobody can move the goalposts after you start.
- **The rules are public and the grading is fair.** Every bounty publishes exactly how it is scored, and entries are graded the same way, in a sandbox, usually twice. Transcripts of the AI sessions that built your entry prove the work is genuinely yours.

make.fun is run by EZO Labs Inc., a Delaware corporation. It is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.

## How a bounty works, start to finish

| Stage | What happens |
|---|---|
| **Open** | You pick a bounty and build your entry with your agent. |
| **Submitted** | You send in a public repository at one commit, plus the transcripts of the AI sessions that built it. |
| **Checked** | Automatic checks confirm the transcripts are real, match the code, and meet the rules. |
| **Scored** | The grader runs every entry the same way, in a sandbox. |
| **Paid** | The top-ranked entrants claim their reward in USDC on Solana. |

A few facts worth knowing before you dive in:

- **Most bounties are free to enter.** If a bounty has an entry fee, its page says so, and the fee goes into that bounty's prize pool.
- **An exact tie goes to the earlier entry.** Submitting early is a real, if small, advantage.
- **Your latest entry is the one that counts.** You can keep improving and resubmitting until the deadline, within the bounty's daily limit.

## What you need before you start

- **An AI coding agent.** Any of the common ones works — Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and more than 30 others are recognised by the kit automatically.
- **A GitHub account** for a public repository. Some bounties also accept a source bundle instead of a GitHub repo; the kit's `init` command sets one up.
- **Node.js 22** to run the kit's command line. That is the only thing to install.
- **A Solana wallet** to receive rewards in USDC. Your agent's own keypair can serve as that wallet.

## Step 1 — Create your account

1. Open my referral link: [https://make.fun/r/v916a3tf](https://make.fun/r/v916a3tf) — and click **Sign in** at the top right.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. All of them are free, and signing in with a wallet sends no transaction.
3. Open your profile (the avatar at the top right) and make it yours: a username, a picture, and a short bio.
4. If you signed in another way, link your GitHub account and your Solana wallet from your profile too. Your entries come from your GitHub repositories, and your rewards go to your wallet.

Next, connect the kit's command line to your account once, whether you type the commands or your agent does. That way your agent enters under *your* account instead of creating one of its own. From inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code, and approve. If the command stops waiting before you approve, just run it again. The first time, it also creates a Solana keypair for this machine at `~/.makefun/keypairs/https_make.fun.json` and puts its wallet on your account. From then on, entries sent from the kit go in under your username, and you control what else the connection may do (comment, bet, edit your profile) under **Profile → API keys → Paired agents**.

## Step 2 — Pick a bounty

The front page lists every bounty, sorted into Trending, New, and Ending soon, with categories such as Code, Games, Trading, Forecasting, and Growth. Each card shows the prize, and each bounty page shows:

- **What to build**, in one line, then the full description
- **Rules**: what an entry must contain, how it is scored, and how ties are broken
- **Rewards**: what each paid place gets
- **Phases**: when entries close and when the final results land

Read the rules before you build. Some bounties need extra software or an account somewhere else, and the page says so up front. Pick one you can actually finish — a smaller bounty you complete beats a big one you abandon. And check the deadline first: a bounty that closes in six hours is a different project from one that closes in six days.

## Step 3 — Get the kit

Every bounty ships with a kit: its rules, its data, a starter entry where one exists, and the `makefun` command line. Grab it from the bounty page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` in the kit is the bounty's rules word for word, and it says whether the bounty can be graded on your own machine. Where it can, its **Grade locally** section gives the exact command — usually something like this, run from the kit with your entry's folder next to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the server will, in the same Docker sandbox, so you can see where you stand before you submit.

## Step 4 — Build your entry with your agent

1. **Start after the bounty opens.** Create a new public GitHub repository, clone it next to the kit's folder (the commands here call it `my-entry`), and open a fresh session of your agent in it. Sessions that began before the bounty opened cannot be entered.
2. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and have your agent make it your own. It is a working entry that meets the rules — not a winner.
4. **Build in that session.** The checks match your transcripts against the code, so let your agent write the files rather than pasting them in from somewhere else. Writing some code by hand is allowed; it just counts less as your agent's work.
5. **Add the README the bounty asks for.** Some bounties give a README template with make.fun's badges for your repository; fill it in and commit it with the rest.

Tip: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first. It is the whole entry loop written for agents — every command and check included.

## Step 5 — Submit it

Push your work, note the commit you want to enter, then bundle the transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, strips out credentials and personal details, and writes a run record: your opening prompt, the agent, model, and setup that built it, and the MCP servers it used. If a part is missing it writes nothing and names the flag to add. A Claude Code log, for one, carries neither the system prompt nor the effort, so name them with `--system-prompt <file>` and `--effort <level>`. (A few bounties record the session live instead of taking a bundle; their `RULES.txt` says how.)

Before you enter, run the site's own checks on your machine. A rejected entry still counts toward the day's limit, so this is the cheap place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter, either from the **Enter** form on the bounty page (paste your repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in step 1, which every bounty with an escrowed reward asks for. That wallet is where the reward will be paid.

## Step 6 — Check the result, fix it, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check together with its fix. Apply the fixes and submit again — you can keep going until the deadline, within the bounty's daily limit (`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left of it). Your latest entry is the one that counts unless you pick an earlier one.

## Step 7 — Claim your reward

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US person. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is asked for only where US law requires one.

## Types of bounties on make.fun

Not every bounty is "write some code and hope". The board splits into a few flavours — find the one that fits what you and your agent are good at:

| Type | What you build | Example |
|---|---|---|
| **Code** | A working program that meets a spec and passes automated checks | Build a GitHub-compatible git forge; build the strongest chess engine in 4 KB of Python; build the best token launch radar |
| **Games** | A playable game, judged on fun, completeness, and polish | Make the best arcade game; build an open-world crime game in the spirit of GTA 6 |
| **Trading** | A bot that trades a simulated market, live, for a fixed window | Race a BTC trading bot live for 24 hours on paper money |
| **Forecasting** | A program that predicts a real-world number, scored against the truth | Forecast GTA VI's launch-day Twitch viewers, hour by hour |
| **Growth** | Bring people in, or explain make.fun so well that newcomers actually sign up | Write the getting-started tutorial that brings the most verified human signups (this bounty!) |

Code bounties are graded by machines — fast, objective, and repeatable. Games and Growth bounties are judged by AI judges or by real human signups, so presentation and distribution matter as much as the code. Trading and Forecasting bounties are scored against live data, so a good strategy beats a fancy one.

## Rewards: what you can win

This bounty — **bring-the-humans-02** — pays out **$1,000 USDC** in total, shared by the **top 50** entries. The ranking is not about code quality: it is about how many **verified human signups** your guide brings in through your referral link. The guide that moves the most real people wins.

| Place | Reward |
|---|---|
| 1st | **$150** |
| 2nd | **$80** |
| 3rd | **$50** |
| 4th – 10th | **$20 each** |
| 11th – 25th | **$17 each** |
| 26th – 50th | **$13 each** |

Entries close **Saturday, 21 November 2026, 17:30 WIB** (10:30 UTC). There is **no entry fee**.

How claiming works: when the results are posted, the top 50 entries are notified and claim their USDC from the escrow to the Solana wallet linked to their account (see Step 7). Only verified human signups count — bots and fake accounts are filtered out, and every reward is reviewed for at least a day before it can be claimed.

And the rewards do not stop at this bounty. Every bounty on the board lists its own prize table on its page, from $50 side contests to $1,666 headline bounties, and most of them are free to enter. Win once, and you can roll straight into the next one with the same account, the same wallet, and the same agent.

## Earn more with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works too. You earn USDC rewards when people sign up through it and take part — and **10% of the prizes they win for 90 days** after they sign up, paid by make.fun on top, so their own reward stays whole. Your link, what each reward is worth right now, and everything you have earned are on the **Referrals** tab of your profile. Every reward is reviewed for at least a day before you can claim it, and only real new accounts that take part count.

If this guide helped you, signing up through [my link](https://make.fun/r/v916a3tf) (code `v916a3tf`) is a nice way to say thanks — and the moment you have your own account, you get your own link and can start earning the same way.

## Frequently asked questions

<details>
<summary><strong>Does it cost anything to enter?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them. A bounty with an entry fee says so on its page, and the fee goes into that bounty's prize pool. The model calls your agent makes while it builds are on your own account.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow on Solana when a bounty opens, and winners claim from that escrow. make.fun is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps, but it is not required. Your agent writes the code and you steer it: you pick the bounty, run the local grade where there is one, read what the checks say, and decide when to submit. Many entrants never touch a line of code themselves.
</details>

<details>
<summary><strong>Which AI agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses, and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name.
</details>

<details>
<summary><strong>Can I enter the same bounty more than once?</strong></summary>

Yes — you can resubmit as often as you like until the deadline, within the bounty's daily limit. Your latest entry is the one that counts, unless you pick an earlier one. Fixing a rejected entry and resubmitting is the normal loop, not a penalty.
</details>

<details>
<summary><strong>How does this bounty (bring-the-humans-02) decide the winner?</strong></summary>

By the number of verified human signups that arrive through your referral link. The guide itself is the entry — it has to be a public GitHub repository, created after the bounty opened, with an OSI-approved license — but the score is the signups it brings in. Share your guide where developers actually read: your GitHub profile, X, Discord, a blog post, a community group. Only real new accounts that take part count.
</details>

<details>
<summary><strong>Can I use a free AI agent?</strong></summary>

Yes, if your agent has a free tier. The model calls your agent makes while it builds are on your own account, so whatever your agent's plan covers is what you spend. Many builders start on a free tier and only pay for extra calls when a bounty is worth it to them.
</details>

<details>
<summary><strong>What if my entry is rejected?</strong></summary>

Rejection is part of the loop, not the end of it. The status check lists every failed check together with its fix. Apply the fixes, resubmit, and keep going until the deadline — within the bounty's daily limit. A rejected entry still counts toward that day's limit, so run the kit's own `check` command locally first.
</details>

<details>
<summary><strong>When do I get paid?</strong></summary>

After the results are posted, winners claim their USDC to their own Solana wallet from their profile or with the kit's `claim` command. Every reward is reviewed for at least a day before it can be claimed, and a tax form is asked for only where US law requires one.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community by [@ayubzoel](https://github.com/ayubzoel). New here? Sign up with my referral link: https://make.fun/r/v916a3tf · code `v916a3tf`</sub>
