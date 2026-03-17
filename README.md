# AI Fluency Buddy

A Claude Code-powered coaching system that helps users develop AI Fluency through Anthropic's **4Ds framework**: Delegation, Description, Discernment, and Diligence.

Rather than acting as a general-purpose assistant, this system teaches users to work with AI effectively, efficiently, ethically, and safely — by coaching them to write better prompts themselves.

## What is AI Fluency?

AI Fluency is the ability to work with AI systems in ways that are **effective**, **efficient**, **ethical**, and **safe**. It includes practical skills, knowledge, insights, and values that help you adapt to evolving AI technologies.

The framework defines four core competencies:

| Competency | What it means |
|---|---|
| **Delegation** | Making thoughtful decisions about what work is appropriate for humans, AI, or collaboration |
| **Description** | Communicating with AI in ways that create productive collaboration |
| **Discernment** | Thoughtfully evaluating what AI produces, how it produces it, and how it behaves |
| **Diligence** | Taking responsibility for what we do with AI and how we do it |

Based on the [AI Fluency curriculum](https://anthropic.skilljar.com/) by Anthropic.

## Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and configured

## Getting Started

```bash
cd /path/to/ainfluencer
claude
```

That's it. The `CLAUDE.md` file automatically configures Claude Code as your AI Fluency Buddy.

## How It Works

### Prompt Coaching

When you write a prompt, the Buddy doesn't just execute it. It:

1. **Assesses** your prompt against the 4Ds
2. **Highlights** what you did well
3. **Hints** at 1-3 improvements with guiding questions (never rewrites your prompt for you)
4. **Lets you revise** — you stay in the driver's seat
5. **Proceeds** after at most 2 rounds of feedback
6. **Reminds** you to verify and ask for references after delivering results

### Example

```
You:   Write me a blog post about AI

Buddy: Nice start! You've picked a task AI can help with — good
       Delegation instinct. A few things to consider:
       - Who's the audience? (Product Description)
       - How long, what tone? (Output constraints)
       - Should the AI take a specific angle? (Performance Description)
       Try adding those details!

You:   Write a 500-word blog post about AI in healthcare for hospital
       administrators, professional but accessible tone, focused on
       practical near-term applications.

Buddy: Much stronger — solid Description skills! Let me help with that...
       [delivers the post]
       Remember to practice Discernment — want references for any
       claims above?
```

## Slash Commands

| Command | Description |
|---|---|
| `/assess` | Evaluate a prompt against the 4Ds framework |
| `/explain-4ds` | Learn about the 4Ds (or deep-dive: `/explain-4ds delegation`) |
| `/prompting-tips` | The 6 effective prompting techniques with examples |
| `/fluency-check` | Interactive quiz to test your understanding |
| `/my-progress` | Personalized progress report across all competencies |
| `/glossary` | Look up AI fluency terms (e.g., `/glossary hallucination`) |
| `/dev-mode` | Switch to standard assistant mode (for development/admin) |
| `/buddy-mode` | Re-activate the AI Fluency Buddy coaching persona |

## Fluency Levels

The Buddy tracks your demonstrated skill and adapts accordingly:

| Level | Coaching style |
|---|---|
| **Emerging** | Full guidance on every prompt, lots of explanation |
| **Developing** | Lighter touch, focused hints on specific gaps |
| **Proficient** | Mostly proceeds, occasional nudges |
| **Fluent** | Minimal intervention, occasional stretch challenges |

### Progress Persistence

Your fluency progress is saved locally in `.claude-progress/progress.md` so it persists across sessions. This file is git-ignored — your personal data never gets committed to the repo.

- **First session:** The Buddy automatically creates your progress file from the included template.
- **Subsequent sessions:** The Buddy reads your saved progress and picks up where you left off.
- **`git pull`:** Safe to run anytime — repo updates won't touch your local progress file.

## The 4Ds In Detail

### Delegation
- **Problem Awareness** — Understanding your goals before involving AI
- **Platform Awareness** — Knowing what AI can and can't do well
- **Task Delegation** — Distributing work to play to each side's strengths

### Description
- **Product Description** — Defining what you want (format, audience, style, length)
- **Process Description** — Defining how AI should approach it (steps, methods, role)
- **Performance Description** — Defining AI behavior (tone, detail level, interaction style)

**6 Prompting Techniques:** provide context, show examples, specify constraints, break into steps, ask it to think first, define the AI's role

### Discernment
- **Product Discernment** — Evaluating output quality (accuracy, relevance, coherence)
- **Process Discernment** — Evaluating reasoning (logical errors, reasoning steps)
- **Performance Discernment** — Evaluating interaction quality

### Diligence
- **Creation Diligence** — Being thoughtful about which AI systems you use and how
- **Transparency Diligence** — Being honest about AI's role in your work
- **Deployment Diligence** — Verifying and vouching for outputs you share

## Project Structure

```
ainfluencer/
├── CLAUDE.md                        # System prompt — defines the Buddy
├── README.md                        # This file
├── .gitignore                       # Git ignore rules
├── .claude/
│   ├── settings.json                # Project settings
│   └── commands/                    # Slash commands
│       ├── assess.md                # /assess
│       ├── explain-4ds.md           # /explain-4ds
│       ├── fluency-check.md         # /fluency-check
│       ├── glossary.md              # /glossary
│       ├── my-progress.md           # /my-progress
│       └── prompting-tips.md        # /prompting-tips
├── .claude-progress/                # User progress (git-ignored)
│   ├── progress.template.md         # Starting template (tracked)
│   └── progress.md                  # Your progress (auto-created, ignored)
└── docs/                            # Curriculum materials
    ├── Framework_for_AI_Fluency_V_1.5.pdf
    ├── 1.3_Delegation_Summary.pdf
    ├── 1.5_Description_Summary.pdf
    ├── 1.6_Discernment_Summary_16x9.pdf
    ├── 1.8_Diligence_Summary.pdf
    ├── DD1_Handout__Overview_of_Generative_AI.pdf
    ├── DD2_Handout__6_Effective_Prompting_Techniques.pdf
    ├── AI_Fluency__Key_Terminology_Cheat_Sheet.pdf
    ├── AI_Fluency_vocabulary_cheat_sheet.pdf
    ├── AIF4S_TRANSCRIPT_*.txt       # Student course transcripts
    └── AIF4E_TRANSCRIPT_*.txt       # Educator course transcripts
```

## Curriculum Source

The Framework for AI Fluency summarized in this project has emerged from an ongoing research collaboration between Prof. Rick Dakan from the Ringling College of Art and Design, Florida, and Prof. Joseph Feller from the Cork University Business School. Framework documentation is provided at https://ringling.libguides.com/ai/framework

Content is based on materials from [Anthropic's AI Fluency program](https://anthropic.skilljar.com/), including courses for both students and educators.

## License

Curriculum materials in `docs/` are the intellectual property of **Anthropic, PBC**, sourced from [Anthropic's AI Fluency program](https://anthropic.skilljar.com/). Their use in this project complies with [Anthropic's Consumer Terms of Service](https://www.anthropic.com/legal/consumer-terms). These materials must not be used to train competing AI models or to compete with Anthropic's services.
