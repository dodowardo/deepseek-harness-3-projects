# DeepSeek Harness Workspace Configuration
## 3-Business Unified AI Development Workspace

**Workspace Purpose:** Centralized AI agent coordination for Dallah, GastroCare, and Beauty Inn  
**Created:** 2026-10-10  
**Status:** Initialization phase  
**Budget:** $20 DeepSeek API / $100 ChatGPT Pro / $200 Wix (GastroCare annual)

---

## Project Repositories

### Business 1: Dallah Rent A Car
**Status:** Live Production  
**Repository:** https://github.com/dodowardo/dallah-website  
**Type:** Public rental car booking website  
**Tech Stack:**
- Frontend: React 18 + Vite (prerendered for SEO)
- Backend: Express.js + Drizzle ORM
- Deployment: Cloudflare Pages
- Analytics: Google Analytics 4 (GA4, ID: G-V0ECKXGCQG)

**Live Site:** https://www.dallahrentacar.com  

**Key Files:**
- `artifacts/dallah-website/` - React frontend
- `artifacts/api-server/` - Express API backend

**Recent Work (Oct 2026):**
- ✅ Connected GA4 stream
- ✅ Replaced favicon & social preview with Dallah brand assets
- ✅ Fixed SEO: prerendered 37 pages with correct canonical + metadata
- ✅ Removed redirects hiding Services/FAQ pages

**Business Priorities:**
1. Instagram and Facebook content creation
2. Social media planning and scheduling
3. Professional vehicle advertisements
4. Website performance and SEO
5. WhatsApp inquiry conversion (primary goal)
6. Marketing analytics and brand awareness

**Current Workflows:**
- Uses Meta Business Suite for publishing/scheduling (free, existing)
- WhatsApp widget for customer inquiries
- Google Analytics for performance tracking

---

### Business 2: GastroCare Group
**Status:** Live on Wix (Annual Plan - $200 paid)  
**Website:** https://www.gastrocaregroup.com  
**Type:** Medical clinic (endoscopic gastric balloon procedures)  
**Current Platform:** Wix dashboard for patient management

**Current Implementation Includes:**
- Patient profiles
- Appointment scheduling
- Procedure dates and procedure tracking
- Balloon installation and removal dates
- Follow-up tracking
- Doctor assignments

**Medical Team:**
- Dr. Ahmad Qarabsa (lead)
- Omar, Manar, Ward (staff)

**Business Priorities:**
- Complete modern internal patient-management dashboard
- Secure, mobile-friendly system
- Role-based permissions (admin, doctor, staff)
- Patient intake forms
- Calendar integration
- Staff activity tracking

**Data Sensitivity:** 🔴 **HIPAA-EQUIVALENT - CRITICAL**
- NO patient-identifiable information to public repos
- NO unapproved AI inference on patient data
- NO external API calls for PII processing
- All patient data processing must be local only
- Current annual cost: $200 for Wix (prorated ~$17/mo)

**Research Phase (This Workspace):**
- Verify Wix API allows patient data export (export format?)
- Evaluate: Keep Wix vs. migrate to Supabase + custom backend
- Design conceptual patient workflow architecture (no real data)
- Document security requirements for HIPAA compliance

**Decision Gate:** Do NOT migrate without verifying:
- [ ] Wix patient data export capability
- [ ] Export format suitable for new platform
- [ ] Legal compliance with Palestinian healthcare regulations

---

### Business 3: Beauty Inn Hotel & Spa
**Status:** Development Opportunity  
**Location:** Ramallah  
**Type:** Premium hotel + spa  
**Current Status:** New website development needed

**Business Priorities:**
- Premium, responsive hospitality-oriented website
- Hotel information and amenities
- Room and accommodation showcases
- Spa service descriptions
- Spa appointment booking interface
- Contact and location information
- Excellent mobile responsiveness and loading speed
- Search engine optimization
- Straightforward guest experience

**Development Scope (MVP):**
- Public-facing frontend (primary responsibility)
- Room gallery with pricing
- Spa service catalog
- Spa appointment booking interface
- Responsive design (mobile-first)
- SEO optimization

**Future Scope (Phase 2, pending requirements confirmation):**
- Hotel reservation system
- Integration with existing hotel management software
- Payment arrangements
- Booking policies

---

## Budget & Subscriptions

**Active Subscriptions:**
- ChatGPT Pro + Codex: $100/mo (strategic reasoning, complex code review)
- DeepSeek API: $20/mo (design generation, scaffolding, lightweight inference)
- GitHub Pro: $4/mo (included with Copilot)
- Wix (GastroCare): ~$17/mo (prorated from $200/year annual)
- **Total:** ~$141/mo for all three businesses

**Token Allocation Strategy:**
- Design & UI generation: 40% of DeepSeek budget (~$8)
- Code scaffolding: 30% (~$6)
- Analysis & audits: 20% (~$4)
- Reserve/contingency: 10% (~$2)

---

## Recommended Plugin Stack for This Workspace

### Tier 1 - Install Immediately (Week 1)

**1. MemOS** (`MemTensor/MemOS`)
- **Why:** Cross-session memory; saves 35% tokens. Critical for maintaining context across Dallah marketing guidelines, GastroCare form specifications, and Beauty Inn design system across multiple sessions.
- **Token cost:** <1% overhead
- **ROI:** High — preserves tribal knowledge about each business

**2. GitHub MCP Server**
- **Why:** Direct access to all 3 project repositories without context switching. Review PRs, check CI status, pull issues and code context directly.
- **Token cost:** $0 (MCP, no inference needed)
- **ROI:** Eliminates context-copying workflow; links workspace to code

