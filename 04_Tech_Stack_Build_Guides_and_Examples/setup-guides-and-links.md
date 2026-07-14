# Setup Guides and Links: Securely Deploying n8n for Your AI Agency in 2026

## Why This Exists

Choosing the right tools (see `tech-stack-comparison.md`) is only half the battle. The real differentiator for a profitable, retainer-based AI Automation Agency in 2026 is a reliable, secure, and cost-effective production deployment of your core orchestration layer—n8n.

Self-hosting n8n gives you data residency control (critical for GDPR, HIPAA, and client trust), predictable costs at scale, deep customization for agentic workflows, and the ability to build defensible IP. However, an insecure or flaky instance destroys client confidence and creates maintenance nightmares.

This guide delivers battle-tested, 2026-aligned setup paths with mandatory security hardening built in from step one. It prioritizes the official-recommended Docker Compose approach (with Traefik for automatic HTTPS) while also covering a traditional Nginx + Let's Encrypt pattern as requested, plus easier alternatives for prototyping.

## How to Use It

1. Start with the easiest option for testing (n8n Cloud or Railway).
2. Move to the recommended self-hosted Docker Compose path for any client work or retainers.
3. Follow the Critical Security Hardening section exactly—do not skip steps.
4. After setup, import workflows from the `example-workflows/` subfolder and configure credentials using environment variables only.
5. Document your instance details, backup plan, and update schedule in your internal agency SOPs (see Module 5).

**[CUSTOMIZE FOR YOUR NICHE]** — For healthcare, legal, or finance clients handling PHI/PII: Use a dedicated VPS in a compliant region (e.g., EU or US HIPAA-eligible), add extra volume encryption, enable comprehensive audit logging, and consider n8n Enterprise features or managed hosting with a BAA. For general ops/landscaping/ecom niches: The standard self-host path below is usually sufficient and highly cost-effective.

## How It Connects to Other Sections

* `tech-stack-comparison.md`: This is the direct implementation guide for the primary recommended tool (n8n self-host).
* `example-workflows/` (`lead-qualification-agent.md`, `support-triage-with-rag.md`, etc.): Import the public JSONs into the instance you build here. All examples assume a stable, HTTPS-accessible n8n with proper `WEBHOOK_URL`.
* **05_SOPs_Delivery_Workflows_and_QA (`build-checklist-and-qa-protocol.md`, `end-to-end-client-journey-map.md`):** Your QA, testing, and deployment processes run against this production instance.
* **07_Legal_Compliance_Operations (`compliance-checklist.md`):** The security controls, data residency choices, and encryption steps documented here support your DPA/ BAA claims and client contracts.
* **02_Business_Planning_and_Model (`financial-model-template.md`):** Hosting (~$5–50/mo VPS + domain) and maintenance time are core cost inputs.
* **06_Sales...:** Use your hardened, custom-branded n8n instance in demos to prove professionalism and data control.

---

## Option 1: Easiest for Prototyping — n8n Cloud

* **When to use:** Quick validation of workflows, client demos without infrastructure overhead, or very low-stakes internal agency automation.
* **Pros:** Zero maintenance, automatic updates, built-in scaling, official support.
* **Cons:** Less data control (cloud-hosted), potential compliance limitations, recurring usage-based or plan costs.
* **Quick Start:**
  1. Go to n8n.cloud and create an account.
  2. Create an instance and set up your admin user.
  3. Set your `WEBHOOK_URL` and test a simple workflow.

