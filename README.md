<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Module 17 - Journals & Planners | The Creator Plug Academy</title>
  <style>
    :root {
      --ink: #24192f;
      --muted: #6f6178;
      --panel: #ffffff;
      --gold: #d9a441;
      --gold-soft: #fff2c9;
      --rose: #f05d8a;
      --teal: #18a6a7;
      --violet: #4d2770;
      --violet-deep: #241332;
      --line: #eadfce;
      --shadow: 0 18px 40px rgba(48, 31, 61, 0.14);
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      color: var(--ink);
      background:
        radial-gradient(circle at 14% 8%, rgba(240, 93, 138, 0.15), transparent 28%),
        radial-gradient(circle at 88% 4%, rgba(24, 166, 167, 0.16), transparent 26%),
        linear-gradient(180deg, #fffaf1 0%, #f8f1e7 45%, #f4ebdd 100%);
      line-height: 1.6;
    }
    a { color: #2c6f91; font-weight: 800; }
    .page { width: min(1120px, calc(100% - 32px)); margin: 0 auto; padding: 28px 0 56px; }
    .hero {
      background: linear-gradient(135deg, rgba(36, 19, 50, 0.96), rgba(77, 39, 112, 0.92));
      color: #fff;
      border-radius: 8px;
      padding: 34px;
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
    }
    .hero:after {
      content: "";
      position: absolute;
      right: -78px;
      top: -82px;
      width: 260px;
      height: 260px;
      border: 2px solid rgba(217, 164, 65, 0.36);
      transform: rotate(20deg);
    }
    .eyebrow {
      display: inline-flex;
      background: rgba(217, 164, 65, 0.18);
      border: 1px solid rgba(217, 164, 65, 0.45);
      color: #ffe3a0;
      border-radius: 8px;
      padding: 7px 11px;
      font-size: 13px;
      font-weight: 800;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }
    h1, h2, h3 { line-height: 1.15; margin: 0; }
    h1 { max-width: 880px; margin-top: 18px; font-size: clamp(34px, 6vw, 70px); }
    .subtitle { max-width: 860px; margin: 18px 0 0; color: #f6e9d6; font-size: 18px; }
    .quick-links { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 24px; position: relative; z-index: 1; }
    .quick-links a, .button-link, .copy-button {
      appearance: none;
      border: 0;
      border-radius: 8px;
      background: var(--gold);
      color: #241332;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-family: inherit;
      font-size: 14px;
      font-weight: 900;
      line-height: 1;
      min-height: 42px;
      padding: 12px 14px;
      text-decoration: none;
    }
    .quick-links a:hover, .button-link:hover, .copy-button:hover { background: #f1c761; }
    .button-link.secondary { background: #ffffff; border: 1px solid var(--line); color: var(--violet); }
    .hero-grid, .three-col { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; margin-top: 26px; }
    .hero-card { background: rgba(255, 255, 255, 0.1); border: 1px solid rgba(255, 255, 255, 0.18); border-radius: 8px; padding: 18px; min-height: 126px; }
    .hero-card strong { color: #ffe1a1; display: block; font-size: 15px; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 8px; }
    .section { margin-top: 24px; background: rgba(255, 255, 255, 0.88); border: 1px solid var(--line); border-radius: 8px; padding: 28px; box-shadow: 0 10px 24px rgba(48, 31, 61, 0.08); }
    .section h2 { color: var(--violet-deep); font-size: clamp(25px, 3vw, 38px); margin-bottom: 12px; }
    .section-intro { max-width: 900px; color: var(--muted); margin: 0 0 20px; }
    .two-col { display: grid; grid-template-columns: repeat(2, 1fr); gap: 16px; }
    .card { background: var(--panel); border: 1px solid var(--line); border-radius: 8px; padding: 20px; }
    .card h3 { color: var(--violet); font-size: 20px; margin-bottom: 8px; }
    .tag { display: inline-block; border-radius: 8px; padding: 5px 9px; margin-bottom: 12px; background: var(--gold-soft); color: #765210; font-weight: 800; font-size: 12px; text-transform: uppercase; letter-spacing: 0.06em; }
    ul, ol { margin: 10px 0 0 20px; padding: 0; }
    li { margin: 8px 0; }
    .link-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-bottom: 24px; }
    .lesson-link { background: #fff; border: 1px solid var(--line); border-radius: 8px; color: var(--violet-deep); display: block; font-weight: 800; padding: 14px; text-decoration: none; }
    .lesson-link:hover { border-color: var(--gold); box-shadow: 0 8px 20px rgba(48, 31, 61, 0.1); transform: translateY(-1px); }
    .lesson { display: grid; grid-template-columns: 84px 1fr; gap: 16px; border-top: 1px solid var(--line); padding: 20px 0; }
    .lesson:first-of-type { border-top: 0; padding-top: 0; }
    .lesson-number { width: 64px; height: 64px; border-radius: 8px; background: linear-gradient(135deg, var(--violet), var(--rose)); color: #fff; display: grid; place-items: center; font-size: 24px; font-weight: 900; box-shadow: 0 12px 22px rgba(77, 39, 112, 0.22); }
    .lesson-number a { color: #fff; display: grid; height: 100%; place-items: center; text-decoration: none; width: 100%; }
    .callout { border-left: 5px solid var(--gold); background: #fff7dc; padding: 16px 18px; border-radius: 8px; margin-top: 16px; }
    .warning { border-left-color: var(--rose); background: #fff0f5; }
    table { width: 100%; border-collapse: collapse; overflow: hidden; border-radius: 8px; background: #fff; border: 1px solid var(--line); }
    th, td { text-align: left; vertical-align: top; border-bottom: 1px solid var(--line); padding: 14px; }
    th { background: var(--violet-deep); color: #fff; font-size: 13px; text-transform: uppercase; letter-spacing: 0.06em; }
    tr:last-child td { border-bottom: 0; }
    .script-box { background: #241332; color: #fdf5e8; border-radius: 8px; padding: 18px; font-family: "Courier New", Courier, monospace; font-size: 14px; line-height: 1.55; white-space: pre-wrap; }
    .copy-row { align-items: center; display: flex; flex-wrap: wrap; gap: 10px; justify-content: space-between; margin-bottom: 10px; }
    .checklist { list-style: none; margin-left: 0; }
    .checklist li { padding-left: 34px; position: relative; }
    .checklist li:before { content: ""; position: absolute; left: 0; top: 5px; width: 19px; height: 19px; border-radius: 5px; border: 2px solid var(--teal); background: #efffff; }
    .footer { margin-top: 24px; text-align: center; color: var(--muted); font-size: 14px; }
    @media (max-width: 820px) {
      .hero { padding: 24px; }
      .hero-grid, .two-col, .three-col, .link-grid { grid-template-columns: 1fr; }
      .lesson { grid-template-columns: 1fr; }
      table, thead, tbody, th, td, tr { display: block; }
      th { display: none; }
      td { border-bottom: 0; padding: 12px 14px; }
      tr { border-bottom: 1px solid var(--line); padding: 8px 0; }
    }
  </style>
</head>
<body>
  <main class="page" id="top">
    <section class="hero">
      <span class="eyebrow">The Creator Plug Academy - Module 17</span>
      <h1>Journals & Planners</h1>
      <p class="subtitle">
        A product-building module for turning planners, journals, trackers, workbooks, and printable templates into sellable digital products without repeating the Canva basics.
      </p>
      <nav class="quick-links" aria-label="Module quick links">
        <a href="#overview">Overview</a>
        <a href="#lessons">Lessons</a>
        <a href="#ideas">Product Ideas</a>
        <a href="#page-bank">Page Bank</a>
        <a href="#bundles">Bundles</a>
        <a href="#pricing">Pricing</a>
        <a href="#copy">Sales Copy</a>
        <a href="#challenge">Challenge</a>
        <a href="#sources">Sources</a>
      </nav>
      <div class="hero-grid">
        <div class="hero-card"><strong>Best For</strong>Creators who want to sell printable PDFs, digital planners, Canva templates, guided journals, and workbook-style products.</div>
        <div class="hero-card"><strong>Core Skill</strong>Turning a niche problem into a structured planner product with useful pages, clear outcomes, mockups, and sales copy.</div>
        <div class="hero-card"><strong>Final Outcome</strong>A ready-to-launch planner or journal product with page list, bundle plan, pricing, listing copy, and delivery checklist.</div>
      </div>
    </section>

    <section class="section" id="overview">
      <h2>Module Overview</h2>
      <p class="section-intro">
        Journals and planners are digital product containers. The value is not just pretty pages. The value is helping a customer organize, reflect, plan, track, decide, or complete something. This module teaches students how to create planner products that solve real problems and can be sold through Etsy, Stan Store, Beacons, Shopify, Gumroad, Payhip, or their own creator store.
      </p>
      <div class="two-col">
        <div class="card">
          <span class="tag">What students learn</span>
          <ul>
            <li>How to choose a profitable planner or journal niche.</li>
            <li>How to structure pages around a real customer outcome.</li>
            <li>How to create printable PDFs, digital planners, workbooks, and Canva templates.</li>
            <li>How to package bundles, bonuses, and upsells.</li>
            <li>How to write listing copy, create mockups, and deliver files.</li>
            <li>How to avoid licensing and template resale mistakes.</li>
          </ul>
        </div>
        <div class="card">
          <span class="tag">Not a Canva repeat</span>
          <p>
            Canva Crash Course teaches the design tool. This module teaches the product model: product strategy, page planning, bundle design, pricing, sales copy, delivery, and launch. Students can use Canva, but the lesson is about creating a sellable planner product.
          </p>
        </div>
      </div>
      <div class="callout warning">
        <strong>Licensing note:</strong> Students must check the license for fonts, graphics, templates, mockups, and stock elements before selling. Do not resell another creator's template as-is.
      </div>
    </section>

    <section class="section" id="lessons">
      <h2>Full Lesson Plan</h2>
      <p class="section-intro">Use these lessons as the core curriculum for the Journals & Planners module.</p>
      <div class="link-grid">
        <a class="lesson-link" href="#lesson-1">1. What Makes a Planner Sell</a>
        <a class="lesson-link" href="#lesson-2">2. Choose the Niche and Customer</a>
        <a class="lesson-link" href="#lesson-3">3. Pick the Product Type</a>
        <a class="lesson-link" href="#lesson-4">4. Plan the Page Structure</a>
        <a class="lesson-link" href="#lesson-5">5. Design for Use, Not Just Looks</a>
        <a class="lesson-link" href="#lesson-6">6. Create Bundles and Bonuses</a>
        <a class="lesson-link" href="#lesson-7">7. Price the Product</a>
        <a class="lesson-link" href="#lesson-8">8. Create Mockups and Listings</a>
        <a class="lesson-link" href="#lesson-9">9. Deliver Files and Support Buyers</a>
        <a class="lesson-link" href="#lesson-10">10. Launch and Improve</a>
      </div>

      <div class="lesson" id="lesson-1">
        <div class="lesson-number"><a href="#lessons">1</a></div>
        <div>
          <h3>What Makes a Planner Sell</h3>
          <p>
            A planner sells when it helps a specific person make progress on a specific goal. Pretty design helps, but a beautiful planner with no useful structure will not create repeat buyers. Students should start with the customer's problem, not the cover design.
          </p>
          <table>
            <thead><tr><th>Weak Product</th><th>Stronger Product</th><th>Why It Works</th></tr></thead>
            <tbody>
              <tr><td>Generic daily planner</td><td>Daily content planner for beginner TikTok creators</td><td>Specific customer and use case.</td></tr>
              <tr><td>Blank journal</td><td>30-day confidence journal for women launching digital products</td><td>Guided outcome and emotional hook.</td></tr>
              <tr><td>Budget planner</td><td>Side hustle income tracker for creators with irregular income</td><td>Solves a real niche problem.</td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <div class="lesson" id="lesson-2">
        <div class="lesson-number"><a href="#lessons">2</a></div>
        <div>
          <h3>Choose the Niche and Customer</h3>
          <p>
            The niche decides the page types, language, mockups, keywords, and sales copy. A planner for brides, teachers, fitness coaches, content creators, moms, or Etsy sellers will not have the same structure.
          </p>
          <div class="script-box">Niche worksheet:
My planner is for:
___

They are trying to:
___

They feel stuck because:
___

They need pages that help them:
___

The transformation is:
from ___ to ___.</div>
        </div>
      </div>

      <div class="lesson" id="lesson-3">
        <div class="lesson-number"><a href="#lessons">3</a></div>
        <div>
          <h3>Pick the Product Type</h3>
          <p>
            Students can sell several types of planner products. The best choice depends on the customer, platform, and how the buyer wants to use it.
          </p>
          <table>
            <thead><tr><th>Type</th><th>Best For</th><th>Delivery</th></tr></thead>
            <tbody>
              <tr><td>Printable PDF</td><td>Buyers who want to print pages at home or a print shop.</td><td>PDF file, usually letter/A4 size.</td></tr>
              <tr><td>Digital Planner</td><td>iPad/GoodNotes/Notability users.</td><td>Hyperlinked PDF, usage instructions.</td></tr>
              <tr><td>Canva Template</td><td>Buyers who want to customize colors, text, and layouts.</td><td>Canva template link plus instructions.</td></tr>
              <tr><td>Workbook</td><td>Students learning a process or completing exercises.</td><td>PDF workbook, fillable PDF, or Canva template.</td></tr>
              <tr><td>Tracker Bundle</td><td>Customers tracking habits, money, content, fitness, meals, or goals.</td><td>Multiple printable PDFs or spreadsheet add-on.</td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <div class="lesson" id="lesson-4">
        <div class="lesson-number"><a href="#lessons">4</a></div>
        <div>
          <h3>Plan the Page Structure</h3>
          <p>
            The page list should follow the buyer's journey. Start with orientation, then planning, then action, then tracking, then reflection.
          </p>
          <div class="three-col">
            <div class="card"><h3>Start Pages</h3><ul><li>welcome page</li><li>how to use</li><li>goal setting</li><li>current situation audit</li></ul></div>
            <div class="card"><h3>Action Pages</h3><ul><li>daily planner</li><li>weekly planner</li><li>checklist</li><li>project plan</li><li>content calendar</li></ul></div>
            <div class="card"><h3>Reflection Pages</h3><ul><li>weekly review</li><li>monthly review</li><li>lesson learned</li><li>progress tracker</li><li>next step planner</li></ul></div>
          </div>
        </div>
      </div>

      <div class="lesson" id="lesson-5">
        <div class="lesson-number"><a href="#lessons">5</a></div>
        <div>
          <h3>Design for Use, Not Just Looks</h3>
          <p>
            Good planners are easy to write on, print, navigate, and understand. Students should avoid tiny text, cluttered backgrounds, low contrast, and pages that look pretty but do not guide action.
          </p>
          <ul class="checklist">
            <li>Use readable font sizes.</li>
            <li>Leave enough writing space.</li>
            <li>Use consistent margins.</li>
            <li>Keep page titles clear.</li>
            <li>Do not overload every page with decoration.</li>
            <li>Test print one page before selling printable products.</li>
            <li>Export PDF Print when the buyer is expected to print.</li>
          </ul>
        </div>
      </div>

      <div class="lesson" id="lesson-6">
        <div class="lesson-number"><a href="#lessons">6</a></div>
        <div>
          <h3>Create Bundles and Bonuses</h3>
          <p>
            Bundles increase perceived value and make the product easier to sell. A good bundle includes pages that solve related problems, not random extras.
          </p>
          <table>
            <thead><tr><th>Bundle Type</th><th>Includes</th><th>Example</th></tr></thead>
            <tbody>
              <tr><td>Starter Bundle</td><td>Core planner, checklist, quick-start guide.</td><td>Creator Store Setup Planner + Launch Checklist.</td></tr>
              <tr><td>Premium Bundle</td><td>Planner, journal, trackers, templates, bonus pages.</td><td>Digital Product Launch Planner + Sales Tracker + Content Calendar.</td></tr>
              <tr><td>Niche Vault</td><td>Multiple products around one audience.</td><td>Self-Care Journal, Habit Tracker, Mood Tracker, Weekly Reset Planner.</td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <div class="lesson" id="lesson-7">
        <div class="lesson-number"><a href="#lessons">7</a></div>
        <div>
          <h3>Price the Product</h3>
          <p>
            Pricing depends on usefulness, page count, niche demand, file type, customization rights, bonuses, and perceived transformation. Students should not price only by page count.
          </p>
          <div class="three-col">
            <div class="card"><h3>Low Ticket</h3><p>$3-$9 for simple printables, single trackers, mini journals, and quick templates.</p></div>
            <div class="card"><h3>Mid Ticket</h3><p>$10-$29 for planners, workbooks, bundles, niche templates, and guided journals.</p></div>
            <div class="card"><h3>Higher Ticket</h3><p>$30-$97+ for large vaults, commercial-use bundles, editable templates, or niche product kits.</p></div>
          </div>
          <div class="callout"><strong>Price test:</strong> If the product saves time, reduces confusion, and gives a guided outcome, it can usually be priced higher than a plain blank template.</div>
        </div>
      </div>

      <div class="lesson" id="lesson-8">
        <div class="lesson-number"><a href="#lessons">8</a></div>
        <div>
          <h3>Create Mockups and Listings</h3>
          <p>
            Buyers need to see what they are getting. Mockups should show the cover, inside pages, page count, file type, dimensions, and how the product is used.
          </p>
          <ul>
            <li>Show cover and 3-6 inside pages.</li>
            <li>Show product size: letter, A4, iPad, Canva template, or PDF.</li>
            <li>Show what is included in the download.</li>
            <li>Use lifestyle mockups only if they match the product.</li>
            <li>Do not imply a physical product if it is a digital download.</li>
          </ul>
        </div>
      </div>

      <div class="lesson" id="lesson-9">
        <div class="lesson-number"><a href="#lessons">9</a></div>
        <div>
          <h3>Deliver Files and Support Buyers</h3>
          <p>
            The buyer experience matters. Students should include clear file names, simple instructions, and a support note so customers know how to access the product.
          </p>
          <div class="script-box">Suggested file package:
1. Product PDF
2. Print instructions
3. Canva template link instructions, if applicable
4. Terms of use
5. Thank-you / support PDF
6. Bonus files, if included</div>
        </div>
      </div>

      <div class="lesson" id="lesson-10">
        <div class="lesson-number"><a href="#lessons">10</a></div>
        <div>
          <h3>Launch and Improve</h3>
          <p>
            Students should launch a useful first version, collect feedback, then improve the product. Waiting for a perfect 200-page planner can stop them from ever selling.
          </p>
          <ul>
            <li>Start with a minimum viable planner: 10-25 useful pages.</li>
            <li>Sell the first version at a simple price.</li>
            <li>Ask buyers what pages they used most.</li>
            <li>Add pages based on real feedback.</li>
            <li>Create a bundle or version 2 after the first product is validated.</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="section" id="ideas">
      <h2>Product Idea Bank</h2>
      <p class="section-intro">Students can use these ideas as starting points and customize them for their audience.</p>
      <div class="three-col">
        <div class="card"><h3>Creator Business</h3><ul><li>content planner</li><li>digital product launch planner</li><li>brand clarity workbook</li><li>sales tracker</li><li>UGC pitch tracker</li><li>creator store setup workbook</li></ul></div>
        <div class="card"><h3>Money and Goals</h3><ul><li>side hustle income tracker</li><li>debt payoff planner</li><li>budget planner</li><li>savings challenge tracker</li><li>goal setting workbook</li><li>monthly reset planner</li></ul></div>
        <div class="card"><h3>Wellness and Lifestyle</h3><ul><li>self-care journal</li><li>fitness planner</li><li>meal planner</li><li>habit tracker</li><li>mood tracker</li><li>morning routine planner</li></ul></div>
        <div class="card"><h3>Faith and Reflection</h3><ul><li>prayer journal</li><li>gratitude journal</li><li>scripture study planner</li><li>faith goal planner</li><li>reflection workbook</li><li>daily devotional tracker</li></ul></div>
        <div class="card"><h3>Family and Home</h3><ul><li>mom planner</li><li>cleaning tracker</li><li>family command center</li><li>school planner</li><li>chore chart</li><li>holiday planning bundle</li></ul></div>
        <div class="card"><h3>Business Niches</h3><ul><li>beauty business planner</li><li>lash tech client tracker</li><li>coach client tracker</li><li>event planner workbook</li><li>Etsy shop planner</li><li>tax prep organizer</li></ul></div>
      </div>
    </section>

    <section class="section" id="page-bank">
      <h2>Planner Page Bank</h2>
      <p class="section-intro">Use this page bank to build products faster. Choose pages that support the outcome, not every page on the list.</p>
      <table>
        <thead><tr><th>Page Type</th><th>What It Helps With</th><th>Example Product</th></tr></thead>
        <tbody>
          <tr><td>Goal Map</td><td>Clarifies desired outcome and timeline.</td><td>90-Day Creator Goal Planner</td></tr>
          <tr><td>Brain Dump</td><td>Gets ideas out of the head and onto paper.</td><td>Content Idea Workbook</td></tr>
          <tr><td>Weekly Planner</td><td>Organizes actions by week.</td><td>Small Business Weekly Planner</td></tr>
          <tr><td>Daily Page</td><td>Plans priorities, tasks, and reflection.</td><td>Productivity Planner</td></tr>
          <tr><td>Tracker</td><td>Tracks habits, income, workouts, content, or mood.</td><td>Habit Tracker Bundle</td></tr>
          <tr><td>Checklist</td><td>Helps buyers complete a process.</td><td>Launch Checklist</td></tr>
          <tr><td>Reflection Page</td><td>Turns experience into learning.</td><td>Self-Growth Journal</td></tr>
          <tr><td>Prompt Page</td><td>Guides journaling or planning.</td><td>Confidence Journal</td></tr>
          <tr><td>Audit Page</td><td>Reviews current situation.</td><td>Brand Audit Workbook</td></tr>
          <tr><td>Resource Page</td><td>Holds links, tools, contacts, or notes.</td><td>Business Organizer</td></tr>
        </tbody>
      </table>
    </section>

    <section class="section" id="bundles">
      <h2>Bundle Builder</h2>
      <p class="section-intro">Bundles help students sell more value without creating an entirely new product from scratch.</p>
      <div class="two-col">
        <div class="card">
          <div class="copy-row"><h3>Bundle Planning Worksheet</h3><button class="copy-button" type="button" data-copy-target="bundle-worksheet">Copy Worksheet</button></div>
          <div class="script-box" id="bundle-worksheet">Bundle name:
___

Buyer:
___

Main problem:
___

Core product:
___

Bonus 1:
___

Bonus 2:
___

Bonus 3:
___

Total file types included:
___

Price:
___

Why this bundle is valuable:
___</div>
        </div>
        <div class="card">
          <h3>Bundle Examples</h3>
          <ul>
            <li><strong>Creator Launch Bundle:</strong> content planner, offer planner, launch checklist, sales tracker.</li>
            <li><strong>Self-Care Reset Bundle:</strong> self-care journal, mood tracker, habit tracker, weekly reset planner.</li>
            <li><strong>Digital Product Seller Bundle:</strong> product idea workbook, listing copy worksheet, mockup checklist, launch calendar.</li>
            <li><strong>Faith Planner Bundle:</strong> prayer journal, gratitude pages, scripture study sheets, weekly faith goals.</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="section" id="pricing">
      <h2>Pricing and Offer Stack</h2>
      <p class="section-intro">Students can make more money from planners by stacking offers instead of selling one file only.</p>
      <table>
        <thead><tr><th>Offer Level</th><th>Example</th><th>Purpose</th></tr></thead>
        <tbody>
          <tr><td>Freebie</td><td>1-page tracker or checklist</td><td>Build email list and trust.</td></tr>
          <tr><td>Mini Product</td><td>$5 habit tracker or content planner</td><td>Easy first purchase.</td></tr>
          <tr><td>Core Product</td><td>$17-$29 full planner or workbook</td><td>Main digital product offer.</td></tr>
          <tr><td>Bundle</td><td>$37-$97 vault or product kit</td><td>Higher value and stronger perceived transformation.</td></tr>
          <tr><td>Upsell</td><td>Editable Canva version, commercial-use version, video walkthrough</td><td>Increases order value.</td></tr>
        </tbody>
      </table>
    </section>

    <section class="section" id="copy">
      <h2>Sales Copy Templates</h2>
      <div class="two-col">
        <div class="card">
          <div class="copy-row"><h3>Product Description</h3><button class="copy-button" type="button" data-copy-target="product-description">Copy Template</button></div>
          <div class="script-box" id="product-description">This ___ was created for ___ who want to ___ without ___.

Inside, you will get:
- ___
- ___
- ___

Use this planner to:
- ___
- ___
- ___

You will receive:
- File type: ___
- Size: ___
- Pages: ___
- Delivery: digital download

Important: This is a digital product. No physical item will be shipped.</div>
        </div>
        <div class="card">
          <div class="copy-row"><h3>Listing Title Formula</h3><button class="copy-button" type="button" data-copy-target="listing-title">Copy Formula</button></div>
          <div class="script-box" id="listing-title">[Niche] [Product Type] for [Outcome] | [Format] | [Use Case]

Examples:
Content Planner for TikTok Creators | Printable PDF | 30-Day Posting Workbook
Self-Care Journal for Busy Moms | Printable Planner | Weekly Reset Pages
Digital Product Launch Planner | Canva Template | Seller Workbook</div>
        </div>
        <div class="card">
          <div class="copy-row"><h3>Customer Instructions</h3><button class="copy-button" type="button" data-copy-target="customer-instructions">Copy Instructions</button></div>
          <div class="script-box" id="customer-instructions">How to use your download:
1. Download the PDF file.
2. Save a copy to your device.
3. Print at home or through a print shop if you purchased a printable.
4. If using a digital planner, import the PDF into your preferred note-taking app.
5. If using a Canva template, open the template link and make a copy in your Canva account.

Need help? Contact:
___</div>
        </div>
        <div class="card">
          <div class="copy-row"><h3>Terms of Use</h3><button class="copy-button" type="button" data-copy-target="terms-use">Copy Terms</button></div>
          <div class="script-box" id="terms-use">Terms of use:
This product is for personal use unless commercial rights are clearly stated.
You may not resell, redistribute, share, or claim this product as your own.
You may not upload this file to public sharing sites.
Due to the digital nature of this product, refunds may be limited according to the shop policy.
Please contact ___ with any access issues.</div>
        </div>
      </div>
    </section>

    <section class="section" id="challenge">
      <h2>14-Day Planner Product Challenge</h2>
      <table>
        <thead><tr><th>Day</th><th>Assignment</th><th>Deliverable</th></tr></thead>
        <tbody>
          <tr><td>1</td><td>Choose one niche and buyer.</td><td>Buyer statement.</td></tr>
          <tr><td>2</td><td>Choose one product type.</td><td>Printable, digital planner, workbook, or Canva template.</td></tr>
          <tr><td>3</td><td>Write the transformation.</td><td>From/to statement.</td></tr>
          <tr><td>4</td><td>Build the page list.</td><td>10-25 page outline.</td></tr>
          <tr><td>5</td><td>Create the first 5 pages.</td><td>Draft pages.</td></tr>
          <tr><td>6</td><td>Create the next 5 pages.</td><td>Draft pages.</td></tr>
          <tr><td>7</td><td>Design cover and instructions.</td><td>Cover and how-to page.</td></tr>
          <tr><td>8</td><td>Export test file and review.</td><td>Test PDF.</td></tr>
          <tr><td>9</td><td>Create mockups.</td><td>3-6 listing images.</td></tr>
          <tr><td>10</td><td>Write listing title and description.</td><td>Sales copy.</td></tr>
          <tr><td>11</td><td>Create delivery files.</td><td>Final PDF/package.</td></tr>
          <tr><td>12</td><td>Set price and offer stack.</td><td>Pricing plan.</td></tr>
          <tr><td>13</td><td>Create 3 promo posts.</td><td>Launch content.</td></tr>
          <tr><td>14</td><td>Publish or prepare product listing.</td><td>Launch-ready product.</td></tr>
        </tbody>
      </table>
    </section>

    <section class="section" id="mistakes">
      <h2>Beginner Mistakes to Avoid</h2>
      <div class="two-col">
        <div class="card"><h3>Only Making It Pretty</h3><p>A planner needs function. Every page should help the buyer do something useful.</p></div>
        <div class="card"><h3>Copying Another Seller</h3><p>Use market research for insight, not copying. Make your own structure, wording, and design.</p></div>
        <div class="card"><h3>No Instructions</h3><p>Customers need to know how to download, print, open, or customize the product.</p></div>
        <div class="card"><h3>Wrong File Expectations</h3><p>Be clear if the buyer receives a PDF, Canva link, digital planner, ZIP file, or printable.</p></div>
        <div class="card"><h3>Ignoring Licensing</h3><p>Do not use fonts, graphics, templates, or mockups commercially unless the license allows it.</p></div>
        <div class="card"><h3>Overbuilding Before Testing</h3><p>Start with a useful smaller product before spending weeks on a huge vault.</p></div>
      </div>
    </section>

    <section class="section" id="completion">
      <h2>Module Completion Requirements</h2>
      <ul class="checklist">
        <li>Choose one planner or journal niche.</li>
        <li>Define the buyer and transformation.</li>
        <li>Create a page list with at least 10 useful pages.</li>
        <li>Create the first product draft.</li>
        <li>Export and test the file.</li>
        <li>Create 3-6 mockup/listing images.</li>
        <li>Write the listing title, description, and instructions.</li>
        <li>Review licensing and terms of use.</li>
        <li>Create 3 promotional posts.</li>
        <li>Publish or prepare the product for launch.</li>
      </ul>
    </section>

    <section class="section" id="sources">
      <h2>Reference Links Used</h2>
      <p class="section-intro">These links help students understand platform expectations, Canva licensing, and digital product delivery basics.</p>
      <ul>
        <li><a href="https://www.etsy.com/seller-handbook/article/1026517522818" target="_blank" rel="noopener">Etsy Seller Handbook: Getting started with digital listings</a></li>
        <li><a href="https://www.canva.com/policies/content-license-agreement/" target="_blank" rel="noopener">Canva Content License Agreement</a></li>
        <li><a href="https://www.canva.com/help/using-canva-to-create-products-for-sale/" target="_blank" rel="noopener">Canva Help: Using Canva to create products for sale</a></li>
        <li><a href="https://www.canva.com/help/download-file-types/" target="_blank" rel="noopener">Canva Help: Download file types</a></li>
      </ul>
    </section>

    <p class="footer">
      <a class="button-link secondary" href="#top">Back to top</a>
      <br /><br />
      The Creator Plug Academy - Journals & Planners - April 2026
    </p>
  </main>
  <script>
    document.querySelectorAll("[data-copy-target]").forEach(function(button) {
      button.addEventListener("click", function() {
        var target = document.getElementById(button.getAttribute("data-copy-target"));
        if (!target) return;
        var text = target.innerText;
        var copyText = function() {
          var textArea = document.createElement("textarea");
          textArea.value = text;
          textArea.setAttribute("readonly", "");
          textArea.style.position = "fixed";
          textArea.style.left = "-9999px";
          document.body.appendChild(textArea);
          textArea.select();
          document.execCommand("copy");
          document.body.removeChild(textArea);
        };
        var copied = navigator.clipboard && window.isSecureContext
          ? navigator.clipboard.writeText(text)
          : new Promise(function(resolve) {
              copyText();
              resolve();
            });
        copied.then(function() {
          var original = button.innerText;
          button.innerText = "Copied";
          setTimeout(function() { button.innerText = original; }, 1600);
        });
      });
    });
  </script>
</body>
</html>
