---
name: china-ecommerce-image-generator
description: Use when a user asks to plan, generate, adapt, or revise product main images, white-background images, carousel selling-point images, SKU images, detail-page modules, or cross-platform image variants for Taobao, Tmall, JD, Pinduoduo, or 国内电商, including 主图, 轮播图, 卖点图, 详情页, 长图, 淘宝天猫图, 健身器材, 单杠, 双杠, 儿童单杠, 哑铃凳, 分体双杠, 参考竞品, 换平台, or 单张重做.
---

# China Ecommerce Image Generator

Create truthful, platform-aware Chinese ecommerce images from product photos,
selling points, and brand direction. Treat platform, category, and image role as
inputs; do not turn an Amazon carousel into Chinese by only translating text.

## Load the right references

- For any image request, read `references/china-ecommerce-image-strategy.md`.
- For home fitness or strength equipment—especially 单杠, 双杠, 儿童单杠,
  室内引体向上器, 力量塔, 哑铃凳, or 分体双杠—also read
  `references/fitness-strength-visual-system.md`.
- For platform-specific output, upload-ready claims, regulated categories,
  prices, promotions, certifications, comparison claims, or AI-generated final
  assets, also read `references/platform-rules-and-compliance.md`.
- Resolve both paths relative to this skill folder.

## Choose the execution mode

Infer the narrowest mode that satisfies the request:

- **Full product image kit**: first image/main image, a recommended carousel,
  and detail-page modules. Generate all three only when the user asks for a full
  set, full page, complete listing, or equivalent.
- **Main image only**: generate or revise only the first/search image. First
  resolve whether the user means an exposure image, a compliant white-background
  image, or a campaign creative; these are not interchangeable.
- **Carousel only**: generate a recommended 4-7 image set. Choose the count by
  distinct buyer questions, not by filling slots.
- **Detail page only**: generate 5-8 separate modules or a modular long-page
  plan. Do not silently collapse them into one unreadable storyboard.
- **SKU/attribute image only**: show one sellable variant accurately. Do not add
  accessories or quantities not included in that SKU.
- **One image/module**: regenerate only the named role using existing context.
- **Cross-platform adaptation**: keep one product-truth core, then redesign the
  hierarchy, text density, crop, and proof for each platform. Do not merely
  resize one canvas.
- **Creative direction exploration**: when the user asks for high-end options,
  style divergence, 发散, 多个方向, or rejects an output as generic/cheap, create
  three strategically different directions before polishing one. Change the
  visual event, camera/crop, lighting, typography, proof device, and copy angle;
  palette-only variants do not count. Generate separate previews when the user
  asks to see effects.
- **Prompt/plan only**: output shot plans and prompts without calling image
  generation only when the user explicitly asks for prompts, planning, or no
  generation.

When the user asks to “生成”, “出图”, “做图”, or equivalent, call the available
image-generation tool. Generate separate production images, one tool call per
slot, unless the user explicitly asks for a direction board or collage.

## Use this image-role vocabulary

Use role ids as output labels, not rigid templates:

| Role | Meaning |
|---|---|
| `MAIN-01` | Search/exposure first image; may be clean or selling-point-led depending on current platform/category rules |
| `WHITE-01` | Compliance-oriented white-background image; product truth dominates and decoration is normally absent |
| `CAR-02` | Core benefit / conversion hook |
| `CAR-03` | Structure, function, material, or mechanism proof |
| `CAR-04` | Size, fit, capacity, compatibility, or model guide |
| `CAR-05` | Lifestyle/use scenario |
| `CAR-06` | Detail, texture, workmanship, or safety proof |
| `CAR-07` | Usage steps, comparison, package contents, or service proof when valuable |
| `SKU-01` | Attribute image for one exact SKU/variant |
| `DET-01...08` | Detail-page modules arranged as a conversion story |
| `CAM-01` | Event/campaign/ad placement creative; never assume ordinary listing rules apply |

Do not map “详情图” to `CAR-06`. “详情图/详情页/长图” means `DET` modules unless
the user explicitly asks for a carousel detail close-up.

## Step 1 — Read inputs and protect product truth

Inspect every supplied product and reference image before planning. Extract:

- product category, materials, colours, shape, size, brand markings;
- included quantity, accessories, packaging, SKU differences;
- visible mechanisms, interfaces, texture, construction, and safety details;
- current product state: folded/unfolded, open/closed, assembled/packed,
  filled/empty, on/off, installed/uninstalled;
