# Sage and Willow Website

Estate planning for Nigerian Canadians. Dual-jurisdiction expertise bridging Canada and Nigeria.

## Sites

| Path | Description |
|------|-------------|
| `/` | Main landing page (services-focused) |
| `/companion` | AI companion variant (Sage & Willow guides) |

## Tech Stack

- HTML + Tailwind CSS (CDN)
- Tally.so for forms/survey
- Vercel for hosting

## Local Development

```bash
python3 -m http.server 8080
# Open http://localhost:8080
```

## Deployment

### Vercel (Recommended)

1. Push to GitHub
2. Connect repo to Vercel
3. Deploy (auto-detects static site)
4. Add custom domain: sageandwillow.online

### Domain Setup (Namecheap → Vercel)

1. In Vercel: Project Settings → Domains → Add `sageandwillow.online`
2. In Namecheap: Advanced DNS → Add records:
   - Type: A, Host: @, Value: 76.76.21.21
   - Type: CNAME, Host: www, Value: cname.vercel-dns.com

## Forms

- **Survey**: https://tally.so/r/NpDZEG (embedded on both sites)
- **Dashboard**: https://tally.so (login to view responses)

## Related Files

- `artefacts/tasks/sage-and-willow-website.md` - Task tracking
- `artefacts/opportunities/sage-and-willow.md` - Business concept
- `artefacts/opportunities/sage-and-willow-research.md` - Market research
