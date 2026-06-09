---
title: "That's a wrap"
week: 12
date: 2026-04-14
author: Natasha Png
summary: "A final reflection on SEAblings: Lighthouse performance results, user testing insights, what shipped for MVP, and what I learned building a full stack web app from scratch."
tags:
  - reflection
  - performance
  - lighthouse
  - user testing
  - SEAblings
---

<style>
/* ── Lighthouse score component ── */
.lh-panel {
  margin: 1.5rem 0;
  padding: 1.25rem 1.5rem;
  background: var(--hover-bg);
  border-radius: 0.5rem;
  border: 1px solid var(--border);
}

.lh-scores {
  display: flex;
  gap: 1.25rem;
  flex-wrap: wrap;
  justify-content: center;
  margin-bottom: 1.25rem;
}

.lh-score-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.45rem;
}

.lh-label {
  font-size: 0.75rem;
  color: var(--muted);
  text-align: center;
  font-weight: 500;
}

.lh-vitals {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  border-top: 1px solid var(--border);
  padding-top: 1rem;
}

.lh-vital {
  flex: 1;
  min-width: 90px;
  background: var(--bg);
  border: 1px solid var(--border);
  border-radius: 0.4rem;
  padding: 0.55rem 0.75rem;
  text-align: center;
}

.lh-vital.lh-highlight {
  border-color: rgba(12, 206, 107, 0.4);
  background: rgba(12, 206, 107, 0.07);
}

.lh-vital-name {
  font-size: 0.68rem;
  color: var(--muted);
  text-transform: uppercase;
  letter-spacing: 0.04em;
  margin-bottom: 0.2rem;
}

.lh-vital-value {
  font-size: 1rem;
  font-weight: 700;
}

