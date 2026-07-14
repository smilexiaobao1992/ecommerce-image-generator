# China Ecommerce Image Strategy

Use this reference before planning or generating any domestic ecommerce image.

## Contents

1. The core difference from Amazon
2. Platform priors
3. Premium flagship visual preset
4. Image-role design
5. Buyer-first content architecture
6. Chinese ecommerce copy system
7. Detail-page narrative
8. Prompt construction
9. Reference-image adaptation
10. Visual quality gates
11. Default set logic

## 1. The core difference from Amazon

Do not translate an Amazon slot system. Domestic ecommerce commonly combines:

- search-feed competition and platform UI overlays;
- Chinese mobile reading at small sizes;
- a platform/category-specific first image plus separate white-background fields;
- carousel images with stronger local information hierarchy;
- SKU attribute images that must make variant and quantity unambiguous;
- longer, modular detail pages with stronger narrative rhythm;
- campaign creatives whose price and event rules differ from ordinary listings.

The durable model is:

```text
platform + category + placement + buyer decision + truthful proof + brand system
```

not:

```text
one universal main-image template + translated slogans + resized exports
```

## 2. Platform priors, not hard rules

Use these only as starting art direction. Validate them against the current
category, user examples, and platform UI.

### Taobao

- Stronger room for differentiated shop style, niche positioning, and benefit-led
  first-image communication when the slot/category permits it.
- Mobile hierarchy should reveal product type first, key difference second, and
  style/brand third.
- Detail pages can be editorial, but the opening screens still need product,
  benefit, and proof before long brand storytelling.
- Use platform-neutral product truth so the same source assets can support 1:1
  and 3:4 publishing flows without unsafe cropping.

### Tmall

- Favour a coherent brand system, stronger finish, cleaner typography, and more
  documented trust signals.
- Let product photography, material/technology proof, official model clarity,
  and service confidence carry the page.
- Avoid turning “premium” into empty black-gold gradients. Premium comes from
  restraint, photography, hierarchy, spacing, and credible proof.
- Campaign periods may use stronger promotional overlays, but ordinary listing
  assets should not depend on stale prices or event badges.

### JD

- Lead with model identity, exact parameters, compatibility, authentic product
  detail, function, service, and purchase confidence.
- Technical diagrams should be clean and rational: dimension lines, port/model
  maps, material sections, package contents, warranty/service conditions.
- Keep first-image direction conservative until the exact field/category rule
  is checked. Do not add marketing text to a white-background slot.
- Make similar model differences obvious before purchase; reduce wrong-SKU risk.

### Pinduoduo

- Product identity, included quantity, core value, and immediate usefulness must
  read quickly at thumbnail size.
- Use larger, simpler benefit language and fewer proof points per image.
- Value communication does not require a noisy bargain poster. Strong product
  scale, clear quantity, one decisive benefit, and high contrast often work better.
- Never imply a pictured premium SKU is available at the lowest displayed price
  when the price belongs to another quantity or variant.
- Keep volatile price, coupon, gift, and countdown information editable and
  conditionally accurate.

### Cross-platform set

Create one product-truth source and separate compositions:

- Taobao: distinction and style;
- Tmall: brand and trust;
- JD: parameters and certainty;
- Pinduoduo: value and immediate comprehension.

Do not caricature the platforms. A premium Pinduoduo category may be cleaner
than a promotion-heavy Tmall campaign; the live category always wins.

## 3. Premium flagship visual preset

Use this preset when the user asks for `高端`, `大气`, `旗舰店`, `品牌感`,
`premium`, or an equivalent mature-brand direction. It is a positioning choice,
not a claim that every top-selling listing uses this style.

### Art direction

- Aim for editorial product photography suitable for a mature Tmall flagship
  store or premium offline catalogue.
- Make the product the visual authority: normally 60-75% of the square frame,
  clearly grounded, with recognisable silhouette and material texture.
- Use one hero product, one decisive claim, and one supporting line. Add a second
  image, inset, or label only when it supplies real proof.
- Choose either a restrained architectural studio or a believable premium home.
  Warm ivory, stone, plaster, timber, and controlled shadow are useful; generic
  luxury props are not.
- Create depth with directional daylight, soft long shadows, edge highlights,
  and contact shadows. Steel should read as steel; fabric, wood, leather, and
  plastic should retain their own finish.

### Colour system

- Use roughly 70-85% warm neutral or quiet environmental colour, 10-20%
  charcoal/product colour, and no more than 5-10% brand accent.
- Suitable neutral families include warm ivory, light stone, greige, taupe,
  charcoal, and near-black. Accent colour should identify meaning, not fill
  decorative blocks.
