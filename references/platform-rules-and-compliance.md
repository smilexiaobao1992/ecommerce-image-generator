# Platform Rules and Compliance

Use this reference for platform-specific, upload-ready, regulated, promotional,
comparison, certification, price, or final AI-generated-image work.

## Contents

- Rule hierarchy and verification record
- Verified platform research snapshot
- Chinese legal baseline
- Regulated and high-risk categories
- Promotion and price gate
- Final compliance status

## Rule hierarchy

Use the most specific current source available:

1. Current merchant publishing field for the exact account, category, and slot
2. Current category/campaign rule in the platform merchant rule centre
3. Current official publishing schema or API documentation
4. Current general platform rule
5. Third-party guides only as discovery aids, never final authority

Record the source and check date. If official sources conflict, prefer the rule
shown in the exact publishing flow. Do not claim upload readiness when the only
source is a blog, training article, old screenshot, or memory.

## Verification record

Capture this before final platform output:

```text
Platform:
Account/store type:
Category:
Placement/slot:
Device/publishing flow:
Rule source URL or screenshot:
Checked on:
Aspect ratio:
Pixel range:
File type/size:
Image count:
Background requirement:
Text/logo/promotion allowance:
Required content or labels:
Unresolved items:
```

## Verified research snapshot — 2026-07-14

This snapshot is evidence for workflow decisions, not a permanent export preset.

### Taobao and Tmall

The official Taobao Open Platform announcement dated 2024-01-26 states that the
new product publishing flow validates 1:1 images in the 1:1 field and 3:4 images
in the 3:4 field, with category rollout, and recommends prioritising 1:1 for the
new detail experience. It also states that Taobao and Tmall use the same image
upload interfaces in this change.

Official source:
https://developer.alibaba.com/support/announcementDetail.htm?id=25721

The official `taobao.item.img.upload` API documentation states that ordinary
product image upload supports JPG/JPEG/PNG, has a 3 MB API field limit, and has
an `is_rectangle` flag for 3:4 product images. It explicitly notes that image
quantity and size restrictions may vary with the seller's enabled services.

Official source:
https://developer.alibaba.com/docs/api.htm?apiId=23&scopeId=12166

Operational consequence:

- Do not say “Taobao/Tmall only accepts square images.”
- Do not assume one global image count or one universal white-background rule.
- Resolve the current 1:1/3:4 field, category, store type, and image role.

### JD

JD's rule centre and merchant open platform are dynamic JavaScript services; the
exact product/category rule may not be available to anonymous text crawlers.
Use the current merchant publishing page or the current rule centre for the
exact category and placement rather than copying a generic 800 px rule from a
third-party guide.

Official entry points:

- https://rule.jd.com/
- https://open.jd.com/
- https://jos.jd.com/

Operational consequence:

- Treat a clean product-led or white-background first image as a conservative
  design direction, not a universal legal claim.
- Verify whether text, logos, background, image count, PC/mobile detail width,
  and file limit differ for self-operated, POP, category, and campaign flows.

### Pinduoduo

Pinduoduo merchant rules and product publishing constraints are account- and
category-facing. Use the merchant backend's current rule centre and publishing
fields; do not rely on articles that label a generic size list “official”.

Official entry points:

- https://mms.pinduoduo.com/other/rule
- https://open.yangkeduo.com/
- https://www.yangkeduo.com/home/help/

Operational consequence:

- Resolve main image, carousel, SKU image, white-background image, and detail
  image as separate fields when the publishing flow distinguishes them.
- Never imply that the lowest displayed price buys the pictured SKU unless the
  exact SKU, quantity, and conditions match.
- Avoid QR codes, phone numbers, external shop names, and off-platform contact
  unless the current platform rule and placement explicitly allow them.

## Chinese legal baseline

This is an execution checklist, not legal advice.

### Truthful product disclosure

Article 17 of the E-Commerce Law requires ecommerce operators to disclose
product/service information comprehensively, truthfully, accurately, and
promptly, and prohibits false or misleading commercial promotion.

Official source:
https://www.samr.gov.cn/zfjcj/tzgg/art/2023/art_d337c3291e8b40459ca03dea54395856.html