*Link:* Official n8n Cloud documentation — [docs.n8n.io](https://docs.n8n.io)

---

## Option 2: PaaS One-Click Style — Railway.app (or Similar)

Railway provides a simple Git-connected deployment experience with automatic HTTPS.
* **When to use:** Fast production-grade deploys without managing your own VPS or reverse proxy from scratch.
* **Steps (high-level):**
  1. Create a Railway account and new project.
  2. Connect a Git repo or use their n8n template (search Railway n8n template).
  3. Add required environment variables (especially `N8N_ENCRYPTION_KEY`, `WEBHOOK_URL`, `N8N_HOST`).
  4. Deploy — Railway handles SSL and scaling.
  5. Add a custom domain if needed.

*Link:* [railway.app](https://railway.app) — search their template marketplace for current n8n templates.

---

## Option 3: Recommended for Production & Control — Self-Hosted Docker Compose

This is the strongly preferred path for most AI agencies in 2026. It aligns with n8n’s strengths in agentic work, gives you full data control, and supports the retainer model profitably.

### Prerequisites
* Linux VPS (Hetzner Cloud, DigitalOcean, AWS Lightsail, etc. — start with 2–4 vCPU / 4–8 GB RAM for most agency workloads).
* Domain name with DNS A record pointing to your server IP (e.g., `n8n.yourdomain.com`).
* Docker and Docker Compose installed (`docker --version` and `docker compose version`).

### Official Recommended Approach (Docker Compose + Traefik)
n8n’s current documentation (as of mid-2026) strongly recommends Traefik as the reverse proxy because it handles automatic Let’s Encrypt SSL, routing, and security headers with minimal configuration.

Follow the complete official guide here:
[docs.n8n.io/deploy/host-n8n/install-options/use-a-cloud-provider/use-docker-compose](https://docs.n8n.io/deploy/host-n8n/install-options/use-a-cloud-provider/use-docker-compose)

#### Key Excerpts for Agency Setup:

1. **Create project directory and .env file**
   ```bash
   mkdir n8n-compose && cd n8n-compose
   ```
   Create `.env` (replace placeholders):
   ```env
   DOMAIN_NAME=yourdomain.com
   SUBDOMAIN=n8n
   GENERIC_TIMEZONE=America/New_York
   SSL_EMAIL=you@yourdomain.com

   # === CRITICAL SECURITY ===
   N8N_ENCRYPTION_KEY=REPLACE_WITH_STRONG_RANDOM_32+_CHAR_STRING
   N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS=true
   NODE_ENV=production

   # Webhook and host settings (HTTPS is mandatory)
   N8N_HOST=${SUBDOMAIN}.${DOMAIN_NAME}
   N8N_PORT=5678
   N8N_PROTOCOL=https
   WEBHOOK_URL=https://${SUBDOMAIN}.${DOMAIN_NAME}/
   ```
   Generate a strong encryption key:
   ```bash
   openssl rand -base64 32
   ```
   Copy the output into `N8N_ENCRYPTION_KEY` to encrypt stored credentials.

2. **Create compose.yaml**
   Use the official Traefik + n8n compose file from the official n8n documentation link above to run the service.

3. **Start the stack**
   ```bash
   docker compose up -d
   ```
   Access your instance at `https://n8n.yourdomain.com`.

### Alternative: Traditional Nginx + Let's Encrypt
If you prefer a classic Nginx setup on your host machine:

`docker-compose.yml` (exposing port only to localhost for security):
```yaml
services:
  n8n:
    image: docker.n8n.io/n8nio/n8n
    restart: always
    ports:
      - "127.0.0.1:5678:5678"
    env_file: .env
    volumes:
      - n8n_data:/home/node/.n8n
      - ./local-files:/files
    environment:
      - N8N_ENCRYPTION_KEY=${N8N_ENCRYPTION_KEY}
      - N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS=true
      - NODE_ENV=production
      - WEBHOOK_URL=https://n8n.yourdomain.com/
      - N8N_HOST=n8n.yourdomain.com
      - N8N_PROTOCOL=https

volumes:
  n8n_data:
```

Nginx configuration (`/etc/nginx/sites-available/n8n`):
```nginx
server {
    listen 80;
    server_name n8n.yourdomain.com;
    return 301 https://$host$request_uri;
}

server {
    listen 443 ssl http2;
    server_name n8n.yourdomain.com;

    ssl_certificate /etc/letsencrypt/live/n8n.yourdomain.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/n8n.yourdomain.com/privkey.pem;

    location / {
        proxy_pass http://127.0.0.1:5678;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```
Obtain Let's Encrypt certificate:
```bash
sudo certbot --nginx -d n8n.yourdomain.com
```
Hardening the firewall:
```bash
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw deny 5678/tcp
sudo ufw enable
```

---

## Critical Security Hardening (MANDATORY)

1. **Owner Account Setup:** The first user to access the web UI becomes the instance owner. Set a strong, unique password immediately.
2. **Restrict Public Registration:** Once the owner account is set, disable public signups. For team access, use invitations via the User Management panel in the settings.
3. **HTTPS Everywhere:** Never run n8n over plain HTTP in production. Webhooks and OAuth credentials require SSL.
4. **Credential Hygiene:** Always use n8n's native encrypted credential manager. Never paste API keys directly into HTTP nodes or prompt structures.
5. **Backups:** Schedule automated backups of the `n8n_data` Docker volume. Store snapshots offsite.

---

## Next Steps

- Verify HTTPS works and the instance logs are clean (`docker compose logs -f`).
- Go to `example-workflows/` to select and configure your first functional template.
