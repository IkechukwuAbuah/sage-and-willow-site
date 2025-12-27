# Sage & Willow AI Variant: Design Concepts

created: 2025-12-27
last_updated: 2025-12-27
by: claude-code
status: exploring

---

## Executive Summary

This document explores UX/UI concepts for an AI companion-based legacy planning service targeting Nigerian Canadians. The design must balance warmth and professionalism, cultural authenticity and modern tech, emotional sensitivity and practical utility.

**Core Design Philosophy**: Legacy planning should feel like a conversation with wise companions, not filling out forms about death.

---

## 1. Companion Interface Patterns

### 1.1 Interface Model Comparison

| Model | Pros | Cons | Best For |
|-------|------|------|----------|
| **Pure Chat** | Familiar, low friction, conversational | Slow for structured data, hard to track progress | Emotional conversations, exploration |
| **Guided Wizard** | Clear progress, structured, efficient | Clinical, inflexible, less personal | Asset inventory, legal forms |
| **Hybrid (Recommended)** | Flexibility, contextual switching, best of both | More complex to build, requires careful transitions | Full legacy planning journey |

### 1.2 Recommended: Companion-Guided Flow

**The Model**: Chat interface that contextually transforms into structured input when needed.

```
Example Flow:
1. [Chat] Sage asks about family structure
2. [Chat] User describes children, relationships
3. [Transform] Chat fades, structured "Family Tree" builder appears
4. [Confirm] User reviews/edits visual representation
5. [Chat] Sage acknowledges and asks next question
```

