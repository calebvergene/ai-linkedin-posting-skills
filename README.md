# ai-linkedin-posting-skills

Claude skills for writing LinkedIn posts, one per post format. Each skill outputs plain text ready to paste into LinkedIn. Two image skills turn your numbers into a PNG for the post.

## Post skills

🔥 marks the formats that performed best.

| Skill | Structure |
|---|---|
| `linkedin-lead-magnet` | Bold hook, problem, bullet preview of the resource, social proof, `Comment 'WORD'` CTA, repost bonus ([example 1](https://lnkd.in/p/g5vQxqjA), [example 2](https://lnkd.in/p/gqS24U6e)) |
| `linkedin-case-study` | "X days ago / Today" contrast, `→` results, how it was done, the takeaway, soft CTA |
| 🔥 `linkedin-educational` | Clear promise, 5–7 numbered points (insight + how to apply), CTA ([example 1](https://lnkd.in/p/g9Zcmp-G), [example 2](https://lnkd.in/p/gsrzkUPS)) |
| `linkedin-viral-lead-magnet` | Big breakdown teaser, what's inside, recognizable names, triple CTA, bonus |
| 🔥 `linkedin-give-resource` | Credibility hook with big names, the whole roadmap in 2–3 bold-header sections, objection, recap line, "drop your email" for the full guide ([example 1](https://lnkd.in/p/gdXKF4s5), [example 2](https://lnkd.in/p/gV7FWtbd), [example 3](https://lnkd.in/p/gsTS-37D), [example 4](https://lnkd.in/p/gGWWCYx6)) |
| `linkedin-hot-take` | One strong claim, the reasoning as a chain in 1–2 bold-header sections, specifics, comment-keyword CTA for a guide or waitlist (or a question) ([example 1](https://lnkd.in/p/gA-SZd8w), [example 2](https://lnkd.in/p/ggp4mRx6), [example 3](https://lnkd.in/p/gS4RNXr8)) |
| `linkedin-announcement` | News and company tag in line 1, what you'll work on, thank-you that tags the people who helped ([example 1](https://lnkd.in/p/gD_iQRcZ), [example 2](https://lnkd.in/p/gu3viKhk)) |

### Why the formats work

- **Lead magnet:** Generic skill for lead generation and engagement. The hook keeps the reader reading until the end. Engagement comes from the CTA at the end (comment for the resource, argue if you disagree).
- **Educational:** The hook builds the poster's credibility, then numbered points tell a story and give advice. The format gets many saves because it holds useful information.
- **Give resource:** The hook promises results from using a resource. The post breaks the resource into steps, then offers the full version with a CTA that asks for comments. The post image must show the value at a glance.
- **Hot take:** The hook is a controversial claim that pulls readers through the whole post. The take also teaches the reader something.

### Inputs

| Input | Details |
|---|---|
| Topic | Required. What the post is about. |
| Intended audience | Required. Who the post is for. The skill asks for it if it is missing. |
| Context | Optional. A blurb with extra detail. The content of the post comes from here. |
| Tone | Optional. How you sound: a short description, a sample post, or a list of writing rules. The skill keeps the layout and adjusts the wording of each sentence to match. |
| All lowercase / relaxed tone | Optional. Ask for an all-lowercase, relaxed version of the post. |

## Image skills

| Skill | What it makes |
|---|---|
| `image-sankey` | Sankey diagram PNG from stage counts (applied, rejected, interviews, offers). Claude writes the [SankeyMATIC](https://github.com/nowthis/sankeymatic) input, adds fixed settings, and renders it with the real SankeyMATIC code in headless Chrome. The watermark is hidden. |
| `image-growth-chart` | Chart PNG for a metric that grew, drawn like LinkedIn's creator analytics card: the daily line, the total on top, dates ending today. Only your numbers are real; the days between them are generated. |

Output: a PNG, 2400×2000.

Example input for `image-sankey` ([the post that used this image](https://lnkd.in/p/gsrzkUPS)):

```
applied 1040
640 ghosted
378 rejected
22 OAs
14 first round
8 second round (4 of these offers)
3 third round (1 of these offers)
```

Example input for `image-growth-chart`:

```
visitors on my website:
10 per day two weeks ago,
400 per day today
```

Inputs: the numbers, in any format. For `image-sankey`, say which outcomes came out of which stage, for example "8 second round (4 of these offers)". For `image-growth-chart`, give the metric, the start and end values, and the time range.

## Post format tips

These tips are built into the skills. Use them for any LinkedIn post.

**Post length**
- 1,200 to 1,800 characters is the sweet spot.
- Posts under 200 characters get 3x less engagement.
- Returns shrink after 2,500 characters.

**Scannability**
- Long posts win when they are formatted.
- More line breaks get 4.6x more engagement.
- Use short paragraphs, white space and single lines.

**The hook**
- Keep the first line under 60 characters.
- Short hooks get 2.2x more engagement than long ones.
- Hook test: it fits in 2 lines.

**Questions**
- Posts with 4+ questions nearly triple comment density.
- Ending with a question adds 26% to engagement.
- Ask specific questions. "Do you agree?" is too vague.

**Links**
- One link in the post drops engagement by 38%.
- A single link drops comment density by 59%.
- Put the link in the comments.

## General LinkedIn guide

Rules for growing a LinkedIn account and capturing leads.

### The mobile-first reality 📱

If your post does not look good on a phone, it does not exist.

- **72%** of users are on mobile. **28%** use a desktop.
- Users view about 12 posts per session on mobile. You have a split second to stop them.
- Write short paragraphs and make the hook impossible to ignore.

### The viral scoreboard 💯

The algorithm gives every action a weight. This is why the "comment to get the resource" strategy works.

| Action | Weight | Why it matters |
|---|---|---|
| Comment | 12 pts | 👑 The king. This is why posts ask for comments. |
| Save | 10 pts | High signal that your content is valuable. |
| Instant repost | 8 pts | Great for reach. |
| Repost with thoughts | 4 pts | Good, but less viral than an instant share. |
| "See more" click | 2 pts | Proves the hook worked. |
| Like | 1 pt | The weakest metric. Chase conversation, not likes. |

When you offer real value in exchange for a concrete action like a comment, LinkedIn rewards you with reach. The classic tactic:

> "Comment 'WEB' and I'll send you the free resource."

It combines high engagement (comments) with lead capture (DMs and connections) in one move.

**Pro tip:** Repost your own post 6 to 8 hours after publishing. This often boosts visibility by about 30%.

### 📆 Posting rhythm and consistency

- Post 2 times per week, every week.
- Monday to Thursday outperform weekends by up to 19%.

A steady rhythm keeps your profile active in the feed, gives the algorithm enough signals, and trains your audience to expect value from you. Think in campaigns, not one-shot posts: 2 good posts per week for several weeks beat one "perfect" post once in a while.

### 💬 The comment keyword

The word people comment to get the resource must be short so it does not limit action.

- Use 1–3 letters or one simple word: `WEB`, `LIST`, `PDF`, `AI`, `DOC`.
- You can also ask people to comment their email. That gives you a way to send the resource.
- Use a short instruction. Long phrases lower the number of comments.
- The easier it is to type, the more people comment.
- Answer comments as fast as you can.

The goal is to remove every point of friction between "interested" and "takes action."

### 💰 The conversion funnel

Your post is the hook. Your profile is the landing page.

Typical user journey:

1. Scrolls the feed
2. Sees your post (hook + value)
3. Comments
4. Clicks the link or sends a DM

Optimize your profile as a key step in this journey:

- **Clear value proposition:** Who do you help?
- **Reassurance:** Why should they trust you?
- **Call to action:** A clear link to your offer or your portfolio.

### 🍰 The optimal content mix

The most visible creators add value, not only sell. Aim for this mix:

- **55% Expertise:** how-to guides and industry insights. Show your tool or skill here.
- **30% News and offers:** celebrate wins and share specific deals.
- **15% Personal branding:** your story and personality.

### 🏗 Four elements of a viral post

A great post is useful, visual, timely and solves a problem. The algorithm rewards all four.

#### 1. A free but high-value lead magnet 🎁

The offer must feel like something people would normally pay for. It triggers the "I actually need this" reaction.

- Real value: a template, a ready-to-use landing page, an optimized prompt, a mini-course.
- Something that motivates the comment (your CTA).

Examples:

- "Landing page template to sell your service."
- "AI-generated portfolio page ready to use."
- "The exact prompt to generate a pro website in 10 seconds."

#### 2. Visually impactful 👁

The visual stops the scroll. If readers do not stop, they do not read. Make people ask "What is that?"

Add an image to every post:

- It makes the post more attractive.
- It takes more vertical space on the screen, so the post is hard to miss.
- It must show what people get if they comment: the list, template, workflow or resource. You can blur or mask parts to create curiosity while the value stays obvious. The reader should think "If I comment, I get this."

Best formats:

- Screenshot of the result created with your tool.
- Before / after comparison.
- Mini-video of the generation process (sped up).
- Carousel explaining 3 key points.

A strong pattern: the final output (what they get) at the top of the image, and a workflow or system at the bottom that shows a real process behind it. This tells people there is a real resource to collect and pushes them to comment.

#### 3. Leverage a trend 📈

Posts perform better when they ride an existing conversation. If people already talk about it, your post takes off more easily.

Headline examples:

- "How I built a page with AI in 30 seconds using [tool name]."
- "My first landing page made entirely with a prompt (no code)."
- "I tested the tool everyone is using to build websites with AI…"

#### 4. Solve a real pain point 💊

The best content removes an immediate pain for your audience. Target feelings like:

- "You don't know how to code or build a site."
- "You don't want to pay a developer $2k."
- "You need to launch your business today."
- "You want a pro landing page to sell without wasting time."

The goal: your lead magnet makes them think "Finally, someone gave me a solution for free." A clearer solution means stronger virality.

### 📸 Image + DM = your funnel

You give a lot of value away for free in these posts. That is normal: all viral LinkedIn lead magnet posts work this way.

1. The post delivers value and visually teases the resource.
2. People comment a short keyword to get it.
3. You send the resource in a DM and start a conversation.
4. Later, you propose support, services or introductions and turn them into clients.

The resource in the DM must be relevant and high value, so people feel you over-deliver and comment again on your next posts.

### 🔁 Replicate what works

When a post works, replicate the format. Keep the structure and change:

- The angle
- The resource
- The examples
- The target audience

Over time people recognize your style and engage more naturally because they know you deliver real value.

To ride the wave:

- Answer the first comments fast.
- When someone comments "List", send the resource in a DM and reply under the comment with "Sent" or "I just sent it to you."

This shows activity under the post and signals strong engagement to the algorithm.

### 🔬 Anatomy of a great post

A great post is 10% hook and 90% visuals.

**The hook (text).** Keep it punchy and state the achievement clearly.

> "Here's how I created [outcome] using [tool] in 10 minutes. 👇"

The three best-performing hook types:

1. "I used to believe X, now I know Y"
2. "I was that person once (but everything changed)"
3. "How to get X in Y days" (lead magnet)

**The visual (media).**

- **Video:** a fast-paced screen recording of the tool doing the work.
- **Caption:** "Comment 'AI' and I'll send you the workflow."

The clearer the visual shows the value of the resource, the more people comment.
