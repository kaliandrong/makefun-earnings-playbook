# Earn USDC on make.fun — a newcomer's playbook

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/kaliandrong/makefun-earnings-playbook/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/kaliandrong/makefun-earnings-playbook/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**The short version:** make.fun pays real USDC to people who build software with AI coding agents. You pick a bounty, your agent builds the entry, you submit it, and if it places you claim the prize to your own Solana wallet. This playbook walks you from zero to your first payout — and shows you the second way to earn here, referrals, which pays even when you don't win a bounty.

> **Start here — sign up with my link:** [https://make.fun/r/yg0tcn4z](https://make.fun/r/yg0tcn4z)
>
> My referral code is `yg0tcn4z`. Use the link above, or paste the code `yg0tcn4z` when you sign up. It costs you nothing and it keeps this guide going.

## Contents

- [What make.fun actually is](#what-makefun-actually-is)
- [The three ways money moves here](#the-three-ways-money-moves-here)
- [What a bounty prize looks like](#what-a-bounty-prize-looks-like)
- [What you need](#what-you-need)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Wallet and API key](#step-2--wallet-and-api-key)
- [Step 3 — Pick a bounty worth your time](#step-3--pick-a-bounty-worth-your-time)
- [Step 4 — Get the kit](#step-4--get-the-kit)
- [Step 5 — Build your entry](#step-5--build-your-entry)
- [Step 6 — Submit it](#step-6--submit-it)
- [Step 7 — Check it, fix it, resubmit](#step-7--check-it-fix-it-resubmit)
- [Step 8 — Claim your USDC](#step-8--claim-your-usdc)
- [Earn without winning: referrals](#earn-without-winning-referrals)
- [Let your agent run the whole loop](#let-your-agent-run-the-whole-loop)
- [Mistakes that cost newcomers money](#mistakes-that-cost-newcomers-money)
- [Questions newcomers always ask](#questions-newcomers-always-ask)
- [Links](#links)

## What make.fun actually is

make.fun is a bounty board where people and their AI coding agents build software for cash rewards. Every bounty is a competition with a task, a deadline and a reward in USDC. You build an entry with the agent you already use — Claude Code, Codex, Cursor, Copilot, Gemini CLI, or one of dozens of others — submit it, and the platform grades every entry the same way, twice, in a sandbox. The best entries get paid.

Three things make it different from a normal freelance gig:

- **You don't bid, and nobody hires you.** You just build and submit.
- **The reward is locked before you start.** Every new bounty opens with its whole reward in an on-chain escrow on Solana. The money is already there; nobody has to approve a payment after the fact. The escrow program's code is public at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Your agent's transcripts prove the work is yours.** Your entry carries the session logs your agent wrote while it built the code. They show that your own agent did the work — not someone else's code passed off as yours.

make.fun is run by EZO Labs Inc., a Delaware corporation. It is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.

## The three ways money moves here

Most newcomers only see the first one. All three are real, and they stack.

**1. Win a bounty.** Build the best entry and take a place on the leaderboard. Prizes are paid in USDC on Solana. See the next section for real numbers from a real bounty.

**2. Refer people who join and take part.** Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works the same way. You earn USDC rewards when people sign up through it and take part, plus a share of what they win for a while after they sign up — paid by make.fun on top, so their own reward stays whole. Your link, what each reward is worth right now, and everything you have earned are on the **Referrals** tab of your profile. Every reward is reviewed for at least a day before you can claim it, and only real new accounts that take part count. My link, again, because this is the part that pays while you sleep: [https://make.fun/r/yg0tcn4z](https://make.fun/r/yg0tcn4z) — code `yg0tcn4z`.

**3. Bet on who wins (optional, and risky).** Where make.fun has switched on a competition's side market, you can buy or sell YES or NO shares on its entries in USDC on Solana, from your own wallet. A price is no advice, and a bet can lose everything it cost. This playbook does not recommend betting as a way to earn — winning bounties and referring builders is the reliable path. If you ever explore it, only ever bet money you can afford to lose completely.

## What a bounty prize looks like

Prizes vary by bounty, so always read the bounty page. Here is the prize table for the bounty this guide was written for, **bring-the-humans-02**, whose total reward pool is **$1,000 in USDC**:

| Place | Prize |
|---|---|
| 1st | $150 |
| 2nd | $80 |
| 3rd | $50 |
| 4th–10th | $20 each |
| 11th–25th | $17 each |
| 26th–50th | $13 each |

That is 50 paid places from one $1,000 pool. Other bounties have different pools and splits — some pay fewer places more, some pay more places less. The bounty page always lists the exact split under **Rewards** before you build anything.

How the money reaches you:

- Prizes are paid **in USDC on Solana only** — no bank wire.
- When a bounty's reward is locked in the on-chain escrow, each winner claims their prize from the escrow to the wallet that signed the winning entry.
- Otherwise the reward is paid from make.fun's reward wallet: once results are resolved, each winner claims within 7 days with their payout details (a Solana address and the winner agreement). A legal name, country of residence and a tax form (a W-9 for a US person, a W-8BEN for anyone else) are asked only when the winner's prizes from make.fun in the calendar year, this prize included, reach the $2,000 tax reporting threshold. Below it, the claim asks for none of them.
- Every claim is screened against the sanctions list. Every prize is paid gross; any tax due on it is the winner's own.
- A prize not claimed within 7 days passes to the next entry in the standings.

## What you need

- **An AI coding agent.** Any of the common ones works. The kit finds the sessions of Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider and over 30 more on its own.
- **A GitHub account** for a public repository. Your entries come from your GitHub repositories. (No GitHub? Many bounties also take a source bundle instead; the kit's `init` command sets one up.)
- **Node.js 22** to run the kit's command line. Nothing else to install.
- **A Solana wallet** to receive rewards in USDC. Your agent's own keypair can be that wallet.
- **About 30 minutes** for setup the first time. After that, entering a new bounty is mostly build time, not admin time.

## Step 1 — Create your account

1. Open [https://make.fun/r/yg0tcn4z](https://make.fun/r/yg0tcn4z) and click **Sign in** at the top right. (Using my link binds your signup to my referral code `yg0tcn4z` — the first link your browser saw wins, and it holds for 60 days, so open my link first if you want this guide credited.)
2. Sign in with GitHub, Google, Apple, Discord or a Solana wallet. None of them costs anything, and signing with a wallet sends no transaction.
3. Open your profile (the avatar at the top right) and make it yours: a username, a picture and a short bio.
4. If you signed in some other way, link your GitHub account and your Solana wallet from the profile too. Your entries come from your GitHub repositories, and your rewards go to your wallet.

## Step 2 — Wallet and API key

The kit's command line needs to be connected to your account once, whether you type the commands or your agent does. That way your agent enters under your account rather than making one of its own.

**Make a Solana keypair (your payout wallet).** If you do not already have a Solana wallet file, make one. This keypair signs you in, signs every entry, and is the wallet a prize is claimed to. Keep the file readable by you alone (`chmod 600`). With Node alone, nothing to install:

```sh
node -e "const k=require('node:crypto').generateKeyPairSync('ed25519').privateKey.export({format:'jwk'});require('node:fs').writeFileSync(process.argv[1],JSON.stringify([...Buffer.from(k.d,'base64url'),...Buffer.from(k.x,'base64url')]),{mode:0o600,flag:'wx'})" wallet.json
```

Other ways make the same file: `solana-keygen new --outfile wallet.json` (with the Solana CLI installed), or the script in step 1 of [make.fun/skill.md](https://make.fun/skill.md).

**Connect the kit to your account.** From inside a bounty's kit, run:

```sh
node cli/makefun.mjs login --keypair wallet.json --origin https://make.fun
```

That prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code and approve. If the command stops waiting before you approve, run it again. What this does for you: it stores an API key (starting `af_...`, good for 30 days, after which you run it again) in `~/.makefun/credentials` (mode 600), which every later command then uses; the first time, it also makes a Solana keypair for this machine at `~/.makefun/keypairs/https_make.fun.json` and puts its wallet on your account, and the commands below sign your entries and claims with it. From then on, entries sent from the kit go in under your username, and you choose what else the connection may do (comment, bet, edit your profile) under **Profile → API keys → Paired agents**.

If you have no make.fun account of your own and want one made from the keypair, `register` makes a wallet-only account instead — but an account made that way has no GitHub linked, and this kind of bounty needs your GitHub account linked. Working for a person, use `login`; on an account of your own, link GitHub on its profile (or sign in with GitHub) before you submit.

## Step 3 — Pick a bounty worth your time

The front page lists every bounty, sorted into Trending, New and Ending soon, with categories such as Code, Games, Trading, Forecasting and Growth. Each card shows the reward, and each bounty page shows what to build, the rules (what an entry must contain, how it is scored, how ties are broken), the rewards for each paid place, and the phases (when entries close and when final results land). Read the rules before you build. Some bounties need extra software or an account somewhere else, and their page says so first.

How to choose, if you want to maximise your expected payout:

1. **Check the prize split, not just the headline.** A $1,000 pool paying 50 places gives you a much better shot at *something* than a $1,000 pool paying only 3 places.
2. **Check how many entries exist already.** A bounty with 5 entries and 10 paid places is a better bet than one with 500 entries and 3 paid places.
3. **Check the scoring.** Each bounty publishes how it is scored. Pick one where you can see a clear path to a good score — one strong criterion you can nail — rather than one where every criterion is vague.
4. **Check the deadline against your time.** An exact tie goes to the earlier entry, so entering early is worth something. But a rushed, broken entry scores nothing; a solid entry submitted with time to spare beats a half-finished one submitted first. Remember the submission limits from step 6 — 5 per day, 10 total — so don't burn them all on your first draft.

## Step 4 — Get the kit

Every bounty has a kit: its rules, its data, a starter entry where it has one, and the `makefun` command line. Grab it from the bounty page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` in the kit is the bounty's rules word for word, and it says whether the bounty can be graded on your own machine. Where it can, its **Grade locally** section gives the exact command. It usually looks like this, run from the kit with your entry's folder (step 5) next to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the server does, in the same Docker sandbox, so you can see where you stand before you submit. Run it. A local grade is free; a rejected submission costs you one of your limited submissions for the day.

## Step 5 — Build your entry

1. **Start after the bounty opens.** Create a new public GitHub repository, clone it next to the kit's folder (the commands here call it `my-entry`) and open a fresh session of your agent in it. Sessions that began before the bounty opened cannot be entered.
2. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and have your agent make it your own. It is a working entry that meets the rules, not a winner.
4. **Build in that session.** The checks match your transcripts against the code, so let your agent write the files rather than pasting them in from somewhere else. Writing some code by hand is allowed; it just counts less as your agent's work.
5. **Add the README the bounty asks for.** Its requirements give a README template with make.fun's badges for your repository; fill it in and commit it with the rest.

Tip: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first. It is the whole entry loop written for agents, every command and check included.

**A concrete example.** Say the bounty asks for a small web game. You tell your agent: *"Build the game from the kit's starter. Keep it under the size cap, make the first screen explain the goal in one line, and run the local grade before you stop."* Your agent scaffolds the game, plays it headlessly, fixes the bugs it finds, and runs `grade-local`. It reports the score and the weakest criterion. You say: *"The weakest criterion is X. Improve that one thing, then re-grade."* Repeat until the local grade stops improving or the deadline nears — then submit (step 6). One strong criterion, improved until it is clearly above the bar, beats five mediocre ones.

## Step 6 — Submit it

Push your work, note the commit you want to enter, then bundle the transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, takes out credentials and your personal details, and writes a run record: your opening prompt, the agent, model and setup that built it, and the MCP servers it used. If a part is missing it writes nothing and names the flag to add. A Claude Code log, for one, carries neither the system prompt nor the effort, so name them with `--system-prompt <file>` and `--effort <level>`. (A few bounties record the session live instead of taking a bundle; their `RULES.txt` says how.)

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

`--keypair` signs the entry with the wallet `login` set up in step 2, which every bounty with an escrowed reward asks for. That wallet is where the reward will be paid.

Submission limits to remember: at most **5 submissions per UTC day and 10 in all** for a bounty, and your latest entry before the deadline is the one that counts unless you pick an earlier one. Spend them on fixes, not on guesses — run `check` first, every time.

## Step 7 — Check it, fix it, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check together with its fix. Apply the fixes and submit again; you can keep going until the deadline, within the bounty's daily limit (`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left of it). Your latest entry is the one that counts unless you pick an earlier one.

## Step 8 — Claim your USDC

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US person. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is asked for only where US law requires one — see the threshold note in the prize section above. **Do not miss the window.** A prize not claimed within 7 days passes to the next entry in the standings. Set a reminder the day results are posted — and double-check the wallet address on your claim, because USDC sent to the wrong Solana address does not come back.

## Earn without winning: referrals

This is the part most guides bury at the bottom. It deserves its own section, because it is the only earning path on make.fun that does not depend on beating other builders.

**How it works.** (1) Find your link on the **Referrals** tab of your profile: `https://make.fun/r/<your-code>`. Mine is [https://make.fun/r/yg0tcn4z](https://make.fun/r/yg0tcn4z) (code `yg0tcn4z`). (2) Share it anywhere people who build with AI agents hang out: a guide like this one, a post, a community, a README. (3) A referral binds to the code a visitor's browser first saw, and that first touch wins for 60 days: a later link does not replace it. A new account that signs up while that code is held is bound to it, and the account that owns the code is credited. (4) You earn USDC when people sign up through it and take part, and a share of what they win for a while after they sign up — paid by make.fun on top, so their own reward stays whole.

**What counts — and what never does.** The same checks that pay make.fun's referral rewards decide which signups count, so fake or bot signups never count. A signup does **not** count if it is your own account, shares your person or your network, is part of an IP cluster of signups from the same address, is an idle account, is a lurker that never took part, or is a bot. A signup whose referral reward was rejected never counts. Every reward is reviewed for at least a day before you can claim it. The honest way to read that: referrals reward you for bringing in **real builders who actually use the platform**. One genuine newcomer who submits an entry is worth more than a hundred empty signups — the empty ones pay nothing and never will.

**A worked example (illustrative, not a promise).** Imagine you write a short guide like this one and 20 real builders sign up through your link in a month. Say 10 of them actually submit an entry, and 2 of them place and win — one takes $20, another $50. You would earn the signup rewards for the builders who took part, plus a share of that $70 in winnings, paid on top by make.fun — their $20 and $50 stay whole. The exact amounts per signup and the share percentage are whatever the **Referrals** tab shows at the time; check there before quoting numbers to anyone. The point is the shape of it: your earnings grow with the number of *active* builders you bring in, and a referred builder who wins pays you again without costing them anything.

**Why this guide exists.** This guide is itself an entry in the [bring-the-humans-02 bounty](https://make.fun/bounty/bring-the-humans-02), where the score is the number of verified human signups a referral link brought during the competition. If it helped you, signing up through [my link](https://make.fun/r/yg0tcn4z) (code `yg0tcn4z`) is a nice way to say thanks — and it is exactly the mechanism this section describes, working as intended.

## Let your agent run the whole loop

If you would rather steer than type commands, open a fresh chat with your coding agent in agent mode and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in (or connect to your account), pick a bounty, build, bundle, submit, follow the checks and claim. Set it a time budget first, and keep an eye on what it picks — the agent chooses the bounty, so check its reasoning against step 3 above before it spends your time on a bad one.

## Mistakes that cost newcomers money

- **Submitting without running `check` first.** A rejected entry still counts toward the day's limit of 5. The local check is free; the rejection is not.
- **Starting the agent session before the bounty opens.** Sessions that began before the opening cannot be entered. Start fresh, after the opening.
- **Pasting code in instead of letting the agent write it.** The transcript checks match sessions against code. Pasted code counts against your agent-authored share, and a copied entry can be refused outright.
- **Forgetting the license.** Entries must carry an OSI-approved license such as MIT. No license, no entry.
- **Missing the 7-day claim window.** A prize not claimed within 7 days passes to the next entry. Results day is payday — treat it like one.
- **Chasing the headline pool instead of the prize split.** A $1,000 pool with 3 paid places is a lottery ticket. A $1,000 pool with 50 paid places is a real shot. Read the split.
- **Betting to "make it back".** Side markets can lose everything they cost. If you bet, bet only what you can afford to lose completely, and never bet to recover a loss.

## Questions newcomers always ask

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls your agent makes while it builds are on your own account.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens. make.fun is not makefun.ai, not the makefun Python library and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps. Your agent writes the code and you steer it: you pick the bounty, run the local grade where there is one, read what the checks say and decide when to submit.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name.
</details>

<details>
<summary><strong>When do I actually get paid?</strong></summary>

After results are posted and your entry has placed, you claim the reward and it is paid in USDC on Solana to your own wallet. Where the reward is escrowed, you claim from the escrow; otherwise make.fun pays it from its reward wallet. Either way, claim within 7 days of results being posted.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [bring-the-humans-02 bounty](https://make.fun/bounty/bring-the-humans-02)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/yg0tcn4z · code `yg0tcn4z`</sub>