- exact user-provided specs, proofs, target buyer, scene, and style constraints.

Preserve the observed product state and geometry. Do not invent hinges,
accessories, colours, ports, ingredients, packaging, effects, or a more extreme
folded/expanded state. Do not turn a visual estimate into an exact specification.

Classify each statement before using it:

- **Verified fact**: visible in the source or supplied with documentary support.
- **User claim**: supplied by the user but not independently verified; may be
  used as copy only when it is lawful and not presented as third-party proof.
- **Inference**: useful for art direction but never displayed as a factual spec.
- **Missing**: omit, mark for confirmation, or use a neutral placeholder in a
  plan; never invent it.

Prefer a real product photo or faithful cutout for `WHITE-01`, `SKU-01`, exact
colour/finish claims, regulated products, and any image where small geometry
differences affect purchase. AI may create the environment and supporting
composition; it must not redesign the sellable item.

## Step 2 — Resolve platform and current rules

Determine target platform, category, image role, placement, and device. If the
user says only “国内电商”, create a **platform-neutral master direction** and
state that exact upload compliance still needs platform/category verification.

For final platform-specific work:

1. Prefer a current screenshot or field constraints from the user's merchant
   publishing page.
2. Otherwise browse the current official platform rule centre, publishing
   schema, or official API documentation.
3. Apply the most specific current category or campaign rule.
4. Record source, date checked, aspect ratio, pixel/file constraints, allowed
   text, background rule, image count, and unresolved items.

Never promise “可直接上传” from memory or a generic online size table. Rules
change by platform, category, account, publishing flow, and campaign placement.
If live verification is unavailable, use a conservative master layout and label
the result “视觉稿，上传前需后台复核”.

## Step 3 — Research category and competitors

When browsing is available and the user asks for platform direction, competitor
reference, top listings, or conversion improvement, inspect 3-5 current examples
from the same platform and category. Prefer:

1. user-provided links or screenshots;
2. top organic/mature brand listings in the exact category;
3. adjacent keywords on the same platform;
4. brand sites or other retailers only as supplementary context.

Inspect the whole path, not only the first image:

- search-result first-image pattern and crop;
- carousel order, text density, proof type, and model/SKU clarity;
- first 3-5 detail-page screens and narrative rhythm;
- repeated buyer objections and missing proof;
- platform UI overlays that may cover text or product.

Separate **category grammar** from **desired positioning**. A search page may be
dominated by promotion-heavy, oversized-copy images while the user is building
a premium flagship-store listing. Learn the category's product scale, click
logic, and proof devices, but let an explicit direction such as “高端、大气、
旗舰店、品牌感” override the category-average decoration style. In that case,
apply the premium flagship preset in the strategy reference and reject outdated
stacked-photo, red-ribbon, coupon-card, and badge-wall treatments.

Extract strategy, never proprietary expression. Do not copy exact wording,
layout, icons, colour system, model pose, background, data, or brand elements.

For a brand system, separate **fixed recognition assets** from **flexible creative
assets**. Keep logo zone, type family, accent logic, and trust-rail grammar
consistent; vary composition, people, camera, environment, proof event, and copy
viewpoint by product. Do not confuse brand consistency with one repeated template.

Choose colour and type sources in this order:

1. user-supplied brand guide, assets, or explicit theme;
2. current official brand site or store system;
3. colours physically present on the exact product/SKU;
4. a named generic preset offered as a choice.

Competitor colours are evidence of category grammar, never permission to replace
the user's brand. Record the palette source and exact tokens before prompting.

## Step 4 — Build the decision map

Write a compact internal map before prompts:

1. **Buyer**: who buys, for whom, and in what situation?
2. **Decision**: what must they understand in 1 second, 5 seconds, and before
   purchase?
3. **Concern**: fit, authenticity, function, material, comfort, safety,
   compatibility, quantity, installation, service, or value.
4. **Claim**: the buyer-facing conclusion.
5. **Proof**: product action, visible structure, exact spec, test/certificate,
   comparison, scale, scene, package contents, or service term.
6. **Best role**: first image, carousel, SKU image, or detail module.

Merge related facts by decision logic:

- claim + material/structure proof;
- mechanism + applicable range;
- size/capacity + real scale context;
- comfort/safety + contact-point detail;
- SKU difference + included quantity;
- service promise + exact conditions.

Do not make one image per raw parameter. Do not repeat the same proof in three
different roles merely with new icons.

## Step 5 — Plan the image set

For every selected image, define:

