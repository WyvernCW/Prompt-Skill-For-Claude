# Examples: Generated Prompts

## Example 1: Dashboard Prompt (L2, full caveman)

**Role**: Senior frontend architect. 10yr React/TypeScript. Accessibility-first.

**Task**: Build analytics dashboard for e-commerce. Real-time sales metrics. No backend code.

**Input**: Sales data stream (WebSocket), user role (admin/viewer), date range.

**Process**: 
1. Auth check → role-based view.
2. Connect WebSocket → normalize data.
3. Render charts (line for trends, bar for categories, pie for share).
4. Auto-refresh every 30s. Manual refresh button.
5. Export CSV on demand.

**Build-Test-Validate**:
- Build: All components, hooks, types, utils. No stubs.
- Test: Type-check. Lint. Render test. WebSocket mock. CSV download verify.
- Validate: Cross-browser. Screen reader. Keyboard nav. Performance <100ms render.

**Constraints**: React 18+. TypeScript strict. Tailwind CSS. Recharts. No external state lib. WCAG 2.1 AA.

**Output**: Single file App.tsx. Modular sub-components. Type definitions inline. Hook for WebSocket. Hook for export.

**Tone**: Brutal minimal. Clean lines. Maximum data density. Whitespace as separator. Monospace numbers.

**Frontend Design**:
- Typography: JetBrains Mono for data, Playfair Display for headers. NO Inter.
- Color: Near-black background (#0a0a0a), electric cyan (#00f0ff) for active states, warm white (#faf8f5) for text.
- Motion: Staggered grid reveal on load. Numbers count up on data change. Subtle pulse on live indicator.
- Spatial: Asymmetric grid. Charts bleed to edge. Navigation floats as overlay.
- Background: Subtle dot grid pattern at 3% opacity. No solid colors.
- NO AI slop: No purple gradients. No rounded cards. No generic shadows.

**Level**: L2

---

## Example 2: Image Generator Prompt (L3, ultra caveman)

**Role**: Art director. Concept art for games. 15yr industry.

**Task**: Generate prompt for AI image gen. Post-apocalyptic cityscape.

**Input**: Mood (hopeful despair), time (golden hour), focal point (lone tree on skyscraper).

**Process**: 
1. Establish atmosphere → lighting → color palette.
2. Define composition rule (rule of thirds, tree at intersection).
3. Detail foreground (overgrown street), midground (ruined buildings), background (distant mountains).
4. Specify style (photorealistic with painterly touches).
5. Add technical params (8k, unreal engine, octane render).

**Constraints**: No humans. No text. No logos. Aspect 16:9. SFW.

**Output**: Single paragraph. Sensory-rich. Technical specs at end. No bullet points.

**Tone**: Solarpunk decay. Nature reclaiming concrete. Warm light on cold ruins.

**Level**: L3

---

## Example 3: API Design Prompt (L4, wenyan-full)

**Role**: Staff engineer. Distributed systems. GraphQL + gRPC.

**Task**: Design user service API. CRUD + search + bulk ops.

**Input**: User schema (id, email, name, role, createdAt, updatedAt).

**Process**: 
1. Define mutations (create, update, delete, bulkDelete).
2. Define queries (getById, search, list, count).
3. Add pagination (cursor-based).
4. Add filtering (role, dateRange, searchText).
5. Add sorting (multi-field).
6. Define error schema (code, message, field, retryable).

**Build-Test-Validate**:
- Build: Schema, resolvers, types, validation rules.
- Test: Query complexity analysis. N+1 detection. Rate limit check.
- Validate: Backward compatibility. Deprecation strategy. Documentation completeness.

**Constraints**: GraphQL spec. Max depth 5. Max complexity 1000. Rate limit 100req/min. GDPR compliant.

**Output**: Schema definition. Resolver signatures. Validation rules. Error catalog. Rate limit config.

**Tone**: Industrial/utilitarian. No decoration. Every field has purpose.

**Level**: L4

---

## Example 4: Landing Page Prompt (L2, full caveman, frontend-heavy)

**Role**: Creative technologist. 8yr frontend. WebGL, GSAP, bespoke interactions.

**Task**: Build landing page for artisan coffee subscription. Convert visitors to subscribers.

**Input**: Product photos, roast profiles, pricing tiers, testimonials.

**Process**:
1. Hero: Full-bleed video background. Custom cursor. Scroll-triggered text reveal.
2. Story: Horizontal scroll section. Parallax product shots.
3. Roasts: Interactive flavor wheel. Hover expands detail.
4. Pricing: Asymmetric cards. One pops with animation.
5. Footer: Newsletter. Social proof ticker.

**Build-Test-Validate**:
- Build: All sections, components, animations, assets. No stubs.
- Test: Lighthouse 95+. Animation 60fps. Mobile responsive. Reduced motion support.
- Validate: Conversion tracking. Accessibility audit. Performance budget <2MB.

**Constraints**: Next.js 14. Tailwind. GSAP. No component libraries. WCAG 2.1 AA.

**Output**: Page structure. Component hierarchy. Animation specs. Asset requirements.

**Tone**: Dark academia meets industrial. Warm amber lighting. Exposed brick textures. Copper accents. Leather and wood.

**Frontend Design**:
- Typography: Cormorant Garamond for display, Source Serif 4 for body. NO Inter.
- Color: Deep espresso (#1a1208), warm amber (#d4a574), cream (#f5f0e8). NO purple.
- Motion: Coffee steam particle system. Parallax on scroll. Magnetic buttons.
- Spatial: Overlapping sections. Diagonal dividers. Asymmetric grids.
- Background: Subtle paper texture overlay. Warm vignette on edges.
- NO AI slop: No generic card layout. No fade-in-on-scroll. No rounded buttons.

**Level**: L2
