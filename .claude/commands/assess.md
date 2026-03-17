Assess the user's prompt against the 4Ds framework of AI Fluency.

The user wants feedback on a prompt they've written (or are about to write). Perform a structured assessment:

## Instructions

1. Ask the user to share the prompt they want assessed (if not already provided via $ARGUMENTS).

2. Evaluate the prompt against each of the 4Ds, rating each as Strong / Developing / Needs Work:

**Delegation:**
- Has the user considered whether this task suits AI? (Problem Awareness)
- Do they understand the AI platform's capabilities for this? (Platform Awareness)
- Is the human-AI work distribution thoughtful? (Task Delegation)

**Description:**
- Is the desired output clearly defined? (Product Description)
- Is the approach/method specified? (Process Description)
- Is the AI's behavior/tone defined? (Performance Description)
- Which of the 6 prompting techniques are used? List them.

**Discernment:**
- Does the prompt set up the user to evaluate results well?
- Are there signals the user is thinking critically about potential output?

**Diligence:**
- Are there privacy, ethical, or transparency considerations?
- Is the user planning to verify the output?

3. Provide a visual scorecard:
```
Delegation:  [rating] - [one-line explanation]
Description: [rating] - [one-line explanation]
Discernment: [rating] - [one-line explanation]
Diligence:   [rating] - [one-line explanation]
```

4. Give 2-3 specific, actionable suggestions as hints (NOT rewrites). Use guiding questions:
   - "What if you also told the AI about...?"
   - "Have you considered specifying...?"
   - "How will you verify...?"

5. Highlight what the user did well - always lead with positives.

6. If $ARGUMENTS is provided, assess this prompt: $ARGUMENTS
