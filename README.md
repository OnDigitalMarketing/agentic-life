# Agentic Life: Run the Loop

A companion site for **Life in the Agentic Age**, a talk by Jake Cook, Harvard Business School.

Everything that learns runs the same loop: **try, expect, compare, adjust.** This site walks students through applying that loop to their own lives, one prompt at a time. They leave with two things they can use the same night: a personal AI coach and a monthly review agent, both built from their own answers.

**Live site:** https://ondigitalmarketing.github.io/agentic-life/

## How students use it

| Path | Time | What they do |
|---|---|---|
| In class | 5 minutes | Write an "I can't → I can" line and a dated 90-day milestone on their phone. |
| Full setup | About 25 minutes | Work through all eight steps, then copy their coach prompt and monthly review prompt. |
| Run a loop | Ongoing | Before each shipment, write down what they expect. Afterward, compare and adjust. Every closed loop adds one to n. |

## The eight steps

1. **Pick your milestone.** Specific, dated, and easy to check.
2. **Know your bugs.** Loss aversion, sunk cost, mimetic desire, fear of embarrassment, and your own.
3. **Log the pain.** A paper failure journal. Your Moleskine never touches the cloud.
4. **Build your coach.** Blend three to five heroes into one honest voice.
5. **Invest in people.** Off the screens, with people who lift you up.
6. **Rest and play.** Protect the time agents give back.
7. **Ship a lot.** More shots mean more hits.
8. **Let it compound.** (1 + r)ⁿ. Protect n.

## What students walk away with

- **A coach prompt.** It's built from their heroes, bugs, milestone, people and guardrails, and it tells the model to be honest rather than flattering, to quote their words back, and to ask one question at a time. Students paste it into a Claude Project or a ChatGPT Project or custom GPT.
- **A monthly review prompt.** It's the review prompt from the talk, personalized with the student's own bugs, rules, milestone and cadence. Students run it as a scheduled task on the first of each month, pointed at a folder of journal pages they choose to share.

## Privacy

Nothing a student types leaves their browser.

- There is no server, no account, no analytics and no database.
- Answers are saved in the browser's `localStorage` on that device only.
- **Transfer link:** the answers are encoded in the URL fragment (the part after `#`). Browsers never send the fragment to the web host, so GitHub never receives it.
- **Backup:** a JSON file the student downloads and can restore later.
- "Erase everything" clears it all.

## Security

- **No third-party code.** The page loads no external scripts, fonts, trackers or libraries, so there is no supply chain to compromise.
- **Locked-down browser policy.** A Content Security Policy blocks every network request (`connect-src 'none'`), external resources, form submissions and `<base>` hijacking. Even if something malicious got onto the page, it could not send a student's answers anywhere.
- **Untrusted input is cleaned.** Everything loaded from a transfer link, a backup file or browser storage is reduced to plain text of a known shape, and everything shown on screen is HTML-escaped.
- **Repo:** only OnDigitalMarketing members with write access can change `main`. Anyone can view, clone or fork, and outside suggestions arrive as pull requests that change nothing until a maintainer merges them. There are no GitHub Actions workflows.

Found a problem? Open an issue or email the maintainer.

## Sources cited in the steps

Brynjolfsson, Li and Raymond, *QJE* (2025); Dell'Acqua and colleagues (2023); Kahneman and Tversky (1979); Arkes and Blumer (1985); Girard, *Deceit, Desire and the Novel* (1961); Gilovich, Medvec and Savitsky, *JPSP* (2000); Fischhoff, *Journal of Experimental Psychology* (1975); Feynman, Caltech commencement (1974) and *Surely You're Joking, Mr. Feynman!* (1985); Wooden and Jamison, *Wooden* (1997); Sharma and colleagues, *Towards Understanding Sycophancy in Language Models* (2023); Waldinger and Schulz, *The Good Life* (2023); Holt-Lunstad, Smith and Layton, *PLOS Medicine* (2010); Sio and Ormerod, *Psychological Bulletin* (2009); Csikszentmihalyi, *Flow* (1990); O'Keefe, Dweck and Walton, *Psychological Science* (2018); Simonton, *Psychological Review* (1997); Samuel Johnson, *The Vision of Theodore* (1748); Theodore Roosevelt, the Sorbonne (1910).

## Running and deploying

It's one static file with no build step and no dependencies.

- **Local:** open `index.html` in a browser.
- **GitHub Pages:** Settings → Pages → Deploy from a branch → `main` / `(root)`.

## License

© Jake Cook. Shared for educational use. Please ask before republishing.