- role id and platform/placement;
- one-sentence core viewpoint;
- buyer question answered;
- visual proof that works before reading text;
- product/person relationship and correct physical contact;
- foreground, middle ground, background, and reserved text zone;
- exact Chinese headline and 0-3 support labels, or intentionally no text;
- dynamic device: action, before/after, range, scale, process, pressure/contact,
  connected close-up, or variant comparison;
- output ratio/size source and safe-zone assumptions;
- negative constraints and unresolved claims.

Every image must pass:

- **One conversion thesis**: a buyer can summarize it in one sentence. The
  image may contain 2-3 short supporting proof points when they all reinforce
  that thesis; “one idea” does not mean “only one line of text”.
- **One proof event**: something is being shown, compared, used, measured, or
  explained; product plus floating badges is not enough.
- **A distinct job**: it changes a buyer decision not already handled elsewhere.
- **Thumbnail clarity**: product and conclusion survive a small mobile preview.
- **Truth alignment**: copy, proof, SKU, and visible product all agree.

## Step 6 — Write generation prompts

Each prompt must include all of the following:

```text
Platform and role: [platform] [role id] [placement]
Output: [verified ratio/size or conservative master], mobile-first safe zones
Visual tier: [value-led / technical / premium flagship / supplied brand system]
Concept family: [sports editorial / engineering luxury / architectural product / other]
Theme preset: [theme id, exact palette, accent ratio]
Information density: [editorial / conversion / technical]
Brand constants: [logo zone, type family, accent rule, trust-rail grammar]
Creative variables: [camera, action/person, lighting, environment, proof device]
Product truth: use supplied product images as exact visual reference; preserve
shape, colour, proportions, state, branding, quantity, and included parts
Core viewpoint: [one buyer-facing conclusion]
Visual proof: [action/mechanism/scale/detail/comparison/process]
Composition: [foreground / middle / background / product scale / camera angle]
Text system: [exact Chinese copy or no text], [placement, hierarchy, background]
Copy stack: [headline], [0-3 supporting proof points], [optional verified number]
Style: [brand/category/platform direction], commercially credible photography
Negative constraints: [unsupported claims, distortions, artifacts, forbidden
elements, wrong SKU, copied competitor devices]
```

Add this truth constraint to every product-generation prompt:

> Use the supplied product photo as the exact sellable-item reference. Preserve
> product geometry, state, colour, materials, logos, SKU quantity, and included
> accessories. Do not invent or remove functional parts.

For sets, vary composition and text systems deliberately. Mix product-led hero,
technical proof, real scenario, macro detail, scale/fit, process, and package/SKU
clarity as relevant. Avoid consecutive images that all use a centred product,
large headline, four icons, and the same colour card layout.

## Step 7 — Handle Chinese text safely

Use simplified Chinese by default. Keep visible copy concrete and short:

- headline: preferably 4-12 Chinese characters;
- support labels: 2-8 characters each;
- exact numbers and units: copy verbatim;
- avoid punctuation-heavy slogans and paragraph text in carousel images.

Choose a text workflow:

- **Fast visual draft**: render only short Chinese copy directly in the image,
  then inspect every glyph, number, unit, price, and qualifier.
- **Production-safe final**: generate a clean visual base with reserved text
  zones, then use deterministic typesetting when available. This is preferred
  for prices, legal qualifiers, certifications, ingredient/spec tables, and any
  copy where one wrong character changes meaning.

If generated text is garbled or inaccurate, do not call the asset final. Remove
the broken text and regenerate, or typeset it deterministically. Never solve
legibility by making a required qualifier tiny or low-contrast.

## Step 8 — Generate and inspect

Before tool calls, show the user the selected roles, assumptions, omitted weak
roles, and any compliance caveat. Then:

- call image generation once per required production image;
- pass all product/reference images needed for consistency;
- do not combine a requested set into one collage;
- reuse existing context for a single-slot revision;
- inspect output for product identity, anatomy, hands, reflections, shadows,
  text, units, SKU quantity, claim/proof alignment, and platform safe zones;
- regenerate only the failed image, not the whole set.

If the image-generation tool requires no text after generation, place all notes
and warnings before the first call and end after the final image call.

## Detail-page module sequence

Use a modular story, not one endlessly repeated banner:

