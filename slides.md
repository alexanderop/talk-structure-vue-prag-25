---
theme: ./theme
title: How to Structure Vue Projects 
website: alexop.dev
handle: alexanderopalic 
mdc: true
favicon: https://alexop.dev/favicon.svg 
highlighter: shiki
lineNumbers: true
layout: intro
---

# How to Structure Vue Projects

---

# Who here has ever struggled with structuring a new project?

---

# Why Structure Matters

> "Organizations which design systems are constrained to produce designs which are copies of the communication structures of these organizations."
— Mel Conway

Known as **Conway’s Law**.

---

# How to Choose a Structure

- Team size (solo → enterprise)  
- Complexity (simple → advanced)  
- Timeline (prototype → long-term)

---

# The Three Structures

📁 Flat → simple, file-type grouping  
🧩 Modular → feature-based, flexible  
🏢 Microfrontends → enterprise-scale  

---

# Rules for Comparison

- Does it scale with team size?  
- Does it reduce cognitive load?  
- Does it help or hurt AI/dev tooling?  
- What are the trade-offs?

---

# Flat Structure

Files grouped by type (components, utils, composables).  
Feels like a monolith — but when scoped per business subdomain, it gives **clarity** and even **AI indexing benefits**.

**Trade-offs**  
✅ Simple, fast to start  
✅ Easy onboarding  
❌ Long imports (fixed with TS path aliases)  
❌ Harder boundaries between features  

---

# Modular Monolith

Group by **feature folders** inside one repo.  
Important: a monorepo ≠ monolith.  

**Trade-offs**  
✅ Strong feature boundaries  
✅ Easier refactoring & scaling  
✅ Works well with path aliases  
❌ Configuration overhead (tooling, CI)  
❌ Deployment is unified (less flexibility)  

---

# Microfrontends

**Definition**: technical representation of a business subdomain with independent implementation and ownership.  

When do they work well?  
- Large organizations with **independent teams**  
- Clear **domain boundaries**  
- Long-lived projects  

**Trade-offs**  
✅ Independent deploys  
✅ Team autonomy  
✅ Scale across orgs  
❌ More infra complexity  
❌ Harder consistency (needs shared UI lib)  

---

# Example Challenge

How would you structure a “Tractor Store” app so that  
- Product Discovery, Details, and Checkout are independent,  
- yet the **user experience stays consistent**?

---

# AI and Structure

AI tools read project trees.  
Flat inside subdomains + modular boundaries = **AI-friendly**.  

---

# Recommendation

- Start flat for small apps.  
- Go modular when features grow.  
- Only adopt microfrontends if you have org-level scale.  

---

# Thanks

I write more about this at **alexop.dev** — check it out.