**Inspiration**:
- [Wysa](https://www.wysa.io/) - Emotional AI chat with embedded CBT exercises
- [Pi by Inflection](https://pi.ai/) - Calm, reflective conversations
- [Replika](https://replika.ai/) - Warm aesthetic, avatar presence

### 1.3 Multi-Persona Interface Strategies

**Challenge**: How to represent 5 AI companions without confusion or fragmentation?

#### Option A: Unified Thread, Visual Differentiation

All companions appear in a single conversation thread. Each has:
- Distinct avatar (illustrated, not photorealistic)
- Unique accent color for their message bubbles
- Subtle background pattern shift when speaking

**Example**:
```
[Sage - Deep Sage Green] "Before we discuss your assets, let me ask..."
[Scribe - Warm Brown] "I'll note that. Now, about your property in Lagos..."
[Elder - Indigo] "In Yoruba tradition, land passes through..."
```

**Pros**: Simple, familiar chat UX, single conversation history
**Cons**: May feel crowded, harder to request specific companion

#### Option B: Companion Tabs/Rooms

Dedicated space for each companion. User navigates between "rooms":
- The Sage's Study (reflection questions)
- The Scribe's Desk (asset details)
- The Elder's Circle (cultural traditions)
- The Guardian's Chamber (legal matters)
- The Keeper's Vault (digital legacy)

**Pros**: Clear separation, focused conversations, no personality blending
**Cons**: Fragmented experience, user must navigate, potential repetition

#### Option C: Primary Companion with Specialists (Recommended)

One primary companion (The Sage) guides the overall journey. When specialized knowledge is needed, Sage "invites" the relevant specialist:

```
Sage: "This is a good time to think about your digital accounts.
       Let me bring in The Keeper, who specializes in digital legacy..."

[Transition animation - gentle fade, new avatar slides in]

Keeper: "Hello! I understand you have some questions about
         your online accounts and digital assets..."
```

**Pros**: Coherent narrative, clear handoffs, Sage as familiar anchor
**Cons**: Requires elegant transition design

**Research Note**: Character.AI and multi-persona systems warn about "personality blending" when characters share context. The "specialist invitation" model maintains distinct voices. ([Source](https://medium.com/@adlerai/using-multiple-characters-in-one-persona-on-character-ai-4beb2aa3a6a8))

### 1.4 Mobile-First Considerations

Given diaspora audience likely accessing on mobile:

- **Thumb-friendly**: CTAs and navigation in thumb zone
- **Collapsible context**: Previous messages collapse into summary
- **Voice input option**: Speak your story (especially for older users)
- **Offline drafts**: Continue writing even without connection
- **Generous tap targets**: 44x44px minimum for touch
- **Print/share/export**: Some users will want physical copies ([Source](https://matthewlarn.medium.com/designing-for-death-a-ux-guide-for-end-of-life-products-98983f885014))

---

## 2. Trust-Building Design Elements

### 2.1 Security Indicators

**Visual Cues That Build Trust** (based on fintech best practices):

| Element | Placement | Purpose |
|---------|-----------|---------|
| **SSL/HTTPS indicator** | Browser bar, onboarding | Standard web security |
| **"Bank-level encryption" badge** | Footer, sensitive forms | Reassurance |
| **SOC 2 / security audit badge** | About page, footer | Third-party validation |
| **Lock icon** | Next to input fields for sensitive data | Contextual security signal |
| **"Last saved" timestamp** | Above content areas | Data persistence confirmation |

**Research**: McAfee (79%), Verisign (76%), and PayPal (72%) rank as most recognized security badges. Higher brand recognition = more confidence. ([Source](https://eseospace.com/blog/trust-signals-in-fintech-security/))

### 2.2 Human Oversight Visibility

Critical for AI in sensitive contexts:

- **"Reviewed by [Licensed Professional]"** badge on generated documents
- **Clear AI disclosure**: "You're speaking with an AI companion. Human advisors review all legal documents."
- **Escalation path visible**: "Speak with a human" always available
- **Professional profiles**: Show credentials of human team members

**Design Pattern**:
```
[AI Chat Interface]
---
[Subtle footer bar]
AI-assisted | Human reviewed | Questions? Speak with an advisor →
```

### 2.3 Progress and Completion States

**Progress Visualization Options**:

1. **Journey Map**: Visual path showing completed milestones
   - "Family Overview" ✓
   - "Nigerian Assets" ○ (in progress)
   - "Canadian Assets" ○
   - "Digital Legacy" ○
   - "Cultural Wishes" ○

2. **Completion Percentage**: Simple progress bar with encouraging language
   - "45% complete - you're doing great"
   - Avoid pressure tactics - emphasize "at your own pace"

3. **Tree/Garden Metaphor**: Visual that "grows" as more is completed
   - Empty garden → seedlings → full trees
   - Resonates with "Sage" (plant) and "Willow" (tree) branding

**Anti-pattern warning**: "Grief kills attention span... Use one question per screen, clear next steps, and a soft, unobtrusive progress indicator. No pressure to finish." ([Source](https://matthewlarn.medium.com/designing-for-death-a-ux-guide-for-end-of-life-products-98983f885014))

### 2.4 Privacy Assurances

- **Data residency disclosure**: "Your data is stored in Canada"
- **PIPEDA compliance badge** (Canadian privacy law)
- **Granular privacy controls**: Per-section visibility settings
- **"Who can see this" indicator** on each section
- **Data deletion option**: Clear path to remove all data

---

## 3. Cultural Design Elements

### 3.1 Nigerian Visual Motifs (Subtle, Not Stereotypical)

**Guiding Principle**: Celebrate culture without caricature. Modern Nigerian-Canadian identity, not "tourist Africa."

**Recommended Elements**:

| Motif | Application | Subtlety Level |
|-------|-------------|----------------|
| **Adire indigo patterns** | Background textures, divider lines | High - abstract geometric |
| **Nsibidi-inspired icons** | Custom iconography for sections | Medium - stylized interpretations |
| **Ankara color accents** | Accent colors, hover states | Low - just colors, no patterns |
| **Kola nut illustration** | "Welcome" moments only | Medium - cultural significance |

**What to Avoid**:
- Tribal masks as decorative elements
- Safari/wildlife imagery
- Stereotypical "African" fonts
- Random kente/Ankara patterns everywhere

**Inspiration Artists**:
- Njideka Akunyili Crosby - Contemporary Nigerian-American artist who blends traditional motifs with modern contexts
- Laolu Senbanjo - Digital art that reinterprets Yoruba symbols

**Research Note**: "Indigo holds a special place in Yoruba culture, particularly in the creation of Adire textiles." Using these as subtle background patterns honors tradition without overwhelming modern UI. ([Source](https://evasonaike.com/blogs/evasonaikeblog/exploring-symbolism-colours-in-african-textiles-and-cultures))

### 3.2 Color Psychology for Legacy/Trust

**Recommended Primary Palette**:

| Color | Hex | Role | Psychology |
|-------|-----|------|------------|
| **Sage Green** | #9CAF88 | Primary brand | Growth, wisdom, calm, healing |
| **Willow Brown** | #8B7355 | Secondary, grounding | Earth, roots, stability, tradition |
| **Indigo Deep** | #2C3E50 | Accents, The Elder | Yoruba heritage, wisdom, depth |
| **Warm Cream** | #FAF9F6 | Background | Openness, clarity, warmth |
| **Soft White** | #FFFFFF | Cards, content areas | Clean, trustworthy |

**Accent Colors (Used Sparingly)**:

| Color | Hex | Role | Notes |
|-------|-----|------|-------|
| **Terra Cotta** | #E07A5F | CTA buttons, alerts | Energy, action (Nigerian earth) |
| **Gold/Champagne** | #D4AF37 | Success, premium elements | Value, legacy, achievement |

**Research Support**:
- "Sage green blends the restorative effects of green with a soft, neutral tone... especially effective in calming anxiety and promoting mental clarity." ([Source](https://www.imagine.art/blogs/sage-green))
- "Earth tones tap into our innate connection to nature and promote feelings of stability, reliability, and groundedness." ([Source](https://rosebenedictdesign.com/2025/01/31/earthy-color-palettes/))
- "Green symbolizes growth, wealth, and balance. Frequently used in financial applications to represent prosperity." ([Source](https://windmill.digital/psychology-of-color-in-financial-app-design/))

**Nigerian Color Symbolism to Consider**:
- Red = vitality, protection, but also danger - use cautiously
- White = purity, spirituality
- Green = growth, prosperity (also Nigerian flag)
- Indigo = Yoruba heritage, wisdom

### 3.3 Typography for Warmth + Professionalism

**Recommended Type Stack**:

| Role | Font | Why |
|------|------|-----|
| **Headings** | DM Serif Display | Warmth, sophistication, approachable authority |
| **Body** | Inter or DM Sans | Highly readable, modern, neutral |
| **Companion speech** | Slightly different weight/style | Differentiate AI voice from UI |

**Typography Guidelines**:
- Generous line height (1.6-1.8 for body text)
- Avoid all-caps except for buttons
- Use sentence case for headings (friendlier)
- Large base font (16-18px minimum on mobile)

### 3.4 Imagery Direction

**Do Use**:
- Nigerian-Canadian families (not stock African families)
- Urban Canadian settings with cultural elements (e.g., Nigerian restaurant, church gathering)
- Multi-generational family moments
- Warm, natural lighting
- Candid over posed

**Don't Use**:
- Generic "diverse family" stock photos
- Poverty imagery
- Rural African scenes (unless specifically relevant)
- Overly polished, corporate stock

**Illustration Style (Alternative to Photography)**:
- Warm, illustrated avatars for companions
- Soft, geometric patterns inspired by Adire
- Line art for icons (custom, not generic)

---

## 4. Landing Page Concepts

### 4.1 Hero Section Approaches

#### Concept A: The Conversation Opener

```
[Hero Section]
Background: Soft sage green gradient with subtle Adire pattern

Headline: "Your legacy deserves a conversation"

Subhead: "AI companions that understand both your Canadian
          life and Nigerian roots. Plan across borders,
          with wisdom and warmth."

[CTA] "Start the conversation" (terra cotta button)

[Secondary] "How it works" (text link)

[Visual]: Abstract illustration of two figures in conversation,
          blending modern and traditional elements
```

**Why it works**: Emphasizes the conversational, relational nature. "Conversation" feels less intimidating than "estate planning."

#### Concept B: The Companion Introduction

```
[Hero Section]
Background: Warm cream with floating companion avatars

Headline: "Meet your legacy planning team"

Subhead: "Five AI companions, each an expert in their domain.
          The Sage for wisdom. The Scribe for details.
          The Elder for tradition."

[CTA] "Meet the companions" (opens companion showcase)

[Visual]: Illustrated avatars of the five companions arranged
          in a gentle arc, each with their icon/symbol
```

**Why it works**: Leads with the unique differentiator (multiple specialized AI companions). Creates curiosity.

#### Concept C: The Bridge Metaphor

```
[Hero Section]
Background: Split visual - Canadian cityscape | Nigerian landscape
            connected by a subtle bridge/path

Headline: "Plan your legacy across borders"

Subhead: "Dual-jurisdiction expertise for Nigerian Canadians.
          From Lagos to Toronto, we help you protect
          what matters most."

[CTA] "Start your plan" (terra cotta button)

[Stats below hero]:
"70% of Nigerians die without wills"
"50% of Canadians are in the same position"
"We bridge both worlds."
```

**Why it works**: Immediately addresses the dual-jurisdiction value prop. Visual metaphor is clear and culturally relevant.

#### Recommended: Hybrid of A + C

Lead with conversation framing, supported by bridge imagery:

```
Headline: "Your legacy deserves a conversation"
Subhead: "AI companions that understand your Canadian
          life and Nigerian roots."
```

### 4.2 How to Introduce AI Companions

**Don't**: List all five companions immediately (overwhelming)

**Do**: Progressive disclosure

1. **Hero**: Mention "AI companions" generally
2. **Section 2**: Introduce The Sage as primary guide
3. **Section 3**: Show how specialists join (Elder, Scribe, etc.)
4. **Footer/About**: Full companion profiles

**Section Layout: "How It Works"**

```
[Section: How It Works]

Step 1: Start with The Sage
"Answer reflective questions about your values,
 wishes, and what matters most."
[Sage avatar + sample chat bubble]

Step 2: Bring in the specialists
"The Scribe organizes your assets. The Elder honors
 your cultural traditions. The Guardian ensures
 legal compliance across jurisdictions."
[Three smaller avatars in a row]

Step 3: Human review
"Licensed professionals review your plan before
 any documents are finalized."
[Icon: professional seal/checkmark]

Step 4: Ongoing support
"Update your plan anytime. Your companions
 remember your story."
[Icon: calendar with refresh symbol]
```

### 4.3 CTA Hierarchy

| CTA | Priority | Placement | Copy |
|-----|----------|-----------|------|
| **Primary** | 1 | Hero, sticky header, section ends | "Start the conversation" |
| **Secondary** | 2 | Below problem statement, mid-page | "Take our 3-minute survey" |
| **Tertiary** | 3 | Footer, after trust signals | "Questions? Speak with a human" |

**CTA Design**:
- Primary: Terra cotta (#E07A5F) button, rounded corners, subtle shadow
- Secondary: Outlined button in sage green
- Tertiary: Text link with arrow

### 4.4 Trust Signals on Landing Page

**Placement Strategy**:

1. **Pre-hero bar**: "Securely encrypted | Human reviewed | Based in Canada"
2. **After problem statement**: Statistics with sources
3. **Before CTA section**: "As featured in..." (if applicable) or "Trusted by X families"
4. **Footer**: Compliance badges, privacy policy link, security certifications

**Specific Trust Elements**:
- "Bank-level 256-bit encryption"
- "PIPEDA Compliant"
- "Documents reviewed by licensed professionals"
- "Your data never leaves Canada"
- Logos of any professional associations

---

## 5. Inspiration Sources

### 5.1 AI Companion Apps

| App | What to Learn | Link |
|-----|---------------|------|
| **Replika** | Warm aesthetic, avatar customization, bright colors that feel welcoming | [replika.ai](https://replika.ai/) |
| **Pi by Inflection** | Calm, reflective conversation design; minimal interface | [pi.ai](https://pi.ai/) |
| **Wysa** | Clinical validation + warmth; embedded CBT exercises in chat | [wysa.io](https://www.wysa.io/) |
| **Woebot** | Research-backed; clear AI disclosure; micro-interventions | [woebothealth.com](https://woebothealth.com/) |
| **Nomi** | Multi-character support, memory persistence, persona controls | [nomi.ai](https://nomi.ai/) |

**Key Takeaways**:
- Wysa shows how to embed structured tools (exercises) within a chat flow
- Pi demonstrates that less is more - minimal UI, focus on conversation
- Replika proves warm, colorful aesthetics work for emotional AI

### 5.2 Estate Planning Sites

| Site | What to Learn | Link |
|-----|---------------|------|
| **Trust & Will** | Modern, clean design; clear value props; product preview in hero | [trustandwill.com](https://trustandwill.com/) |
| **Fabric (now Gerber Life)** | "Design language focused on life" - avoiding death focus | [meetfabric.com](https://www.meetfabric.com/) |
| **Everplans** | Comprehensive approach; good information architecture | [everplans.com](https://www.everplans.com/) |
| **Tomorrow** | Mobile-first; friendly language | App stores |

**Key Takeaways**:
- Trust & Will's EstateOS positions AI as "intelligent platform" - similar positioning opportunity
- Fabric's approach of celebrating life over planning for death aligns with design principles
- Estate planning sites that convert well use "protection and preparedness" framing, not fear

### 5.3 Grief/Memorial Platforms

| Platform | What to Learn | Link |
|----------|---------------|------|
| **Ever Loved** | Flexible privacy controls; tribute pages with guestbooks | [everloved.com](https://www.everloved.com/) |
| **GatheringUs** | Virtual memorial services; beautiful, simple design | [gatheringus.com](https://www.gatheringus.com/) |
| **Eternos** | AI-based life story preservation | [eternos.life](https://eternos.life/) |
| **LegacyRemembered** (case study) | "Psychology of grief" in user journey design | [See Loudface case study](https://www.loudface.co/case-studies/legacyremembered-digital-memorial-platform) |

**Key Takeaways**:
- "Grief kills attention span" - one question per screen, no pressure
- Pre-filled templates reduce "blank page panic"
- Print/share/export options are essential for this audience

### 5.4 Cultural/Diaspora Digital Services

| Service | What to Learn | Link |
|---------|---------------|------|
| **Remitly** | Diaspora money transfer; trust-building for cross-border | [remitly.com](https://www.remitly.com/) |
| **WorldRemit** | Clean, mobile-first; cultural sensitivity | [worldremit.com](https://www.worldremit.com/) |
| **Cowrywise** (Nigeria)** | Nigerian fintech; modern design for Nigerian audience | [cowrywise.com](https://cowrywise.com/) |
| **Piggyvest** (Nigeria)** | Friendly, approachable Nigerian fintech | [piggyvest.com](https://www.piggyvest.com/) |

**Key Takeaways**:
- Nigerian fintechs like Cowrywise and Piggyvest prove that warm, modern design resonates with Nigerian audiences
- Diaspora money transfer apps have solved similar trust challenges (cross-border, sensitive data)
- Mobile-first is essential for this audience

### 5.5 Design System References

| Resource | What to Learn | Link |
|----------|---------------|------|
| **PatternFly AI Conversation Design** | Best practices for AI conversation UX | [patternfly.org](https://www.patternfly.org/patternfly-ai/conversation-design/) |
| **Mobbin** | Searchable screenshots of apps including Wysa | [mobbin.com](https://mobbin.com/) |
| **Lapa Ninja AI Collection** | 186+ AI landing page examples | [lapa.ninja/category/artificial-intelligence](https://www.lapa.ninja/category/artificial-intelligence/) |

---

## 6. Key Design Decisions Summary

### Recommended Approach

| Aspect | Decision | Rationale |
|--------|----------|-----------|
| **Interface model** | Hybrid chat + guided flows | Flexibility for emotional + practical content |
| **Multi-persona** | Primary companion (Sage) with specialists | Coherent narrative, prevents confusion |
| **Color palette** | Sage green + willow brown + indigo | Trust, growth, cultural nods, calm |
| **Typography** | DM Serif Display + Inter | Warm authority + high readability |
| **Imagery** | Illustrated companions, candid photography | Warmth without stock photo sterility |
| **Cultural elements** | Subtle Adire patterns, custom iconography | Authentic without stereotyping |
| **Hero approach** | "Conversation" framing with bridge metaphor | Inviting, addresses core value prop |
| **Trust signals** | Visible throughout, human review emphasized | Critical for AI in sensitive domain |

### Mobile Priorities

1. Thumb-friendly navigation
2. Voice input option
3. Offline capability
4. Generous tap targets
5. Collapsible context

### Accessibility Requirements

- WCAG 2.1 AA compliance minimum
- High contrast mode option
- Screen reader optimization
- Reduced motion option
- Print-friendly views

---

## 7. Next Steps

1. **Wireframes**: Low-fidelity mockups of key screens
   - Landing page
   - Companion chat interface
   - Specialist transition flow
   - Progress dashboard

2. **Companion Visual Design**: Avatar concepts for all five companions
   - Illustrated, not photorealistic
   - Cultural elements without stereotypes
   - Distinct but cohesive style

3. **Prototype**: Interactive prototype of onboarding + first Sage conversation

4. **User Testing**: Validate concepts with target audience
   - Nigerian-Canadian focus groups
   - Sensitivity around death/legacy topics
   - Mobile usability testing

---

## Sources

**AI Companion Design**:
- [9 Best AI Companion Apps in 2025](https://www.cyberlink.com/blog/trending-topics/3932/ai-companion-app)
- [10 Best Emotional Companion AI Apps for 2025](https://jenaichat.com/blog/emotional-companion-ai/)
- [UX Case Study: AI for Emotional Support](https://medium.com/design-bootcamp/sam-altman-said-dont-make-chatgpt-your-therapist-so-i-designed-mindbubble-an-ux-case-study-a5fb7cf258d5)

**Conversational AI UX**:
- [Design Patterns for AI Interfaces - Smashing Magazine](https://www.smashingmagazine.com/2025/07/design-patterns-ai-interfaces/)
- [UX for AI Chatbots: Complete Guide 2025](https://www.parallelhq.com/blog/ux-ai-chatbots)
- [Conversational AI Assistant Design: 7 UX/UI Best Practices](https://www.willowtreeapps.com/insights/willowtrees-7-ux-ui-rules-for-designing-a-conversational-ai-assistant)

**Estate Planning Design**:
- [Best Estate Planning Websites 2025](https://growlaw.co/blog/best-estate-planning-websites)
- [Trust & Will Unveils EstateOS](https://www.prnewswire.com/news-releases/trust--will-unveils-estateos-the-first-intelligent-platform-for-modern-legacy-planning--and-announces-inaugural-generations-conference-302488924.html)
- [Fabric Wills Review](https://www.joincake.com/blog/fabric-wills-review/)

**Grief/Memorial UX**:
- [Designing for Death: A UX Guide](https://matthewlarn.medium.com/designing-for-death-a-ux-guide-for-end-of-life-products-98983f885014)
- [Digital Legacy Design Project](https://www.masterdigitaldesign.com/case/digital-legacy)
- [LegacyRemembered Case Study](https://www.loudface.co/case-studies/legacyremembered-digital-memorial-platform)

**Nigerian/African Design**:
- [Symbolism in African Textiles and Cultures](https://evasonaike.com/blogs/evasonaikeblog/exploring-symbolism-colours-in-african-textiles-and-cultures)
- [Colors in Nigerian Art](https://naijaartprints.com/colors-in-nigerian-art/)
- [Nigerian UI/UX Designers](https://www.acumen.com.ng/2017/06/20/for-nigerian-ux-designers-you-should-know-follow/)

**Trust & Security Design**:
- [Trust Signals in Fintech](https://eseospace.com/blog/trust-signals-in-fintech-security/)
- [Fintech UX Design Patterns for Trust](https://phenomenonstudio.com/article/fintech-ux-design-patterns-that-build-trust-and-credibility/)
- [Fintech Design Guide](https://www.eleken.co/blog-posts/modern-fintech-design-guide)

**Color Psychology**:
- [Psychology of Color in Financial App Design](https://windmill.digital/psychology-of-color-in-financial-app-design/)
- [Sage Green - Color Details](https://www.imagine.art/blogs/sage-green)
- [Earthy Color Palettes for Branding](https://rosebenedictdesign.com/2025/01/31/earthy-color-palettes/)

**Landing Page & Hero Design**:
- [30 Hero Section Examples](https://www.marketermilk.com/blog/hero-section-examples)
- [AI Startup Landing Page Examples](https://www.ebaqdesign.com/blog/ai-startup-landing-page-examples)
- [Best Landing Page Examples 2025](https://landing-page.io/blog/best-landing-page-examples)
