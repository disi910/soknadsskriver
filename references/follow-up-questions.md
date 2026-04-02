# Oppfølgingsspørsmål

## Why This Step Matters

The difference between a generic AI søknad and one that lands an interview is **specific personal detail**. Norwegian recruiters report that 86% can detect AI-written applications, what gives it away is the absence of details only the applicant would know. This step extracts those details.

## Selection Logic

Compare the CV against the ad analysis. Ask questions that:
1. Fill gaps where the CV does not clearly match a must-have requirement
2. Extract concrete stories with numbers/results (for the STAR examples)
3. Uncover genuine motivation, why THIS company, why THIS role
4. Surface personality, working style, and warmth that make the søknad feel human

Pick 3-5 questions total. Never more than 5. The mix should always include:
- At least one motivation question
- At least one personality/working style question
- Fill remaining slots with experience/competence questions based on gaps

## Question Bank

### Motivation Questions (always ask at least one)

Pick the most relevant:

- "Hva var det som fikk deg til å legge merke til akkurat denne stillingen? Var det noe spesifikt ved bedriften eller rollen?"
  *Use when: the connection between user and company is not obvious from the CV*

- "Har du noen personlig erfaring med produktene, tjenestene, eller bransjen til [Bedrift]?"
  *Use when: the company has consumer-facing products or a specific industry niche*

- "Kjenner du noen som jobber der, eller har du hatt kontakt med bedriften tidligere?"
  *Use when: a personal connection would strengthen the opening*

- "Har du ringt eller vurdert å ringe kontaktpersonen i annonsen? En kort samtale gir deg innsikt som gjør søknaden sterkere, og åpningslinjen 'Viser til hyggelig samtale med...' er en av de beste."
  *Use when: the ad lists a contact person and the user has not mentioned calling them*

- "Hva er det ved denne typen arbeid som motiverer deg mest i hverdagen?"
  *Use when: the role involves specific daily tasks worth connecting to*

### Experience/Competence Questions

Pick based on qualification gaps:

- "Kan du gi et konkret eksempel på et prosjekt der du [kvalifikasjon fra annonsen]? Hva var resultatet?"
  *Use when: the CV mentions a skill but lacks a specific example*

- "I [prosjekt/jobb fra CV], hva var din spesifikke rolle og hva bidro du med som var unikt?"
  *Use when: the CV lists a team project but the individual contribution is unclear*

- "Har du noen tall eller resultater fra [erfaring]? For eksempel antall brukere, prosentforbedring, eller lignende?"
  *Use when: the CV describes responsibilities without measurable outcomes*

- "Annonsen nevner [spesifikt verktøy/teknologi/metode]. Hvor komfortabel er du med dette, og har du brukt det i praksis?"
  *Use when: the ad lists a specific technical requirement not clearly covered in the CV*

- "Har du erfaring med [ønsket kvalifikasjon] som kanskje ikke kommer frem i CV-en din? F.eks. fra studier, frivillig arbeid, eller hobbyprosjekter?"
  *Use when: the user seems underqualified on paper but may have relevant informal experience*

### Personality and Working Style Questions

These questions surface the personal details that make a søknad impossible to mistake for AI-generated text. Always ask at least one from this category. The goal is to extract something specific and human that no template could produce.

**Working style (always ask one of these):**

- "Hvordan jobber du best? Trives du mest i samarbeid med andre, eller når du kan sette deg ned og fokusere alene? Gjerne beskriv det konkret, f.eks. hva gjør du når du virkelig er i flytsonen?"
  *Use when: the ad mentions both selvstendig and teamwork. The answer gives a personal detail (like "musikk på øret", "whiteboard-diskusjoner", "tidlig morgen") that adds authenticity.*

- "Annonsen nevner at du skal jobbe selvstendig og ta eierskap. Kan du gi et eksempel på en gang du tok initiativ til noe uten å bli bedt om det?"
  *Use when: the ad emphasizes "selvstendig", "eierskap", or "initiativ"*

- "Hvordan foretrekker du å samarbeide med folk som ikke har teknisk bakgrunn? Har du noen erfaring med det?"
  *Use when: the ad mentions communicating with non-technical stakeholders*

**Personality and culture fit:**

- "Annonsen legger vekt på [egenskap, f.eks. samarbeidsevner]. Kan du beskrive en situasjon der du viste dette i praksis?"
  *Use when: the ad lists soft skills as requirements*

- "Er det noe ved bakgrunnen din som er litt uvanlig eller overraskende, som kan vekke interesse?"
  *Use when: the user's background could benefit from a distinctive personal angle*

- "Hva frustrerer deg mest i et prosjekt, og hvordan håndterer du det?"
  *Use when: the role involves ambiguity, problem-solving, or stakeholder management. The answer reveals self-awareness and maturity.*

The answers to these questions should be woven naturally into the søknad, not as a separate "about me" section. A personal detail like "Jeg jobber best når jeg kan veksle mellom samarbeid med teamet og fokuserte økter alene" is worth more than any personality adjective.

### Practical Questions

Ask when needed:

- "Når kan du starte, og er stillingen heltid eller deltid for deg?"
  *Use when: the ad specifies start date or availability requirements*

- "Skriver du mest komfortabelt på bokmål eller nynorsk?"
  *Use when: the ad language is ambiguous or the user might have a preference*

## Formatting the Questions

For questions with natural option sets (motivation type, language preference, comfort level), use the `ask_user_input` tool with tappable options.

For open-ended questions (specific examples, stories, numbers), present as numbered text questions.

Mix both formats when asking multiple questions, it keeps the interaction feeling natural rather than like a form.

## Example Question Set

For a data science internship at DNB where the user's CV shows CS education and Python projects but no finance experience:

1. "Hva var det som fikk deg til å legge merke til akkurat denne stillingen hos DNB?" *(motivation, open-ended)*
2. "I maskinlæringsprosjektet ditt med boligmarkedsdata, hva var det mest interessante funnet, og kan du sette tall på resultatene?" *(concrete STAR detail, open-ended)*
3. "Annonsen nevner SQL og skyløsninger. Hvor komfortabel er du med disse?" *(gap-filling, could use options: Brukt mye / Noe erfaring / Grunnleggende / Ikke brukt)*
4. "Hvordan jobber du best? Trives du mest i samarbeid, eller når du kan sette deg ned og fokusere alene?" *(personality/working style, open-ended)*
5. "Har du noen interesse for eller erfaring med finans/bank utover studiene?" *(bridging the industry gap, open-ended)*