- Do not equate premium with black-gold gradients. A near-black editorial scene
  is valid only when narrow highlights preserve the full product silhouette.
- Avoid broad saturated red/yellow fields, discount-card colour blocking, and
  multiple competing accents unless the supplied brand system or campaign
  explicitly requires them.

### Composition patterns

Prefer one of these structures:

1. **Product right / copy left** — large product on the right two-thirds,
   deliberate negative space on the upper-left, low visual noise.
2. **Architectural full-bleed** — product dominates a believable room or studio;
   one quiet claim sits in an uncluttered corner.
3. **Dark editorial** — near-black space, sculpted rim light, minimal pale copy,
   and no gold badges or fake luxury motifs.

For search-feed images, the product must remain legible before the room and copy.
Do not shrink the product to make the scene look cinematic.

### Typography system

For deterministic production typesetting, prefer a modern Chinese sans with
complete glyph coverage and an appropriate licence, such as Source Han Sans SC /
Noto Sans CJK SC, HarmonyOS Sans SC, Alibaba PuHuiTi, or MiSans. Use the available
brand font when one is supplied. Typeface names in an AI-image prompt describe
the intended character only; they do not prove that the generated pixels use
that exact font.

- Headline: 1-2 lines, usually 4-10 Chinese characters, approximately 8-14% of
  canvas height, weight 600-700, line height 0.95-1.08, tracking -1% to +2%.
- Supporting line: approximately 2.5-4% of canvas height, weight 400-500,
  generous breathing room; use separators consistently.
- Functional labels or English eyebrow: smaller and quieter, weight 400-500,
  tracking 2-6%; never let decorative English outrank the Chinese conclusion.
- Use at most two font weights on one first image. Align text to a visible grid,
  keep line breaks deliberate, and avoid heavy outlines, bevels, glow, faux 3D,
  or mixed display fonts.
- A key number may be largest only when it is verified and purchase-decisive.
  Otherwise the product, not typography, owns the frame.

For exact final copy, generate a clean base with a reserved text zone and typeset
deterministically. Direct AI-rendered Chinese is acceptable only for a reviewed
visual draft.

### Premium anti-patterns

Reject these unless the user supplies them as a mandatory brand device:

- red corner wedges, red ribbon captions, coupon strips, price explosions;
- three stacked photo windows or detail-page collage inside a first image;
- pill-badge collections, floating icon constellations, certification walls;
- black/yellow bargain cards, excessive strokes, drop shadows, bevels, and glow;
- generic marble, gold frames, chandeliers, sports cars, or other borrowed luxury;
- a tiny product surrounded by oversized slogans and empty effects.

Premium quality gate: could the asset sit beside a mature flagship-store product
or a premium retail catalogue without relying on a price badge? Do material,
light, spacing, and type make the product feel considered?

## 4. Image-role design

### MAIN-01 — Search/exposure first image

Goal: communicate product identity and the single strongest reason to click.

Decide first:

- Is this field a white-background compliance image or a selling image?
- What UI overlays, price blocks, corners, or crops cover the asset?
- Does the category sell through look, function, quantity, model, or price?
- Which visual tier is intended: value-led, technical, premium flagship, or the
  supplied brand system? Explicit user positioning overrides category-average
  decoration.

Composition:

- make the sellable product unmistakable and large;
- preserve a safe edge and avoid placing essential copy in UI collision zones;
- use one product-specific benefit, not five badges;
- show quantity/variant visually when it is a decisive purchase fact;
- use a scene only if it improves immediate comprehension rather than hiding form.

Avoid:

- generic “品质之选/美好生活/匠心制造” slogans;
- price explosions without verified current conditions;
- accessories styled as included items when they are only props;
- small product surrounded by oversized typography;
- main image that resembles a detail-page collage.

### WHITE-01 — Compliance product image

Goal: show the exact sellable item clearly.

- Prefer a real photographed item, accurate cutout, neutral lighting, and honest
  shadow when allowed.
- Show the correct SKU, quantity, orientation, colour, and included parts.
- Do not invent a perfect unbranded body, remove legally required markings, or
  smooth away functional seams.
- Omit text, badges, borders, props, and scenery unless the exact field rule
  explicitly permits them.

### CAR-02 — Core benefit

Goal: convert the most important click into interest.

- One concrete Chinese conclusion.
- One visible proof event: product in use, result, range, capacity, or meaningful
  before/after.
- 0-2 supporting facts.
- Product remains larger and clearer than decoration.

### CAR-03 — Function / structure / material proof

Goal: explain why the main benefit is credible.

- Connect labels to real parts.
- Combine claim + mechanism + proof.
- Use a hero product with 2-4 connected details, not a constellation of icons.
- For hidden structure, use an honest cutaway or diagram and label it as a
  structural illustration when it is not a documentary photo.