Apply it visually:

- pictured SKU, quantity, colour, accessories, scale, and function must match;
- qualifiers that affect a purchase cannot be hidden or contradicted by the hero;
- a scene must not imply included furniture, gifts, or accessories without a
  clear and sufficiently visible distinction.

### Internet advertising

The Internet Advertising Measures apply to online commercial promotion using
text, images, audio, video, or other formats, and require advertising to be true,
lawful, and recognisable where applicable.

Official source:
https://www.samr.gov.cn/zw/zfxxgk/fdzdgknr/fgs/art/2023/art_d93a579afd45413e8576e4623fab348f.html

### Absolute and ranking language

The official enforcement guide identifies “国家级”, “最高级”, “最佳”, and
equivalent or similar expressions as absolute language under Article 9(3), while
also describing context-specific exceptions. Do not use a prohibited-looking
claim merely because an exception might exist; require a clear factual basis and
valid context.

Official source:
https://www.samr.gov.cn/ggjgs/tzgg/art/2023/art_183b5cb48d9e4f0dba67f9f912a913ba.html

Reject by default:

- 全网第一、行业第一、销量第一、国家级、最高级、最佳、顶级、唯一;
- zero-risk/permanent/100% claims that cannot be proven under all stated conditions;
- unsupported “专利技术”, “权威认证”, “官方推荐”, “医用级”, or test results.

### Qualifiers and small print

Current 2026 market-regulation guidance highlights the risk of attracting with
large claims while materially limiting them through weak, tiny, or hard-to-read
qualifiers. Keep important conditions close to the claim, legible, and visually
proportionate.

Official source:
https://www.samr.gov.cn/ggjgs/tzgg/art/2026/art_23fa8f1eaa5546af86528157fbc85db5.html

Apply it to:

- price thresholds, coupon conditions, member-only prices, limited regions;
- measured performance, test environments, model compatibility, capacity;
- “effect image”, “scene image”, “accessory not included”, and colour variation.

### AI-generated-content identification

China's Measures for Labelling AI-Generated or Synthesised Content and the
supporting mandatory national standard took effect on 2025-09-01. They cover
explicit and implicit identification and prohibit malicious removal, tampering,
forgery, or concealment of required labels.

Official source:
https://www.cac.gov.cn/2025-03/14/c_1743654685899683.htm

Execution rules:

- preserve metadata or labels supplied by the generation service;
- do not instruct tools to strip mandatory AI metadata;
- follow the target platform's current upload and display requirements;
- when a generated scene could be mistaken for a real product test, label or
  redesign it so it is not presented as documentary evidence;
- use real photography/documented test assets for regulated or high-stakes proof.

## Regulated and high-risk categories

For medicine, medical devices, health products, food, infant products,
cosmetics, finance, education, pesticides, veterinary products, safety gear,
electrical performance, environmental claims, or other regulated areas:

1. Browse current national law and the exact platform category rule.
2. Require qualification, approval, test, ingredient, or certificate evidence
   before displaying a regulated claim.
3. Match wording, scope, model, issuer, standard, test conditions, and validity.
4. Do not use actors, white coats, lab scenes, charts, or before/after imagery to
   imply proof that does not exist.
5. Escalate uncertain legal claims to the user instead of inventing safe-sounding copy.

## Promotion and price gate

Only display price, discount, coupon, gift, sale count, stock, delivery time, or
campaign timing when the user supplies current facts and requests them.

Record:

- exact SKU/quantity tied to the displayed price;
- original/current price basis and coupon threshold;
- store/member/region/channel restrictions;
- start/end time and timezone;
- gift quantity and “while stocks last” condition when applicable.

Prefer keeping volatile promotion data in editable overlays rather than baking
it into evergreen product renders.

## Final compliance status

Use one of these labels in the pre-generation plan or handoff:

- **规则已核对**: exact current official/backend rule was checked and recorded.
- **视觉方向稿**: platform/category rule was not fully verified; not claimed as upload-ready.
- **待证明**: a claim needs user evidence before it may appear.
- **不采用**: claim or device is deceptive, unsupported, infringing, or too risky.