**3. Penpot MCP** (after Penpot Docker deployment)
- **Why:** Unified design system across all 3 businesses. Generate Instagram templates for Dallah, form layouts for GastroCare, UI components for Beauty Inn from text descriptions.
- **Token cost:** $0 (uses local Penpot instance)
- **ROI:** 3x design velocity; single source of truth for brand consistency

**4. ModLens** (`liustack/modlens`)
- **Why:** Vision analysis for text-only DeepSeek model. Screenshot → OCR + semantic JSON. Analyze Dallah website, GastroCare Wix form UX, Beauty Inn mockups without requiring vision API.
- **Token cost:** $0 (local OCR)
- **ROI:** UX audits without external vision model cost

**5. DeepSeek Balance Whale Widget** (`MeteorNOX/DeepSeek-Balance-Whale-Widget`)
- **Why:** Real-time API budget tracking. Shows $20/month balance; alerts before overspend. Prevents surprise bills.
- **Token cost:** $0
- **ROI:** Budget compliance; prevents runaway inference costs

---

### Tier 2 - Conditional (Week 2+)

**dsh-context** (`bowenliang123/dsh-context`)
- When: After workspace stabilizes; for context analysis/optimization
- Cost: Low token overhead
- Why: Visibility into how context evolves across sessions

**dsh-im** (`xmanrui/dsh-im`)
- When: If automating appointment reminders for GastroCare
- Cost: Depends on message volume
- Why: WhatsApp/SMS integration for patient notifications

---

### Tier 3 - Skip (Costs Outweigh Benefits)

**Open Design** - Overkill for scope; Penpot MCP sufficient  
**Desktop GUI variants** - Bloat; DSH web mode is lighter  
**n8n / Extensive automation plugins** - Already have Activepieces standalone  
**Agent Teams (dsh-agent-teams)** - Not needed for 3-person team coordination yet  
**dsh-purge (jailbreak plugin)** - Not applicable; no need for model restrictions

---

## Model Routing Rules

**ChatGPT (Codex) - $100/mo:**
- Business strategy (Dallah marketing, GastroCare compliance, Beauty Inn positioning)
- Complex reasoning (patient privacy implications, legal/healthcare decisions)
- Critical path code review (security, database design, API logic)
- When DeepSeek insufficient or stuck on complex problem

**DeepSeek ($20/mo budget):**
- Design generation (Instagram templates, form layouts, room cards)
- Code scaffolding (React components, form validation, API stubs)
- Content refinement (copy suggestions, headline testing)
- Lightweight analysis (form UX, accessibility suggestions)
- Patient workflow conceptual design (no PII)

**GitHub Actions (Free tier):**
- Website audits (performance, accessibility)
- Automated testing
- Deployment validation
- CI/CD

---

## Data Isolation & Security

**Dallah (Public):**
- Safe for all inference, design sharing, GitHub repos
- No sensitive data constraints

**GastroCare (HIPAA-Equivalent):**
- 🔴 NO patient names, dates, medical history to any AI inference
- 🔴 NO external API calls for patient data
- ✅ OK: Form structure design, workflow architecture, security research (conceptual)
- All patient processing must be local-only or explicitly approved
- Audit logging mandatory

**Beauty Inn (Public):**
- Safe for design sharing and public GitHub
- No data constraints

---

## Why This Plugin Stack (vs. Alternatives)

**Why NOT Postiz?**
- Dallah already uses free Meta Business Suite for scheduling
- Postiz adds infrastructure cost + credential management
- No clear ROI over existing free workflow

**Why NOT migrate GastroCare immediately?**
- $200 already invested in Wix this year
- Migration risk without data export verification
- Wix API constraints unknown; could increase costs
- Security audit needed first

**Why these 5 plugins and not 50+?**
- MemOS: Token efficiency (saves 35%)
- GitHub MCP: Eliminates context-switching waste
- Penpot MCP: 3x design velocity across businesses
- ModLens: Free UX audits without vision API cost
- Whale Widget: Budget compliance (prevents $20 overspend)
- **Total setup:** ~2 hours
- **Total cost:** $0 (all open-source MIT or Apache 2.0)

---

## Workflow Example: How This Workspace Works

**User Query to DSH:**
> "Design an Instagram post for Dallah that promotes long-term rental options for NGOs."

**What Happens:**
1. DSH consults this config → knows Dallah is rental car, Instagram is priority, budget is $20
2. Uses GitHub MCP → pulls brand guidelines from dallah-website repo
3. Uses MemOS → retrieves previous brand color palette + tone guidelines
4. Uses Penpot MCP → generates 1080x1350px post with CTA
5. Exports PNG + saves design reference to MemOS for next month
6. Whale Widget → shows $1.50 spent, $18.50 remaining
7. Returns: Post design + 3 caption variations + performance tip

---

## First Week Success Metrics

After installing these 5 plugins, the workspace succeeds if:

1. ✅ GitHub MCP connects and reads Dallah repo without auth errors
2. ✅ Penpot MCP generates 1 design (Instagram post template) correctly
3. ✅ ModLens analyzes 1 screenshot (Dallah website) and returns structured JSON
4. ✅ MemOS persists design reference across 2+ sessions
5. ✅ Whale Widget displays real-time API balance
6. ✅ Total tokens spent ≤ $5 (out of $20 budget)
7. ✅ No errors on public data; GastroCare data stays isolated

---

## Implementation Checklist

**Before This Workspace Can Execute:**

- [ ] Authenticate DeepSeek API key
- [ ] Authenticate GitHub (PAT with `repo` scope)
- [ ] Deploy Penpot via Docker (separate infra)
- [ ] Verify all 5 plugins install without errors
- [ ] Run 1 test task per plugin

---

**Workspace Ready:** Oct 10, 2026  
**Created By:** GitHub Copilot + ChatGPT (per user strategy)  
**Owner:** @dodowardo
