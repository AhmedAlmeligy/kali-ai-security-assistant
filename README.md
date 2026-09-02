# AI-Enhanced Natural Language Assistant for Kali Linux

> Final Year Project — BSc (Hons) Cyber Security & Forensics, GCET, Muscat, Oman (2025)
> Recognized as one of the best final year projects at GCET

## Overview
Kali Linux's CLI is powerful but has a steep learning curve for beginners and creates
friction for experts. This project embeds an AI natural-language assistant directly into
Kali Linux, using Open Interpreter as the execution engine and a locally fine-tuned
Gemma 3 model, so users can issue security tasks in plain English while receiving
real-time educational explanations.

## Key Results
- 97.6% command-generation accuracy
- 96.3% execution success rate
- 91.2% intent-recognition accuracy (target was 80%)
- 99.2–100% threat-detection accuracy in the security validation layer
- 35% reduction in task completion time; beginners ran basic network scans in
  under 45 minutes vs. 2–3 hours traditionally
- 42% increase in user satisfaction; post-task quiz scores doubled

## Architecture (5 layers)
1. **User Interaction Layer** — conversational interface via Open Interpreter
2. **Natural Language Understanding Engine** — fine-tuned Gemma 3 for intent
   recognition & entity extraction
3. **Verification & Security Layer** — authentication, command validation,
   least-privilege whitelisting
4. **Integration & Execution Layer** — maps intent to Kali tools (Nmap, Metasploit)
   via sandboxed Python subprocess execution
5. **Feedback & Educational Module** — real-time "Did You Know?" explanations
   tied to each command

## Tech Stack
- **Language:** Python
- **NLP:** spaCy, NLTK
- **LLM:** Gemma 3 (locally fine-tuned, 8-bit quantized)
- **Execution engine:** Open Interpreter
- **Security:** OAuth, JWT
- **Data:** PostgreSQL (structured logs), MongoDB (unstructured session data)
- **Monitoring:** ELK Stack, Prometheus

## Methodology
Agile, mixed-methods approach — user interviews, iterative prototyping, and
quantitative evaluation across 10 representative security tasks on a clean Kali VM.

## Limitations
- Gemma 3 needs ~1.6GB RAM even after quantization — tight on low-end hardware
- Complex multi-part commands can be misinterpreted
- Currently covers a core subset of Kali tools (not yet Burp Suite, John the Ripper, SQLmap)
- Small evaluation cohort limits generalizability

## Future Work
Adaptive skill-level UI, full analytics dashboard, Active Directory integration,
personalized learning paths, voice interaction, plugin ecosystem, hybrid cloud-edge deployment.

## Author
**Ahmed Osama Almeligy** — Cyber Security & Forensics Graduate
- LinkedIn: [ahmed-al-meligy-89b16729b](https://www.linkedin.com/in/ahmed-al-meligy-89b16729b)
- Email: ahmedalmeligy2108@gmail.com
