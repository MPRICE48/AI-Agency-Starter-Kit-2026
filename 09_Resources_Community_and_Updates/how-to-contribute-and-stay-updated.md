# How to Contribute and Stay Updated

**Keeping Your Fork Current and Helping Improve the AI Agency Starter Kit 2026**

*Module 9: Resources, Community, and Updates | AI Agency Starter Kit 2026*

---

## Why This Exists

The AI automation and agent landscape moves extremely fast. New tools, patterns, pricing models, and real-world lessons about what actually works for profitable retainers emerge constantly. 

A static kit would quickly become outdated. By making this repository easy to fork and contribute to, we create a living resource that improves over time through collective practitioner experience.

---

## Step-by-Step Sync Workflow

### 1. Fork the Repository (One-Time Setup)
1. Go to the main repository on GitHub.
2. Click the **Fork** button (top right).
3. Choose your account as the destination.

### 2. Clone Your Fork Locally
```bash
git clone https://github.com/YOUR_USERNAME/AI-Agency-Starter-Kit-2026.git
cd AI-Agency-Starter-Kit-2026
```

### 3. Add the Upstream Remote
This allows you to pull the latest changes from the official kit:
```bash
git remote add upstream https://github.com/original-org/AI-Agency-Starter-Kit-2026.git
git remote -v   # Verify both origin and upstream exist
```

### 4. Keep Your Fork Synchronized
Run this regularly to stay updated with upstream bug fixes and additions:
```bash
# 1. Fetch latest changes from upstream
git fetch upstream

# 2. Switch to main branch
git checkout main

# 3. Merge upstream changes
git merge upstream/main

# 4. Push updates to your fork
git push origin main
```
*Tip: Sync your fork at least once every 1–2 weeks, or immediately before starting a new customization.*

---

## How to Contribute (Pull Request Process)

We welcome community contributions that improve templates, guides, or tool recommendations.

1. **Create a new branch:**
   ```bash
   git checkout -b feature/add-new-tool-or-niche-example
   ```
2. **Make your changes following these guidelines:**
   - Keep content aligned with the kit philosophy (retainer focus, security first).
   - Include `[CUSTOMIZE FOR YOUR NICHE]` placeholders where appropriate.
   - Never commit real secrets, API keys, or client-identifiable data.
3. **Commit with clear messages:**
   ```bash
   git add .
   git commit -m "Add practical example for landscaping niche in value-proposition-canvas-template.md"
   ```
4. **Push your branch:**
   ```bash
   git push origin feature/add-new-tool-or-niche-example
   ```
5. **Open a Pull Request (PR) on GitHub:**
   - Go to the original repository.
   - Click "Compare & pull request".
   - Explain what you changed and why it helps agency builders.

---

## Security & Quality Review Requirements

All community-submitted Pull Requests are reviewed against this checklist before merging:
- **No secrets or credentials:** All keys, passwords, and sensitive values must use environment variables (`$env.VAR_NAME` or equivalent).
- **Alignment with philosophy:** Changes must support niche focus, productized retainer models, and agentic systems with human oversight.
- **Security best practices:** Proper input validation, secure DPA disclosures, and warnings about data privacy.
- **Quality & consistency:** Follows the existing structure and tone.
- **Actionable & tested:** All scripts or workflow JSONs should be verified.

---

## Common Pitfalls & Mitigations

- **Merge conflicts after long periods without syncing:** Sync weekly to minimize drift. Resolve conflicts carefully and test files.
- **Accidentally committing secrets:** Set up your `.gitignore` properly. Never hardcode credentials in your code files or n8n nodes. Run `git diff` before committing.
- **drift from the kit’s retainer-focused philosophy:** Read the core principles in the master README before submitting changes.
