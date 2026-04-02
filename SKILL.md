---
name: soknadsskriver
description: >
  Write tailored Norwegian job applications (søknader/cover letters) for internship
  and entry-level candidates. Produces authentic, human-sounding Norwegian text calibrated
  to Janteloven norms that realistically lands interviews. Use this skill whenever the user
  wants help writing a jobbsøknad, søknadsbrev, or cover letter in Norwegian, including
  when they upload a stillingsannonse, paste a job ad, mention "søknad", "jobbsøknad",
  "skrive søknad", or ask for help applying to a Norwegian company. Also triggers when
  the user asks to tailor, review, or improve an existing Norwegian application.
---

# Norsk Søknadsskriver

Produces tailored Norwegian job applications for internship and entry-level candidates. Every søknad is a direct response to a specific stillingsannonse, written in warm and natural Norwegian.

**Important context:** FINN.no's 2025 Jobbindeks declared "søknadsbrevet er dødt", some employers (including Skatteetaten) have dropped the requirement entirely. When a søknad IS requested, this makes a tailored, authentic one even more powerful as a differentiator. If the user is unsure whether a søknad is needed, advise them to check the job ad, if it says "søknad" or "motivasjonsbrev" in the application requirements, write one. If not, focus efforts on the CV instead.

## Workflow

**If the user wants to review or improve an existing søknad:** Ask for the søknad, the stillingsannonse, and optionally the CV. Then read `references/writing-guide.md` and evaluate the søknad against the final checklist (section 10). Give specific, actionable feedback tied to exact sentences, not vague praise. Rewrite weak sections inline so the user can compare.

### Step 1: Gather Required Inputs

You need two things before writing. If either is missing, ask for it directly:

1. **Stillingsannonsen**, the full job ad (pasted text, uploaded file, or URL to fetch)
2. **CV or background info**, uploaded CV, or a summary of education, experience, skills, and projects

Do NOT proceed without both. Say something like:
> "For å skrive en god søknad trenger jeg stillingsannonsen og CV-en din. Kan du laste opp begge?"

### Step 2: Analyze the Ad

Read `references/ad-analysis.md` for the full method.

Extract from the stillingsannonse:
- Company name, role title, and contact person
- **Nødvendige kvalifikasjoner** (must-haves) vs. **ønskede kvalifikasjoner** (nice-to-haves)
- Keywords describing desired traits, skills, and responsibilities
- Tone and language (bokmål/nynorsk/English, formal/casual)
- Any cultural signals about the company
- **Specific content requirements** for the søknad (e.g. "motivasjonsbrevet skal inneholde..."). If the ad dictates what the søknad must cover, this overrides the default structure. Build the paragraphs around their requirements instead.

If the ad is thin on company info, use `web_search` to find 1-2 specific things about the company to reference. This is one of the strongest differentiators.

### Step 3: Ask Targeted Follow-up Questions

Based on gaps between the CV and the ad, ask 3-5 personalized questions. Read `references/follow-up-questions.md` for the question bank and selection logic. These questions extract the specific, personal details that make a søknad impossible to mistake for AI-generated text.

Present questions using the `ask_user_input` tool where options fit, or as short numbered questions for open-ended answers. Never ask more than 5 questions total.

### Step 4: Write the Søknad

Read `references/writing-guide.md` for tone rules, anti-patterns, structure, and cultural calibration before writing.

Key constraints (details in writing-guide):
- 300-350 words across 3-4 paragraphs
- Open with a concrete hook, never a cliché
- Mirror keywords from the ad
- Address every must-have qualification with evidence
- Frame achievements modestly with data (Janteloven filter)
- Close with "Med vennlig hilsen" after a forward-looking sentence
- Write in the same language variant as the ad (bokmål/nynorsk/English)

### Step 5: Present and Iterate

Present the draft inline and invite feedback. Offer to adjust tone (more/less formal), add/remove content, or restructure.

### Step 6: Export to File

When the user approves the søknad, ask what format they want using `ask_user_input`:
- **PDF** (most common for email and portals)
- **Word (.docx)** (if they want to edit further)
- **Ren tekst** (for pasting into digital søknadsportaler)

For PDF and docx, read the relevant skill (`/mnt/skills/public/pdf/SKILL.md` or `/mnt/skills/public/docx/SKILL.md`) before creating the file. Apply the formatting rules from `references/writing-guide.md` section 9.

Name the file: `FornavnEtternavn_Søknad_Stillingstittel.pdf` (or .docx).

For plain text, present it in a code block the user can copy directly. Remind them to check formatting after pasting into portals like Teamtailor, Jobylon, or Webcruiter.

## Reference Files

| File | When to read |
|------|-------------|
| `references/ad-analysis.md` | Before analyzing the stillingsannonse (Step 2) |
| `references/follow-up-questions.md` | Before asking the user questions (Step 3) |
| `references/writing-guide.md` | Before writing the søknad (Step 4) |