### CAR-04 — Size / fit / capacity / compatibility

Goal: prevent “will it fit/work with mine?” hesitation.

- Use exact supplied measurements only.
- Anchor dimensions to visible product edges or a floor plane.
- Show compatible models/users/spaces clearly, with exclusions when important.
- For inferred dimensions, use a planning placeholder, never a production label.

### CAR-05 — Lifestyle/use scenario

Goal: show who uses the product, where, and how.

- One primary action per scene.
- Hands, body, tools, food, cables, liquids, doors, and other contact points must
  interact physically with the correct product part.
- Use lived-in local environments appropriate to the buyer, not a generic CGI
  showroom.
- Keep secondary props from being mistaken for package contents.

### CAR-06 — Detail / workmanship / comfort / safety

Goal: add new confidence, not repeat CAR-03.

- Use one strong macro plus 1-3 connected insets.
- Show texture, seam, joint, contact surface, finish, closure, or interface under
  relevant use.
- Skip this role if the details add no new buyer value.

### CAR-07 — Choose one optional job

Use only when it removes a real objection:

- usage/installation steps;
- same-brand model comparison;
- package contents and exact quantity;
- care/maintenance;
- documented service or delivery scope;
- validated proof/certificate summary.

Do not manufacture a weak comparison or a fake “others” product just to fill a slot.

### SKU-01 — Attribute image

Goal: make the selected purchasable variant unmistakable.

- One image equals one exact SKU/variant.
- Match colour, finish, size, pack count, included pieces, and model name.
- Do not add promotional gifts to the SKU image unless they are inseparable from
  that exact SKU and current offer.
- When variants look similar, use deterministic labels outside the product body.

## 5. Buyer-first content architecture

Create an evidence matrix:

| Buyer question | Buyer-facing claim | Valid proof | Best role |
|---|---|---|---|
| What is it and why click? | Core product difference | Product silhouette/action/quantity | MAIN-01 or CAR-02 |
| Will it work for me? | Fit/compatibility | Exact size/model/range | CAR-04 or DET-06 |
| Why believe the claim? | Mechanism/material | Visible part/test/certificate | CAR-03 or DET-04 |
| What is included? | Exact bundle | Flat lay/labelled components | SKU-01 or CAR-07 |
| Is it easy/safe? | Process or contact benefit | Steps/hand contact/guard detail | CAR-06/07 |
| What happens after buying? | Service/delivery | Exact documented terms | DET-07/08 |

If no proof exists, weaken or remove the claim rather than decorating it.

## 6. Chinese ecommerce copy system

Write for rapid mobile scanning.

### Good headline forms

- mechanism + result: `双层锁扣 稳稳固定`
- exact capacity + use: `可收纳 24 件夏装`
- problem + result: `小户型也能轻松展开`
- material + benefit: `加厚钢管 支撑更稳`
- model/fit: `适配 13-16 英寸笔记本`
- quantity: `1 盒含 60 片`

Use only when truthful and supported.

### Weak headline forms

- 品质之选
- 匠心制造
- 开启美好生活
- 高端大气上档次
- 全面升级
- 买它就对了

Replace generic mood with a specific conclusion and visible proof.

### Text hierarchy

- headline: one conclusion;
- key number/model: largest element only when it drives the decision;
- support: 0-3 short facts;
- qualifier: near the claim, readable, not cosmetic small print;
- body paragraphs: detail page only, and preferably HTML/native text when the
  platform supports it rather than rasterised into an image.

### Typography

- Use Chinese typefaces with reliable glyph coverage. For premium work, apply
  the font families, weights, scale, tracking, and line-height rules in section 3.
- Keep line breaks deliberate; avoid splitting a number from its unit.
- Use one accent colour for meaning, not rainbow emphasis.
- Reserve whitespace before generating the scene; do not paste text over faces,
  hands, product controls, dimensions, or critical material detail.

## 7. Detail-page narrative

Treat each module as one screen-level argument.

### DET-01 — Product and value hero

Show the product clearly in the target context, with one specific promise.
Brand can frame the module but must not delay product comprehension.

### DET-02 — Real pain point to solution

Use a meaningful contrast: cluttered/organised, incompatible/fitted,
hard-to-use/easy process, weak contact/stable structure. Avoid exaggerated dirt,
danger, pain, or impossible before/after effects.

### DET-03 — Core benefit in action

Show the product doing its primary job. Use scale, movement, flow, pressure,
coverage, or capacity as physical proof.

### DET-04 — Why it works

Connect the full product to enlarged material, joint, motor, fabric, ingredient,
interface, or mechanism detail. Each inset answers a different objection.