.lh-green  { color: #0cce6b; }
.lh-orange { color: #ffa400; }
.lh-red    { color: #ff4e42; }

/* ── Side-by-side photo row ── */
.photo-row {
  display: flex;
  gap: 0.75rem;
  margin: 1.25rem 0;
}

.photo-row img {
  flex: 1;
  min-width: 0;
  max-height: 300px;
  object-fit: cover;
  border-radius: 0.4rem;
  margin: 0;
}

/* ── Polaroid photo ── */
.polaroid-wrap {
  display: flex;
  justify-content: center;
  margin: 2rem 0;
}

.polaroid {
  background: #fff;
  padding: 0.75rem 0.75rem 3rem;
  box-shadow: 0 4px 18px rgba(0, 0, 0, 0.22), 0 1px 4px rgba(0, 0, 0, 0.1);
  transform: rotate(-1.5deg);
  max-width: 420px;
  width: 100%;
}

.polaroid img {
  display: block;
  width: 100%;
  margin: 0;
  border-radius: 0;
}

.polaroid-caption {
  text-align: center;
  font-size: 0.95rem;
  color: #37352f;
  margin-top: 0.6rem;
  font-style: italic;
  font-weight: 500;
}
</style>

That's a wrap for the semester! This unit was a roller coaster and I'm glad that it is over... JK! I really enjoyed this unit and being able to work in a collaborative team. Now let's look back and reflect.

## Performance

### Performance Evaluation

To evaluate the application's performance, we ran a Lighthouse audit on the local development server. The results returned a Performance score of 91, with supporting scores of 87 for Accessibility, 91 for SEO, and 70 for Best Practices.

<div class="lh-panel">
  <div class="lh-scores">
    <div class="lh-score-card">
      <svg viewBox="0 0 100 100" width="88" height="88" aria-label="Performance score 91">
        <circle cx="50" cy="50" r="45" fill="none" stroke="var(--border)" stroke-width="8"/>
        <circle cx="50" cy="50" r="45" fill="none" stroke="#0cce6b" stroke-width="8"
          stroke-dasharray="282.74" stroke-dashoffset="25.45"
          transform="rotate(-90 50 50)" stroke-linecap="round"/>
        <text x="50" y="50" text-anchor="middle" dominant-baseline="central"
          font-size="22" font-weight="700" fill="#0cce6b" font-family="ui-sans-serif, system-ui, sans-serif">91</text>
      </svg>
      <span class="lh-label">Performance</span>
    </div>
    <div class="lh-score-card">
      <svg viewBox="0 0 100 100" width="88" height="88" aria-label="Accessibility score 87">
        <circle cx="50" cy="50" r="45" fill="none" stroke="var(--border)" stroke-width="8"/>
        <circle cx="50" cy="50" r="45" fill="none" stroke="#ffa400" stroke-width="8"
          stroke-dasharray="282.74" stroke-dashoffset="36.76"
          transform="rotate(-90 50 50)" stroke-linecap="round"/>
        <text x="50" y="50" text-anchor="middle" dominant-baseline="central"
          font-size="22" font-weight="700" fill="#ffa400" font-family="ui-sans-serif, system-ui, sans-serif">87</text>
      </svg>
      <span class="lh-label">Accessibility</span>
    </div>
    <div class="lh-score-card">
      <svg viewBox="0 0 100 100" width="88" height="88" aria-label="SEO score 91">
        <circle cx="50" cy="50" r="45" fill="none" stroke="var(--border)" stroke-width="8"/>
        <circle cx="50" cy="50" r="45" fill="none" stroke="#0cce6b" stroke-width="8"
          stroke-dasharray="282.74" stroke-dashoffset="25.45"
          transform="rotate(-90 50 50)" stroke-linecap="round"/>
        <text x="50" y="50" text-anchor="middle" dominant-baseline="central"
          font-size="22" font-weight="700" fill="#0cce6b" font-family="ui-sans-serif, system-ui, sans-serif">91</text>
      </svg>
      <span class="lh-label">SEO</span>
    </div>
    <div class="lh-score-card">
      <svg viewBox="0 0 100 100" width="88" height="88" aria-label="Best Practices score 70">
        <circle cx="50" cy="50" r="45" fill="none" stroke="var(--border)" stroke-width="8"/>
        <circle cx="50" cy="50" r="45" fill="none" stroke="#ffa400" stroke-width="8"
          stroke-dasharray="282.74" stroke-dashoffset="84.82"
          transform="rotate(-90 50 50)" stroke-linecap="round"/>
        <text x="50" y="50" text-anchor="middle" dominant-baseline="central"
          font-size="22" font-weight="700" fill="#ffa400" font-family="ui-sans-serif, system-ui, sans-serif">70</text>
      </svg>
      <span class="lh-label">Best Practices</span>
    </div>
  </div>
  <div class="lh-vitals">
    <div class="lh-vital lh-highlight">
      <div class="lh-vital-name">First Contentful Paint</div>
      <div class="lh-vital-value lh-green">0.8 s</div>
    </div>
    <div class="lh-vital">
      <div class="lh-vital-name">Largest Contentful Paint</div>
      <div class="lh-vital-value lh-orange">1.9 s</div>
    </div>
    <div class="lh-vital lh-highlight">
      <div class="lh-vital-name">Total Blocking Time</div>
      <div class="lh-vital-value lh-green">0 ms</div>
    </div>
    <div class="lh-vital lh-highlight">
      <div class="lh-vital-name">Cumulative Layout Shift</div>
      <div class="lh-vital-value lh-green">0</div>
    </div>
  </div>
</div>

![Lighthouse performance audit](assets/reflection/lighthouse-performance.png)

### Best Practices (70)

The Best Practices score of 70 was primarily dragged down by the absence of HTTPS, which Lighthouse flagged across all five requests made during the audit. Since the application was tested against a local development server (`http://0.0.0.0:3000`) rather than a deployed production environment, HTTPS was not configured, which is expected and intentional at this stage of the project. A production deployment would resolve this automatically, as platforms like Render, Fly.io, or Vercel provision TLS certificates by default.

The audit also flagged the absence of a Content Security Policy (CSP) and HSTS header. These are HTTP response headers that would typically be configured at the server or hosting layer in production to mitigate XSS and protocol downgrade attacks. With more time, adding a CSP header to the MojoJS application, even a basic one restricting script sources, would address this and meaningfully harden the app against cross-site scripting.

The remaining console error (`crypto.randomUUID is not a function`) was traced to a Chrome browser extension injected during testing, not the application itself, and can be disregarded.

In summary, the Best Practices score reflects the absence of production infrastructure rather than flaws in the application code, and would improve significantly upon deployment.

![Lighthouse best practices audit](assets/reflection/lighthouse-bestpractices.png)

### Strengths

The application performed particularly well on interactivity and visual stability. Total Blocking Time (TBT) came in at 0 ms, meaning the main thread was never blocked long enough to delay user input, so the app feels immediately responsive once it loads. Cumulative Layout Shift (CLS) was also 0, indicating no unexpected visual movement as the page renders, which contributes to a smooth user experience.

The accessibility score of 87 reflects deliberate attention to semantic HTML throughout development. ARIA labels, proper heading hierarchy, form labels, and sufficient touch target sizes all contributed. It sits just below the green threshold of 90, which gives a clear target for improvement in a follow-up pass.

### Weaknesses

The main performance bottleneck is the Largest Contentful Paint (LCP) of 1.9 seconds, which Lighthouse flagged as needing improvement. The First Contentful Paint (FCP) was strong at 0.8 seconds, but the gap between FCP and LCP suggests a large element (likely a hero image or above-the-fold card) is loading late. The main stylesheet `hub.css` and Google Fonts (DynaPuff) both sit in the critical render path and contribute to this delay.

The accessibility score of 87 is amber and the issues behind it are fixable. Some of the ARIA attributes we added are not actually read correctly by screen readers. Applying `aria-label` to non-interactive elements or using roles incorrectly means assistive technology either ignores them or reads them in a confusing order. Font sizes are also a recurring issue, with several labels and secondary text elements falling below the recommended minimum, making the interface harder to use for people with low vision. Both are things we would have caught and fixed if we had run the audit earlier in the build rather than at the end.

![Lighthouse accessibility audit](assets/reflection/lighthouse-accesibility.png)

Lighthouse also flagged that `hub.css` (43 KB) carries an estimated 39 KB of unused CSS on any given page. This is a direct consequence of the single-file CSS architecture used throughout the project, where all styles across all pages are loaded upfront regardless of which page the user is on. Similarly, `hub.css` has no cache headers set, meaning repeat visitors re-download the full stylesheet every visit.

### What I would improve with more time

The highest-impact change would be addressing the Google Fonts render-blocking issue, either by adding `font-display: swap` to allow text to render before the custom font loads, or by self-hosting the font files to eliminate the external network dependency entirely.

For the CSS, I would introduce a build step to minify the stylesheet (estimated saving of 12 KB) and consider splitting it into page-specific bundles or using a tool like PurgeCSS to remove unused rules per route. Setting appropriate `Cache-Control` headers on static assets like `hub.css` and `htmx.min.js` would also meaningfully improve load times for returning users.

It is worth noting that the audit was run on the `/login` redirect rather than the intended authenticated page, since Lighthouse cannot log in automatically. Running it against authenticated routes would give a more complete picture of performance under real usage conditions.

More broadly, running the Lighthouse audit earlier in the semester, mid-build rather than at the end, would have given us time to actually act on the accessibility findings. The ARIA and font size issues are not difficult to fix, but finding them on the last week meant there was no capacity left to address them. Making Lighthouse a regular checkpoint, rather than a final step, is something I would do differently next time.

## User Experience

To improve on the user experience, we ran two user testing sessions. We deliberately chose Southeast Asians who cook to help us with this testing.

<div class="photo-row">
  <img src="assets/reflection/usertesting-01.JPG" alt="User testing session 1">
  <img src="assets/reflection/usertesting-02.JPG" alt="User testing session 2">
</div>

**Tasks:**

- Browsing the feed
- Posting a recipe
- Finding an ingredient on the map

### Test insights

Both participants were able to complete all tasks. P1, a design student, flagged three interface issues: CTA hierarchy confusion, an icon-heavy layout that made action buttons hard to distinguish, and an unexpected destination when clicking "post a tip", which led to the recipe posting form rather than a tips page. Despite this, P1 offered a quote that directly validated our core concept: "A lot of the times the SE Asian recipes are usually shared within families so having a small dedicated community would help a lot." P1 rated the app 3/5.

![CTA hierarchy issue flagged during user testing](assets/reflection/CTA-hierachy.png)

P2 rated it 5/5 and navigated without any visible confusion. However, P2 was notably more tech-savvy than our target audience, which limits how much weight this score carries. It likely reflects their prior experience with web applications rather than the design's clarity for a general user.

### Actions taken

Changes were made following the usability test, though we had to prioritise them around remaining MVP features that still needed to be implemented first. Once those were in place, I evaluated the feedback and addressed it in order of impact.

The icon-led buttons were updated to be more descriptive, resolving the issue of actions being hard to distinguish at a glance. The "post a tip" button was removed entirely. That feature (a community tips and tricks page) was a stretch goal rather than an MVP requirement, and removing it eliminated the confusing misdirection to the recipe form. It can be reintroduced in a later stage when the full tips flow is built out as our future steps.

![The post a tip button that was removed](assets/reflection/postatip.png)

The festive collections page was another feature we scoped out of the MVP. The concept was to group recipes by seasonal occasions, giving the community a reason to return around specific cultural events. It was designed but never wired up to real data in time, so it lives in the backlog for a future iteration.

![Festive collections page design](assets/reflection/festival-page.png)

The repeated CTAs ("Share yours" and "Post recipe") were a lower priority. Both links correctly lead to the same page, and the duplication is intentional: the feed is designed to act as a home page that surfaces all key actions in context. In hindsight, the confusion here was likely a limitation of having only one participant who gave critical feedback; with a larger test group, this pattern would more likely have read as expected for a dashboard-style layout rather than as a design flaw.

## Functional Requirements

All 4 main features we wanted for the MVP were shipped: recipe feed, recipe posting, ingredient finder map, and user profiles. We split responsibility across the 4 features. I was in charge of recipe posting, Patricia handled the map, and Amorino led the user profiles and the feed (with all of us contributing to the feed). All features met the functional requirements, but only to an extent. Even though this was more of a development-focused unit, we are still designers, and for most of the features the result is functional but nowhere near as user-friendly as we would want it to be.

A good example is the recipe posting form I was in charge of. The form works functionally in that everything links to the right destination and database, but there is so much more potential to it. I would consider it one of the most important features in the app, and right now it is just a single page form which does not feel very welcoming. What I imagine for the future is a walkthrough-style, step-by-step process that makes posting feel more engaging for content creators rather than tedious. That was a want though, and it had to be cut to the bare minimum for the MVP given our capacity.

A lot of our time was spent getting the backend working and wiring everything together, which meant the front end had to wait. Since the backend side was new to all of us, it left less time to polish the UI. This shows most clearly in the map, which Patricia was in charge of. Most of the time was spent just getting the map functional, and even then the database is limited because it is meant to grow as the community contributes to it. Right now it only works with dummy data. When I was building the recipe posting form that connects to the map, I noticed that Leaflet does not have a lot of Asian grocery stores in its data. The solution I landed on was to let users pin the store location themselves on the map and enter the name manually so they can navigate back to it later. Moving forward, we would look into using something like Google Maps which has more comprehensive location data, so users can pin places more accurately.

We also specified that users could find ingredient locations, but we never defined what the experience should look like when no community entries exist yet for a given ingredient. That edge case only became visible once we were actually using the app.

## Lessons Learned

The biggest thing I learned was how fast you have to move and adapt when developing full stack. A lot of this unit was self-paced, which meant a lot of the planning and responsibility fell on us, and we had to learn things while we were still scoping the project. It genuinely mimicked a real-world setting in that way.

One clear flaw looking back is that we did not define the concept with enough detail at the start. Our initial concept was very vague, and part of that was intentional so we could iterate based on what was actually feasible to build. But I think we could have been a lot more ambitious upfront and then cut from there. Because we started with a bare minimum concept, we just stayed there. If we had aimed higher from the beginning, I think we could have pushed the project a lot further.

On the other hand, I am genuinely proud of how we worked as a team. We held up really well and collaborated smoothly using GitHub Projects, which was a first for all of us and honestly a workflow I really enjoyed. It made it easy to assign tasks and see where everyone was at. Our team was great at communicating, which made everything a lot easier. Big up Amo and Pat.

SEAblings came out differently to what I expected initially. The visual identity Amorino developed made the whole webapp feel considered and put together, which was a real strength given that the branding was inspired by one of his favourite Thai dishes. What I think could have been stronger was the interactivity side of things, and that comes down to planning. That is something I will think about a lot more if I build something like this again.

DECO2017 was genuinely one of the most rewarding units I have taken in terms of learning. Who would have thought three designers could build a full stack webapp in a semester? It involved a lot of learning, and a lot of prompting (haha), but the skills I picked up feel relevant in a real way. This is the last selective I will take at USYD and I am glad I chose this one. I am keen to see where we can take SEAblings over the break, especially since I will not be back in Malaysia until December and will be missing the food. We will be the first ones to post recipes on there! :D

<div class="polaroid-wrap">
  <figure class="polaroid">
    <img src="assets/reflection/teamphoto.JPG" alt="SEAblings team in class">
    <figcaption class="polaroid-caption">SEAblings in class</figcaption>
  </figure>
</div>