- `DET-01` — value/brand hero: product, target scene, and one clear promise;
- `DET-02` — pain point to solution: meaningful contrast, not fake drama;
- `DET-03` — core benefit with visible action or result;
- `DET-04` — structure/material/mechanism proof with connected details;
- `DET-05` — use cases or target users in separated, plausible scenes;
- `DET-06` — model/SKU/size/fit/compatibility guide;
- `DET-07` — steps, installation, care, package, or service when useful;
- `DET-08` — trustworthy close: documented credentials, brand/service terms, or
  purchase checklist; skip when there is no real proof.

Default to 5-8 modules. The first 3 modules should answer identity, main benefit,
and proof; do not spend the opening screens on brand poetry or generic lifestyle.

## Compliance gate

Before final output, reject or qualify:

- invented prices, discounts, stock, gifts, delivery, or campaign deadlines;
- “国家级/最高级/最佳/第一/顶级” and near-equivalents without a clearly valid,
  supportable context;
- medical, health, food, cosmetic, safety, environmental, load, durability,
  sales-volume, patent, certification, or test claims without adequate evidence;
- misleading before/after, fake test scenes, impossible effects, false scale, or
  materially different product geometry;
- competitor logos, denigration, unlicensed IP, celebrity likeness, copied
  packaging, watermarks, QR codes, phone numbers, or off-platform contact;
- dynamic qualifiers hidden in tiny low-contrast text;
- removal or concealment of required AI-generated-content metadata/labels.

Platform approval is not legal approval. Platform rejection is not the only risk.

## Quality checklist

- [ ] Correct platform, category, placement, and image role resolved
- [ ] Current rules verified or caveat stated
- [ ] Product/SKU state, geometry, colour, quantity, and accessories preserved
- [ ] Facts separated from user claims and inferences
- [ ] One buyer decision and one visual proof per image
- [ ] Copy density fits the platform/category; premium does not become information-empty
- [ ] Theme id, palette, accent ratio, type system, and layout family are explicit
- [ ] Direction exploration varies at least five creative axes, not only colour
- [ ] Brand constants stay recognisable while product-specific visual events change
- [ ] Palette source is recorded; competitor colour has not overridden the brand
- [ ] Platform adaptation changes hierarchy, not only canvas size
- [ ] Explicit premium/flagship direction overrides mass-market category-average decoration
- [ ] Premium assets use restrained composition, material, light, and typography—not red ribbons, stacked cards, badge walls, or automatic black-gold styling
- [ ] Main image, white-background image, SKU image, carousel, and detail page not confused
- [ ] Chinese copy short, exact, legible, and not rendered with broken glyphs
- [ ] Price/promotion/certification/comparison claims have source and conditions
- [ ] No absolute, medical, deceptive, infringing, or off-platform claims
- [ ] Set uses varied compositions and avoids template repetition
- [ ] Weak or repetitive slots skipped with reason
- [ ] Separate production images generated for a requested set
- [ ] Final assets inspected on the real affected path before claiming completion

## Common mistakes

| Mistake | Corrective rule |
|---|---|
| Translating an Amazon image set into Chinese | Rebuild around domestic platform role, mobile hierarchy, buyer decision, and category norms |
| Treating “主图” as one universal asset | Resolve exposure, white-background, carousel-first, and campaign roles separately |
| Applying one fixed platform size table forever | Verify the current merchant field/category rule and record the source/date |
| Resizing one design for four platforms | Preserve product truth but redesign hierarchy, crop, proof, and text density |
| Filling images with price and badges | Use price only when current, supplied, requested, and legally/platform appropriate |
| Treating “高端” as black-gold, red banners, or more effects | Build premium value through product scale, architectural space, controlled light, restrained colour, precise typography, and credible proof |
| Treating “高端” as one vague headline in empty space | Use one conversion thesis plus 2-3 concise, evidence-backed support points when the category requires fast comparison |
| Picking colours independently for every image | Choose a named theme preset and keep its palette, accent ratio, typography, and proof-rail logic across the set |
| Calling three palette swaps “creative directions” | Change subject/action, crop, light, type composition, proof device, and copy viewpoint |
| Repeating one branded template across every SKU | Fix the recognition layer; vary the product story and visual event |
| Blindly copying the dominant search-page style | Preserve the category's click logic while designing to the requested brand position |
| Generating exact products from imagination | Use real product references; synthesize scene, not sellable-item identity |
| Rendering long Chinese text inside AI images | Keep copy short or use deterministic post-typesetting |
| Making long details as repeated banners | Build a varied module narrative with proof and decision progression |
| Copying a competitor that converts well | Transfer the communication principle, then create an original composition |