### DET-05 — Who/where/how

Use separated scenes or vignettes for different users and environments. Do not
crowd unrelated actions around one distorted product.

### DET-06 — Choose correctly

Explain size, SKU, colour, model, compatibility, capacity, or installation space.
Use tables only when the buyer genuinely compares structured facts.

### DET-07 — Ownership experience

Show setup, care, package contents, replacement, storage, delivery, or service
only when it matters. Use exact terms and conditions.

### DET-08 — Trust close

Use documented brand, manufacturing, certification, testing, warranty, or
purchase-checklist content. Skip generic certificate walls and unsupported seals.

### Detail-page rhythm

Vary module grammar:

- cinematic scene;
- close product + strong claim;
- structural overlay;
- connected macro;
- comparison or process split;
- model/spec board;
- package/service close.

Avoid repeating `headline at top + centred product + four icon badges` down the page.

## 8. Prompt construction

Every prompt should make these decisions explicit:

1. platform, role, placement, ratio, and safe zones;
2. visual tier and supplied brand system;
3. exact product-reference fidelity;
4. single conclusion and proof event;
5. camera, product scale, and physical interaction;
6. foreground/middle/background;
7. exact Chinese copy or reserved text area;
8. font family character, weight, scale, tracking, line height, and label system;
9. category-appropriate lighting and environment;
10. forbidden claims, copied devices, geometry changes, and AI artifacts.

Example prompt skeleton:

```text
Create a [platform] [role] ecommerce image for [product]. Use the supplied
product photo as the exact sellable-item reference. Preserve [state, geometry,
colour, quantity, logo, included items].

Visual tier: [value-led / technical / premium flagship / supplied brand system].
Core viewpoint: [short Chinese conclusion].
Visual proof: [specific event tied to a real part/spec].
Composition: [camera and product placement]; foreground [hook]; middle ground
[product/proof]; background [context]. Reserve [zone] for text and keep [UI
collision zones] clear.
Visible text: [exact text] / no generated text; [hierarchy and colour treatment].
Style: [platform/category/brand direction], realistic commercial photography,
mobile thumbnail clarity.
Avoid: [unsupported claims, wrong SKU, invented accessories, distorted product,
copied competitor layout, garbled text, plastic people, impossible reflections].
```

## 9. Reference-image adaptation

From a user reference, extract:

- core viewpoint;
- proof device;
- composition skeleton;
- product scale and crop;
- text density and hierarchy;
- palette/contrast/mood;
- dynamic device and background depth.

Then change the layout, copy, colours, model, props, and scene for the current
product. If a reference conflicts with product truth, current rules, or buyer
value, keep only the useful communication principle.

## 10. Visual quality gates

### Human-made test

1. Would the image still communicate after decorative effects are removed?
2. Is the product clearer than the typography?
3. Does the proof attach to a real product part, action, scale, or fact?
4. Does it look like a marketplace designer could assemble it from photography,
   retouching, typography, diagrams, and honest overlays?
5. Is the composition original rather than a competitor trace?

### Avoid generic AI ecommerce style

- neon outlines and energy rings without functional meaning;
- black-gold gradients as a shortcut for premium;
- floating glass UI cards around every product;
- random icons disconnected from visible parts;
- perfect CGI rooms with no believable local context;
- duplicated people, impossible hands, bent products, or floating shadows;
- large generic slogans and unreadable support copy;
- one template repeated across the entire set.
- legacy red-banner or stacked-card marketplace styling presented as “premium”.

### Product consistency check

Compare every output against the reference:

- silhouette and proportions;
- colour and finish;
- visible seams, holes, ports, joints, handles, labels, and logos;
- folded/open/installed state;
- number of items and accessories;
- model/SKU and package relationship.

Any material mismatch requires regeneration or use of real product photography.

## 11. Default set logic

When the user asks broadly for “主图+轮播图” and gives enough product evidence:

- `MAIN-01`: one first-image direction after rule check;
- `CAR-02`: core benefit;
- `CAR-03`: mechanism/material proof;
- `CAR-04`: fit/size/model if purchase-relevant;
- `CAR-05`: one realistic use scene;
- `CAR-06`: detail proof only if new;
- `CAR-07`: steps/package/comparison/service only if it removes an objection.

Use 4-7 carousel images. Skip a role when it repeats another or lacks evidence.

When the user asks broadly for “详情页”, use 5-8 `DET` modules. Put product
identity, main benefit, and proof in the opening sequence; move model guide,
steps, package, and service later.

When the user asks for all four platforms, plan four `MAIN-01` variants and only
duplicate carousel/detail modules when the platform strategy truly changes. Do
not waste generation calls on identical resized art.
