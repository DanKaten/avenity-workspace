# Verified Website, Schema, and Listings Corrections

**Evidence reviewed:** July 30, 2026

This register contains only discrepancies observed on live pages or in live structured data. It does not include theoretical checks.

## 1. Avenity Business Solutions homepage: incorrect geographic coordinates

**Page:** https://avenitybusinesssolutions.com/
**Location:** `ProfessionalService` JSON-LD

The schema declares the correct Montgomery, Texas address but supplies:

```json
"latitude": 40.0641205,
"longitude": -83.0675592
```

Latitude 40 and longitude -83 are not in Montgomery, Texas. Replace them with the coordinates for the declared business location or remove the `geo` node until the correct coordinates are available.

## 2. Avenity Business Solutions homepage: two disconnected organization descriptions

**Page:** https://avenitybusinesssolutions.com/

The homepage emits:

- a `ProfessionalService` entity with no `@id` and an empty `sameAs` array; and
- a separate `Corporation` entity with `@id` `https://avenitybusinesssolutions.com#Organization` and three social profiles.

These describe the same company but are not joined by a shared identifier. Assign the same stable organization `@id` to the business entity or consolidate the overlapping organization nodes. Preserve the existing official Facebook, LinkedIn, and Instagram URLs.

## 3. Avenity Business Solutions homepage: invalid aggregate-rating scale

**Page:** https://avenitybusinesssolutions.com/
**Location:** `aggregateRating` JSON-LD

The schema currently declares:

```json
"ratingValue": "5.0",
"bestRating": 5,
"worstRating": 5
```

For a five-point rating scale, `worstRating` should be `1`, not `5`.

## 4. Avenity Mercantile homepage: visible content does not match the stated role

**Page:** https://avenitymercantile.com/

Avenity Mercantile is the standard-marketing side of the business for clients who do not want AI-related marketing. The live homepage instead leads with:

- “AI Visibility, GEO & AEO Services in Montgomery, TX”
- the AI Visibility Authority Engine;
- ChatGPT, Google AI Overviews, and Perplexity; and
- Avenity Business Solutions as the primary service identity.

Replace the homepage positioning with Avenity Mercantile’s actual traditional services: Google Ads, Meta Ads, TikTok Ads, paid social, traditional SEO, website support, lead generation, and reporting. Link to Avenity Business Solutions as the related AI-visibility service rather than using ABS as the Mercantile homepage’s primary identity.

## 5. Avenity Mercantile homepage: conflicting organization names for one `@id`

**Page:** https://avenitymercantile.com/
**Shared identifier:** `https://avenitymercantile.com/#organization`

Three JSON-LD blocks use the same organization `@id` but give it different names:

1. `Strategic Growth For Your Business`
2. `Avenity Mercantile`
3. `Avenity Marketing`

The third block also uses `Avenity Business Solutions` as the alternate name, while the first WebSite node is named `Avenity Business Solutions - Strategic Growth For Your Business`.

Use `Avenity Mercantile` as the organization and WebSite name for this domain. Consolidate or remove the duplicate generated nodes so the same `@id` does not identify three different names.

## 6. Avenity Mercantile homepage: conflicting founder definitions

**Page:** https://avenitymercantile.com/

Two schema blocks define founders differently for the same organization `@id`:

- one identifies Andrea Katen as founder; and
- another identifies Daniel Katen and Andrea Katen.

Publish one authoritative founder definition for the Mercantile entity and use it consistently.

## 7. Avenity Mercantile homepage: inconsistent official-profile connections

**Page:** https://avenitymercantile.com/

The three organization blocks contain different `sameAs` sets, including:

- `/avenitymercantile/` and `/avenitybusiness` Instagram destinations;
- a Facebook share link in one block and a canonical Facebook page in another; and
- different LinkedIn and YouTube coverage.

Use one merged list of canonical, official profile URLs on the authoritative `Avenity Mercantile` organization node.

## 8. Conroe/Lake Conroe Chamber listing: conflicting main telephone number

**Listing:** https://www.chamber.conroe.org/list/member/avenity-business-solutions-5200879

The business header displays:

```text
(281) 733-5151
```

The Daniel Katen representative section on the same listing displays:

```text
(936) 701-0994
```

The first number is outside the two Avenity-owned numbers identified by the business. Replace the business-header number with the correct current Avenity number.

## 9. Yellow Pages and Superpages: non-Avenity telephone number and closed hours

**Listings:**

- https://www.yellowpages.com/nationwide/mip/avenity-mercantile-571937189
- https://www.superpages.com/nationwide/bpp/avenity-mercantile-571937189

Both listings display:

```text
(832) 422-6727
```

This number is outside the two identified Avenity-owned numbers. The listings also show the business as closed Monday through Sunday. Replace the telephone number and operating hours with the current Mercantile information.

## 10. Yahoo Local: wrong website destination and outdated positioning

**Listing:** https://local.yahoo.com/info-233036553-avenity-business-solutions-montgomery/

The listing is named `Avenity Business Solutions` but points to:

```text
avenitymercantile.com
```

Its description also says ABS:

- focuses exclusively on private-sector industrial firms;
- targets companies with $5M–$30M in revenue; and
- operates in the Houston market.

That description conflicts with the current ABS positioning for local and regional service businesses and the broader documented industry record. Change the destination to `https://avenitybusinesssolutions.com/` and replace the description with the current ABS service scope.

## GitHub-only correction already handled

The schema in `best-ai-visibility-agencies-texas-2026.html` identified Daniel Katen as `Founder and COO`. It has been corrected in the repository branch to `Founder and CEO`. This is not a website or listings task.
