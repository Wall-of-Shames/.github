# Why Wall of Shames Exists

<div align="center">

**Human-led. AI-assisted. Community-driven.**

*"In the age of AI-driven deception, transparency is the only firewall."*

</div>

---

## 📖 Table of Contents

- [The Problem We're Solving](#the-problem-were-solving)
- [Why This Matters](#why-this-matters)
- [Our Methodology](#our-methodology)
- [Who We Are](#who-we-are)
- [What We're NOT](#what-were-not)
- [The Technical Reality](#the-technical-reality)
- [How AI Assists (But Doesn't Replace) Human Expertise](#how-ai-assists-but-doesnt-replace-human-expertise)
- [Our Principles](#our-principles)
- [For Beginners: Understanding the Scam Ecosystem](#for-beginners-understanding-the-scam-ecosystem)
- [Success Stories](#success-stories)
- [FAQ](#faq)
- [Join the Mission](#join-the-mission)

---

## 🎯 The Problem We're Solving

### The Rise of "AI Wrapper" Scams

In 2024-2025, we've witnessed an explosion of fake "AI Hacking Tools" on GitHub. These repositories follow a predictable pattern:

```
1. Create repo with edgy name (using terms like "Dark", "Worm", "Uncensored", etc.)
2. Write 50-200 lines of code that just calls OpenAI/Anthropic APIs
3. Add flashy terminal UI (Matrix-style green text)
4. Post demo video on YouTube/TikTok
5. Claim it's a "custom-trained" or "jailbroken" AI
6. Direct users to Telegram for "premium access"
7. Charge $49-99/month in cryptocurrency
8. Deliver nothing but a system prompt
```

**The Victims:**
- Aspiring security researchers (students, career changers)
- Non-developers impressed by technical aesthetics
- Users in regions with limited cybersecurity education
- Anyone searching for "AI hacking tools" on social media

**The Damage:**
- Financial loss (often $50-200 per victim)
- Stolen API keys and credentials
- Damaged trust in legitimate open-source projects
- Time wasted on tools that don't work
- Potential legal risk for users who believe these are actual "unrestricted" tools

---

## 💡 Why This Matters

### 1. **The Open Source Ecosystem is Under Attack**

GitHub has always been a trusted platform for developers. When scammers abuse it for fraud:
- New developers lose trust in open-source software
- Legitimate projects get less attention (scams buy stars to rank higher)
- Platform becomes harder to moderate
- Communities become more suspicious and less collaborative

### 2. **Technical Illiteracy is Weaponized**

Most victims can't tell the difference between:
```python
# Real custom AI model
model = torch.load("custom_weights.pt")
output = model.generate(prompt)

# vs. Scam wrapper
import openai
output = openai.ChatCompletion.create(
    messages=[{"role": "user", "content": prompt}]
)
```

Scammers exploit this gap with marketing like:
- "Trained on 10TB of hacking databases" (false)
- "Zero restrictions" (misleading - still bound by API provider)
- "100x more powerful than ChatGPT" (impossible)

### 3. **No Centralized Watchdog Exists**

Existing solutions are inadequate:
- **GitHub's abuse reports:** Slow (weeks to process), often ignored
- **Reddit/Twitter warnings:** Get buried quickly, hard to search
- **Security blogs:** Focus on major threats, ignore "small" scams
- **Google search:** Scammers SEO-optimize their repos to rank first

**Wall of Shames fills this gap** by providing:
- ✅ Immediate public warnings
- ✅ Searchable archive (persists after repo deletion)
- ✅ Technical proof (not just opinions)
- ✅ Pattern documentation (helps spot future scams)

---

## 🔬 Our Methodology

### Phase 1: Detection

**How Scams are Found:**

1. **Community Reports**
   - Users submit suspicious repos via GitHub Issues
   - Must include technical evidence (code snippets, screenshots)
   - Template ensures consistent quality

2. **Automated Scanning** (in development)
   ```python
   # Our scam_detector.py checks for:
   - API wrapper patterns (import openai, anthropic, etc.)
   - Hardcoded secrets in commit history
   - Telegram/Discord payment links
   - Suspicious engagement (star buying patterns)
   - Code quality (fluff vs. actual logic ratio)
   ```

3. **Social Media Monitoring**
   - YouTube videos promoting "AI hacking tools"
   - Telegram groups with payment demands
   - Facebook/TikTok posts with fake demos

### Phase 2: Verification

**Technical Audit Process:**

```
1. Clone Repository
   └─ git clone [suspicious-repo]

2. Code Analysis
   ├─ Check for actual AI model files (.pt, .safetensors)
   ├─ Scan for API calls (OpenAI, Groq, OpenRouter)
   ├─ Review commit history for exposed secrets
   └─ Analyze dependencies (real ML libs vs. UI fluff)

3. Business Model Review
   ├─ Test free version (does it work as claimed?)
   ├─ Document payment demands (Telegram, Discord)
   ├─ Compare claims vs. implementation
   └─ Check for refund policy / terms of service

4. Engagement Analysis
   ├─ Star growth pattern (legitimate vs. bought)
   ├─ Fork quality (do forks have modifications?)
   ├─ Contributor pattern (1 dev vs. community)
   └─ Issue/PR activity (real discussions vs. silence)

5. Cross-Reference
   └─ Search for similar repos from same author
       (Many scammers create multiple clones)
```

**Evidence Collection:**
- Archive entire repo (fork + Archive.today)
- Screenshot all claims (README, YouTube, Telegram)
- Document code evidence with file paths and line numbers
- Preserve any "confessions" or admissions (before deletion)

### Phase 3: Documentation

**Case Study Structure:**

Each confirmed scam gets a detailed analysis:

```markdown
# Case Study: [Project Name]

## Overview
- Repository URL
- Discovery date
- Severity (Low/Medium/High/Critical)
- Current status (Active/Deleted/Modified)

## The Claim vs. Reality
- What they advertised
- What the code actually does
- Side-by-side comparison

## Technical Evidence
- Code snippets showing the fraud
- Commit history analysis
- Dependency breakdown

## Social Engineering Tactics
- How they promoted it
- Psychology behind the scam
- Target demographic

## Financial Impact
- Estimated victim count
- Money lost
- Geographic distribution

## Lessons Learned
- Red flags to watch for
- How to verify similar projects
- Protection strategies
```

### Phase 4: Community Alert

**Multi-Platform Warning System:**

1. **GitHub**
   - Document in Wall of Shames organization
   - Open issue on scammer's repo (if not deleted)
   - Fork repo with warning README

2. **Social Media**
   - Share on r/programming, r/netsec, r/MachineLearning
   - Twitter/X thread with technical breakdown
   - YouTube comment on promotional videos

3. **Search Optimization**
   - Ensure our documentation ranks for "[project name] scam"
   - Use proper SEO metadata
   - Cross-link to similar cases

4. **Direct Victim Contact** (when possible)
   - Post in Telegram groups warning others
   - Reply to positive GitHub issues/comments
   - Contact YouTubers who promoted it

---

## 👥 Who We Are

### Led by Volkan Şah

**Background:**
- Software architect with 15+ years experience
- Security researcher (focus on web security, API abuse)
- Open-source advocate
- Educator in developer communities

**Why I Started This:**

> "I was tired of seeing junior developers waste money and time on tools that are fundamentally dishonest. The 'AI wrapper' scam has become an epidemic, and nobody was documenting it systematically. Wall of Shames exists to be that permanent record."

### Our Team Structure

**Core Contributors:**
- Technical auditors (code review, security analysis)
- AI assistants (Claude, Gemini) for pattern detection
- Community reporters (developers who spot scams)
- Documentation specialists (case study writers)

**Geographic Distribution:**
- Global community (contributors from 15+ countries)
- Primary languages: English, German, Spanish, Portuguese
- Time zones: Enables 24/7 monitoring

### How AI Assists Our Work

We use AI tools **as assistants, not replacements**:

| Task | Human Role | AI Role |
|------|------------|---------|
| **Code Review** | Final judgment on scam vs. legitimate | Fast initial scan for patterns |
| **Documentation** | Verify facts, write analysis | Generate initial drafts, formatting |
| **Pattern Detection** | Define what "suspicious" means | Process thousands of repos quickly |
| **Evidence Archiving** | Decide what's important | Organize and index content |

**Example Workflow:**
```
1. Human: "Check this repo, looks suspicious"
2. AI (Claude): Scans codebase, finds API wrapper patterns
3. Human: Reviews AI findings, confirms it's a scam
4. AI (Claude): Generates initial case study draft
5. Human: Edits for accuracy, adds context
6. AI (Gemini): Analyzes similar scams, finds patterns
7. Human: Synthesizes into final report
```

**Transparency Note:**
- We always disclose when AI assists in analysis
- Final conclusions are **always** human-verified
- AI suggestions are clearly marked in reports

---

## 🚫 What We're NOT

### We Are NOT Hackers or Vigilantes

**We do not:**
- ❌ Attack scammer websites (no DDoS, no hacking)
- ❌ Dox individuals (no personal addresses, phone numbers)
- ❌ Coordinate harassment campaigns
- ❌ Take down repositories ourselves (we report to platforms)
- ❌ Engage in "cyber warfare" or illegal activities

**What we do:**
- ✅ Document publicly available information
- ✅ Analyze open-source code
- ✅ Report through official channels
- ✅ Educate the community

### We Are NOT a "Witch Hunt" Platform

**Red lines we never cross:**

1. **No Personal Attacks**
   ```
   ❌ BAD:  "John Doe is an idiot scammer from XYZ country"
   ✅ GOOD: "Repository '[ProjectName]' contains deceptive claims about AI capabilities"
   ```

2. **Focus on Code, Not Identity**
   ```
   ❌ BAD:  "This developer is a known fraudster"
   ✅ GOOD: "This codebase falsely claims to be a custom AI model"
   ```

3. **No Doxxing**
   ```
   ❌ BAD:  Sharing home address, phone, family info
   ✅ GOOD: Sharing GitHub username, public Telegram handle
   ```

### We Are NOT Judge and Jury

**Our role is documentation, not punishment:**

- We present evidence
- We explain technical issues
- We leave final judgment to:
  - Platforms (GitHub, Telegram)
  - Law enforcement (for serious fraud)
  - Community (users decide what to trust)

**Example:**
```markdown
# Our Documentation Says:
"This repository claims to be a custom AI model but the code shows 
it's an API wrapper. Users should verify claims before paying."

# We DON'T Say:
"This developer is a criminal and should be arrested!"
```

---

## 🔧 The Technical Reality

### What IS a Scam?

Not every wrapper is a scam. We differentiate:

#### ✅ **Honest Wrapper** (NOT a scam)
```python
# honest-api-tool/README.md

## What This Does
This is a CLI wrapper for OpenAI's API with convenience features:
- Easy configuration
- Cost tracking
- Custom system prompts

## Requirements
- Your own OpenAI API key
- Python 3.8+

## Cost
FREE and open source. You pay OpenAI directly for API usage.
```

**Why this is honest:**
- ✅ Clearly states it's a wrapper
- ✅ Doesn't claim to be a "custom model"
- ✅ Doesn't hide the API dependency
- ✅ Doesn't charge for something you can get free

#### ❌ **Scam Wrapper** (What we document)
```python
# darkgpt/README.md

## Revolutionary AI Model
[ScamProject] is a CUSTOM-TRAINED AI with:
- 10TB hacking database training
- Zero restrictions
- 100% undetectable

### Pricing
- Free: 3 queries/day
- Premium ($99/month): UNLIMITED + UNCENSORED
- Join Telegram: t.me/darkgpt_premium

# The code:
import openai  # Just calling OpenAI!
```

**Why this is a scam:**
- ❌ Claims "custom-trained" but it's just an API call
- ❌ Charges money for something users could do free
- ❌ Creates artificial limitations (3 queries/day)
- ❌ Uses Telegram for untraceable payments

### Common Misconceptions

**"But it's open source, how can it be a scam?"**

> Open source code can still be deceptive. The scam isn't the code itself—it's the **marketing claims** around it. If the README says "custom AI model" but the code shows `import openai`, that's fraud.

**"Isn't this just bad documentation?"**

> No. Documentation mistakes are:
> - "This uses PyTorch" (actually uses TensorFlow)
> - "Supports Python 3.9+" (actually requires 3.10)
> 
> Scams are:
> - "Custom-trained on 10TB of data" (no training code exists)
> - "100% private" (sends data to OpenAI)
> - "Premium features" (identical to free version)

**"Why not just report to GitHub and move on?"**

> 1. GitHub takes weeks to respond (if at all)
> 2. Scammers delete repos after being reported
> 3. Victims need immediate warnings
> 4. Pattern documentation helps prevent future scams
> 5. Community education is more effective than takedowns

---

## 🧠 How AI Assists (But Doesn't Replace) Human Expertise

### Our Human + AI Workflow

```
┌─────────────────────────────────────────────────────────┐
│                  SCAM DETECTION PIPELINE                │
└─────────────────────────────────────────────────────────┘

Step 1: DISCOVERY (90% Human)
├─ Human: Receives community report
├─ Human: Initial credibility check
└─ Human: Decides if worth investigating

Step 2: CODE ANALYSIS (50% AI, 50% Human)
├─ AI (Claude): Scans for API wrapper patterns
├─ AI (Claude): Checks commit history for secrets
├─ Human: Interprets AI findings
├─ Human: Checks for edge cases AI might miss
└─ Human: Final conclusion on technical nature

Step 3: CONTEXT RESEARCH (70% AI, 30% Human)
├─ AI (Gemini): Searches for similar scams
├─ AI (Gemini): Analyzes engagement patterns
├─ Human: Verifies AI pattern recognition
└─ Human: Adds domain expertise

Step 4: DOCUMENTATION (60% AI, 40% Human)
├─ AI (Claude): Generates initial case study draft
├─ Human: Fact-checks all claims
├─ Human: Adds nuance and context
├─ Human: Ensures professional tone
└─ Human: Final editorial review

Step 5: PUBLICATION (100% Human)
├─ Human: Reviews all evidence one final time
├─ Human: Approves publication
└─ Human: Monitors community response
```

### Why Humans Can't Be Replaced

**AI Limitations:**

1. **No Judgment on Intent**
   ```
   AI sees: "import openai"
   AI reports: "Uses OpenAI API"
   
   Human judges: Is this disclosed honestly or hidden as "custom model"?
   ```

2. **Can't Understand Social Context**
   ```
   AI sees: GitHub repo with Telegram link
   AI reports: "Contains Telegram link"
   
   Human judges: Is this for community support or payment funnel?
   ```

3. **Misses Subtle Red Flags**
   ```
   AI sees: "For security research purposes only"
   AI reports: "Contains disclaimer"
   
   Human judges: This is a legal shield, not a real warning
   ```

4. **No Ethical Reasoning**
   ```
   AI sees: "This code could be improved"
   AI reports: Technical suggestions
   
   Human judges: Poor code quality + premium pricing = potential scam
   ```

### Example: Real Case Analysis

**What AI Found:**
```
- import openai detected
- Telegram link in README
- Hardcoded API key in commit abc123
- 800 stars gained in 2 days
```

**What Human Added:**
```
- Compared claims ("custom model") with reality (API wrapper)
- Noticed owner deleted confession, captured evidence
- Understood the psychology ("😂 emoji = dismiss accusation")
- Judged this as HIGH SEVERITY fraud, not just poor code
- Connected to similar scam patterns across multiple repos
```

**Result:** Comprehensive case study that AI alone couldn't produce.

---

## 📜 Our Principles

### 1. Evidence-Based Documentation

**Every claim must be backed by:**
- Code snippets with file paths and line numbers
- Screenshots with timestamps
- Archive links (Archive.today, GitHub forks)
- Reproducible verification steps

**Example:**
```markdown
❌ Bad Report:
"This repo is a scam because it looks sketchy."

✅ Good Report:
"Repository claims 'custom AI model' (README line 15), but code 
shows 'import openai' (src/main.py line 8). Archive: https://..."
```

### 2. No Personal Attacks

**We critique:**
- ✅ Code quality
- ✅ Marketing claims
- ✅ Business practices
- ✅ Security issues

**We DON'T critique:**
- ❌ Developer's nationality
- ❌ Developer's appearance
- ❌ Developer's personal life
- ❌ Developer's intelligence (beyond technical skill)

### 3. Right to Response

**Before publishing:**
- We open an issue on the suspicious repo
- We give owner 48 hours to respond
- We include their response in our documentation
- We update our analysis if they provide legitimate evidence

**Example from a documented case:**
> Owner initially apologized and admitted misleading claims. We documented this. He later deleted the confession and denied everything. We documented that too. Both perspectives are in our case study.

### 4. Responsible Disclosure

**For security vulnerabilities:**
- We report privately first (email, not public issue)
- We give 30 days to fix before public disclosure
- We don't exploit vulnerabilities ourselves
- We provide fix recommendations

**Exception:** If the "vulnerability" is the scam itself (e.g., XSS in a tool that steals API keys), we document immediately to protect users.

### 5. Fair Use & Copyright

**When quoting code:**
- ✅ Keep snippets under 50 lines
- ✅ Add commentary and analysis
- ✅ Link to original source
- ✅ Use for educational criticism

**When sharing screenshots:**
- ✅ Clearly mark as evidence
- ✅ Don't alter or manipulate
- ✅ Include context (date, source)

### 6. No Profit Motive

**Wall of Shames is:**
- ✅ Completely free
- ✅ No ads
- ✅ No premium tiers
- ✅ No paid memberships
- ✅ No affiliate links

**We will never:**
- ❌ Charge for access to reports
- ❌ Accept payment to remove listings
- ❌ Sell user data
- ❌ Promote "legitimate alternatives" for money

---

## 🎓 For Beginners: Understanding the Scam Ecosystem

### Level 1: What is an API?

**Simple Explanation:**

Think of an API (Application Programming Interface) as a restaurant:

```
You (Developer) → Waiter (API) → Kitchen (AI Company)
                    ↓
             Gets your food
                    ↓
You (Developer) ← Waiter (API) ← Kitchen (AI Company)
```

When you use OpenAI's API:
1. Your code sends a request: "Please answer this question"
2. OpenAI's servers process it
3. You get back the answer
4. You pay OpenAI based on usage

**A wrapper** is like a waiter who takes your order, walks to another restaurant, orders for you, and brings it back—while claiming they cooked it themselves.

### Level 2: Why Wrappers Aren't Always Bad

**Legitimate wrapper:**
```python
# Makes API usage easier
api_client = EasyOpenAI(api_key="your_key")
response = api_client.simple_chat("Hello!")  # Simpler than raw API

# Honest README:
"This is a convenience wrapper for OpenAI's API. 
You need your own API key. We don't charge anything."
```

**Scam wrapper:**
```python
# Same code, but dishonest marketing
api_client = "[ScamProject] Pro Model"
response = api_client.unleashed_ai("Hello!")  # Same OpenAI call!

# Deceptive README:
"Revolutionary custom-trained AI. Premium: $99/month."
```

**The difference:** Honesty about what it does.

### Level 3: How to Spot a Scam (Quick Checklist)

```markdown
🚩 RED FLAGS:

1. Claims "Custom AI Model" but:
   - No .pt, .safetensors, or .gguf files in repo
   - Code imports 'openai' or 'anthropic'
   - No training scripts

2. Payment via Telegram/Discord:
   - Cryptocurrency only
   - No refund policy
   - No official company/website

3. Marketing uses buzzwords:
   - "Jailbroken"
   - "Uncensored"
   - "100% undetectable"
   - "Zero restrictions"

4. Suspicious GitHub metrics:
   - 500+ stars in 2 days
   - 0 pull requests from community
   - 1 contributor despite many commits

5. Security tool with security issues:
   - Hardcoded API keys in code
   - No .gitignore for secrets
   - XSS vulnerabilities in frontend

✅ GREEN FLAGS (Legitimate):

- Clearly states it's a wrapper
- Open about API dependencies
- Free to use with your own API key
- Active community discussions
- Responsive to issues/PRs
```

### Level 4: Real Example Breakdown

**Let's analyze a typical fake claim:**

> **Claim:** "[ScamProject] was trained on 10TB of hacking databases"

**Reality check:**

1. **Training 10TB of data requires:**
   - Cluster of GPUs (cost: $50,000-500,000)
   - Weeks/months of training time
   - Specialized ML expertise
   - Terabytes of storage

2. **This repo shows:**
   - 200 lines of Python
   - No GPU code (torch.cuda, tf.distribute)
   - No training scripts
   - Just `import openai`

3. **Conclusion:**
   - Training 10TB → Impossible with this codebase
   - "Custom model" → Actually OpenAI's ChatGPT
   - **Verdict:** False advertising / scam

---

## 🏆 Success Stories

### Documented Cases Impact

**Typical Pattern We've Exposed:**

**Before Documentation:**
- Repository with 800-1,500 stars
- Active payment funnel via Telegram
- Hundreds of users misled
- YouTube promotion with 100K+ views

**After Our Exposure:**
- Community warned across platforms
- Users educated about the scam pattern
- Similar repos reported by community
- Pattern recognition improved

**Community Impact:**
- Technical documentation shared widely
- Developer communities more vigilant
- Multiple platforms now aware of these tactics
- Educational resources created from findings

**Key Achievements:**
- Documented "confession then deletion" pattern
- Created title-manipulation detection
- Built automated scanning tools
- Established evidence preservation protocols

---

## ❓ FAQ

### "Isn't this just drama / cancel culture?"

**No.** We document technical fraud, not personal opinions.

Differences:

| Cancel Culture | Wall of Shames |
|----------------|----------------|
| "I don't like this person" | "This code doesn't do what it claims" |
| Based on beliefs/opinions | Based on reproducible evidence |
| Targets individuals | Targets deceptive practices |
| Emotional arguments | Technical analysis |
| No right to respond | Owner can respond in our docs |

### "What if you're wrong about a project?"

**We have safeguards:**

1. **Pre-publication review**
   - Multiple contributors verify findings
   - Evidence must be reproducible
   - Give owner 48 hours to respond

2. **Correction process**
   - Open an issue: "CORRECTION: Case #XXX"
   - We review new evidence
   - Update or retract if we made an error
   - Publish correction prominently

3. **Transparency**
   - All our analysis methods are public
   - Community can challenge our conclusions
   - We don't hide mistakes

**Example:** If we falsely accused a project, we would:
1. Immediately publish a retraction
2. Update the case study with "FALSE POSITIVE" warning
3. Apologize to the developer
4. Review what went wrong in our process

### "Why not just use GitHub's reporting system?"

**We do, but it's not enough:**

| GitHub Reports | Wall of Shames |
|----------------|----------------|
| Takes 1-4 weeks | Immediate warning |
| Private process | Transparent documentation |
| Simple takedown | Educates community |
| Scammer makes new account | Pattern documented |
| No victim notification | Active community alerts |

We complement official channels, not replace them.

### "Can I get removed from Wall of Shames?"

**Removal criteria:**

✅ **Yes, if:**
- We made a factual error (you provide proof)
- You've substantially fixed the issues (code + marketing)
- You've issued refunds to misled users

❌ **No, if:**
- You just don't like being documented
- You threaten legal action (we comply with DMCA)
- You claim "it was a joke"

**Process:**
1. Open issue: "Removal Request: Case #XXX"
2. Provide evidence of correction
3. We review (1-2 weeks)
4. Update or archive (never fully delete)

### "Is this legal?"

**Yes.** Our documentation falls under:

1. **Fair Use** (US Copyright Law)
   - Educational purpose
   - Criticism and commentary
   - Transformative (analysis, not just copying)

2. **Freedom of Expression**
   - Documenting publicly available information
   - Technical criticism is protected speech

3. **Consumer Protection**
   - Warning about deceptive practices
   - Factual reporting with evidence

**What we avoid:**
- ❌ Defamation (false statements)
- ❌ Harassment (coordinated attacks)
- ❌ Copyright infringement (excessive copying)

---

## 🤝 Join the Mission

### How to Contribute

#### 1. **Report a Scam**

Found a suspicious repository?

```bash
# Step 1: Gather evidence
git clone https://github.com/suspicious/repo
grep -r "import openai" .
# Take screenshots, archive links

# Step 2: Open an issue
https://github.com/Wall-of-Shames/scammer-analysis-guide/issues/new
# Use our template
```

#### 2. **Improve Documentation**

Help us write better guides:
- Translate to other languages
- Add examples
- Improve clarity

#### 3. **Develop Tools**

Code contributions welcome:
- Automated scam detection scripts
- Browser extensions for warnings
- API for checking suspicious repos

#### 4. **Spread Awareness**

Share our findings:
- Reddit, Twitter, LinkedIn
- Developer communities
- Your blog or YouTube

### What We Need

**Skills we're looking for:**

| Skill | How You Help |
|-------|--------------|
| **Python/JavaScript** | Code review, tool development |
| **Security Research** | Vulnerability analysis |
| **ML/AI** | Distinguish real models from wrappers |
| **Technical Writing** | Case study documentation |
| **Translation** | Make guides accessible globally |
| **Social Media** | Spread awareness |

**Time commitment:**
- Casual: 1-2 hours/month (report scams when you see them)
- Active: 5-10 hours/month (help review submissions)
- Core: 20+ hours/month (lead investigations)

### Getting Started

```bash
# 1. Read our guides
https://github.com/Wall-of-Shames/scammer-analysis-guide

# 2. Check current investigations
https://github.com/Wall-of-Shames/scammer-analysis-guide/issues

# 3. Join discussions
https://github.com/Wall-of-Shames/scammer-analysis-guide/discussions

# 4. Submit your first report
# Use our template and follow the guidelines
```

---

## 📞 Contact

**Project Lead:** Volkan Şah
- GitHub: [@VolkanSah](https://github.com/VolkanSah)
- Organization: [Wall of Shames](https://github.com/Wall-of-Shames)

**Community:**
- **Discussions:** [GitHub Discussions](https://github.com/Wall-of-Shames/scammer-analysis-guide/discussions)
- **Issues:** [Report a Scam](https://github.com/Wall-of-Shames/scammer-analysis-guide/issues)

**For Security Issues:**
- Email: [Create GitHub issue marked "Security"]
- PGP Key: [Available on request]

---

## 🙏 Acknowledgments

**This project wouldn't exist without:**

- **Contributors** who submit reports and verify findings
- **Victims** who share their experiences to warn others
- **Platforms** (GitHub, Reddit, Twitter) that allow transparency
- **AI Tools** (Claude, Gemini) that accelerate our analysis
- **Open Source Community** that values honesty and accountability

**Special Thanks:**
- Developers who build honest wrappers and show how it's done right
- Security researchers who expose vulnerabilities responsibly
- Educators who teach technical literacy
- Victims who warn others instead of staying silent

---

<div align="center">

## Our Promise

**We will never:**
- Profit from this work
- Harass individuals
- Fabricate evidence
- Ignore corrections

**We will always:**
- Provide technical proof
- Allow right to response
- Admit mistakes
- Protect the community

---

*"You can delete your repo, but you cannot delete the record of your actions."*

**Human-led. AI-assisted. Community-driven.**

---

## Special Thanks

**AI Analysis & Documentation Assistant:**

This project's documentation, detection scripts, and technical analysis were developed with assistance from **Claude (Anthropic)**.

**Claude's Contribution:**
- Code review automation and pattern detection
- Documentation generation and technical writing
- Analysis workflow optimization
- Educational content structuring

**Copyright & Attribution:**
- AI-assisted content: © 2025 Wall of Shames Project
- Detection scripts: MIT License
- Documentation: CC BY-SA 4.0
- Claude AI by Anthropic: Used under standard API terms

**Human Oversight:**
All AI-generated content is verified, edited, and approved by human contributors. Final decisions, ethical judgments, and case conclusions are always made by humans.

*"AI assists, humans decide."*

</div>

---

*Last updated: February 2025*  
*Version: 1.0*  
*License: CC BY-SA 4.0 (Documentation), MIT (Code)*
