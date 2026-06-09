---
title: "That's a wrap"
week: 12
date: 2026-04-14
author: Natasha Png
summary: "A final reflection on SEAblings: Lighthouse results, user testing insights, what shipped for MVP, and what I learned building a full stack web app from scratch."
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

That's a wrap for the semester! This unit was a roller coaster and I'm glad that it is over... JK! I genuinely enjoyed this unit and being able to work in a collaborative team. Now let's look back and reflect.

## Performance Evaluation

To evaluate the application, we ran a Lighthouse audit on the local development server. The results returned a Performance score of 91, Accessibility 87, SEO 91, and Best Practices 70.

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

The Best Practices score was mainly affected by the lack of HTTPS. Since the audit was run locally rather than on a deployed production environment, this was expected. Lighthouse also flagged missing Content Security Policy and HSTS headers, which would normally be configured at the hosting layer. With more time, adding a basic CSP would improve security.

The remaining console error came from a Chrome extension rather than our application, so it can be ignored. Overall, the lower Best Practices score reflects missing production infrastructure rather than issues with the application itself.

![Lighthouse best practices audit](assets/reflection/lighthouse-bestpractices.png)

### Strengths

The application performed particularly well in responsiveness and visual stability. Total Blocking Time was 0 ms, meaning user interactions were never delayed, and Cumulative Layout Shift was also 0, preventing unexpected movement during rendering.

The Accessibility score of 87 reflects the effort we put into semantic HTML, heading hierarchy, form labels, and touch target sizes. While it falls just below the green threshold, it provides a clear target for future improvements.

### Weaknesses

The biggest performance issue was the Largest Contentful Paint of 1.9 seconds. Although the First Contentful Paint was strong at 0.8 seconds, the delay suggests a large element was loading later than ideal. Google Fonts and our main stylesheet contributed to this.

Lighthouse also identified accessibility issues with some ARIA attributes and font sizes. These problems were fixable, but we only discovered them near the end of the semester when there was little time left to address them.

![Lighthouse accessibility audit](assets/reflection/lighthouse-accesibility.png)

Another issue was our CSS architecture. Because we used a single stylesheet for the whole application, Lighthouse estimated that most of the file was unused on any given page. Cache headers were also absent, meaning returning users would re-download assets every visit.

### What I Would Improve

The biggest improvement would be addressing render-blocking fonts through `font-display: swap` or self-hosting. I would also minify the CSS, split styles by page, and configure caching for static assets.

More broadly, I would run Lighthouse earlier in the development process rather than treating it as a final step. Discovering accessibility issues earlier would have given us time to act on them.

## User Experience

We conducted two usability tests with Southeast Asian users who cook.

<div class="photo-row">
  <img src="assets/reflection/usertesting-01.JPG" alt="User testing session 1">
  <img src="assets/reflection/usertesting-02.JPG" alt="User testing session 2">
</div>

Both participants completed all tasks successfully, including browsing the feed, posting a recipe, and using the ingredient map.

P1, a design student, highlighted issues with CTA hierarchy, icon-heavy buttons, and confusion around the "Post a Tip" feature. Despite this, they validated our core concept with the comment:

> "A lot of the times the SE Asian recipes are usually shared within families so having a small dedicated community would help a lot."

P1 rated the app 3/5.

![CTA hierarchy issue flagged during user testing](assets/reflection/CTA-hierachy.png)

P2 rated it 5/5 and experienced no confusion, although they were significantly more tech-savvy than our intended audience.

### Actions Taken

Following testing, we prioritised fixes around the remaining MVP work.

The icon-led buttons were made more descriptive, and the "Post a Tip" feature was removed entirely. Since it was only a stretch goal, removing it eliminated the confusing navigation.

![The post a tip button that was removed](assets/reflection/postatip.png)

The Festive Collections page was also scoped out of the MVP. Although designed, it was never connected to real data and remains part of the backlog for future development.

![Festive collections page design](assets/reflection/festival-page.png)

The repeated CTAs were intentionally left unchanged. Since both buttons lead to the same page, we felt the issue may have been influenced by the small sample size rather than being a fundamental design flaw.

## Functional Requirements

All four planned MVP features were delivered:

* Recipe feed
* Recipe posting
* Ingredient finder map
* User profiles

Responsibilities were divided across the team. I worked on recipe posting, Patricia handled the map, and Amorino led user profiles and the feed, with all of us contributing to the feed itself.

Although all features met the functional requirements, many of them are functional rather than polished. As designers, we know they could provide a much better experience.

The recipe posting form is a good example. Everything works correctly, but it currently exists as a single-page form. Ideally, I would redesign it into a more guided, step-by-step experience that feels more engaging for creators. However, that level of polish had to be sacrificed to deliver the MVP.

Because full stack development was new to all of us, much of our time went into understanding the backend and connecting everything together. As a result, UI improvements became secondary.

This was especially noticeable with the ingredient map. Much of Patricia's time was spent simply getting the functionality working, and the map currently relies on dummy data because it is designed to grow with community contributions.

While building the recipe form, I also realised that Leaflet lacked many Asian grocery locations. My solution was to let users manually pin stores and enter names themselves. In the future, we would likely explore Google Maps for more comprehensive location data.

We also discovered edge cases we had not considered initially, such as what happens when an ingredient has no community entries yet. These issues only became visible once we started using the app ourselves.

## Lessons Learned

The biggest lesson I learned was how quickly you have to adapt when building full stack applications. Because the unit was largely self-directed, we had to plan, scope, and learn simultaneously. In many ways, it genuinely felt like a real-world project.

Looking back, I think our concept started too small. We intentionally kept it broad so we could stay realistic, but I now think it would have been better to start more ambitiously and cut features later. Because we began with the minimum, we largely stayed there.

On the other hand, I am genuinely proud of how we worked as a team. GitHub Projects was new to all of us, but it ended up becoming one of my favourite workflows. It made task management clear and helped us communicate effectively throughout the semester.

Big up Amo and Pat.

SEAblings ended up looking different from what I originally imagined. Amorino's visual identity gave the entire web app a strong sense of personality, especially with branding inspired by one of his favourite Thai dishes.

If I could strengthen one aspect, it would be the interactivity. That ultimately comes back to planning, and it is something I will think about much more in future projects.

DECO2017 has genuinely been one of the most rewarding units I have taken. Who would have thought three designers could build a full stack web app in a semester?

There was a lot of learning and a lot of prompting (haha), but the skills I picked up feel genuinely useful.

This is the last selective I will take at USYD, and I am glad I chose this one.

I am excited to see where we can take SEAblings over the break, especially since I will not be back in Malaysia until December and will definitely be missing the food.

We will be the first ones posting recipes on there. :D

<div class="polaroid-wrap">
  <figure class="polaroid">
    <img src="assets/reflection/teamphoto.JPG" alt="SEAblings team in class">
    <figcaption class="polaroid-caption">SEAblings in class</figcaption>
  </figure>
</div>
