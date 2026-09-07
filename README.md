
The important distinction is that you're cataloguing **publicly available posts and their reported consequences**, not storing the videos themselves.

A good structure would be:

### Balai Rempit — Core catalogue

| Field                   | What to record                                            |
| ----------------------- | --------------------------------------------------------- |
| Record ID               | BR-0001                                                   |
| Date discovered         | When you found the post                                   |
| Incident date           | Date of the actual incident, if known                     |
| Social media platform   | TikTok / Facebook / X / Instagram / etc.                  |
| Account                 | Public account name                                       |
| Post URL                | Link to original post                                     |
| Post description        | Neutral description of what is shown                      |
| Location                | State / district / road, if reliably known                |
| Incident type           | Racing / accident / dangerous riding / disturbance / etc. |
| Motorcycle              | Model, manufacturer, or category                          |
| Rider count             | Number visible/mentioned                                  |
| Other vehicles          | Cars, lorries, motorcycles, etc.                          |
| Accident description    | What happened, without speculation                        |
| Police action           | Arrest / summons / investigation / seizure / unknown      |
| Casualties              | Injured / deceased                                        |
| Property damage         | Vehicles/property damaged                                 |
| Estimated loss          | RM amount, **if supported by a source**                   |
| Source for consequences | Police statement / news / official agency                 |
| Evidence confidence     | High / Medium / Low                                       |
| Notes                   | Additional information                                    |

### 1. You need a **source hierarchy**

This is particularly important.

Don't treat a TikTok caption saying *"5 people injured"* as equivalent to a police statement.

I'd use:

**Level 1 — Official**

* PDRM
* JPJ
* Fire and Rescue Department
* Ministry/municipal authorities
* Court documents

**Level 2 — Established news organisations**

**Level 3 — Original social-media post**

**Level 4 — Secondary reposts / comments**

Then your sheet can have:

> **Casualty source: Level 1 — PDRM statement**

rather than simply recording an unverified number.

---

## 2. Methodology for determining "kerugian"

This needs to be very strict.

Don't invent a number based on what the vehicle looks like.

For example:

> Car appears badly damaged → RM20,000 loss

wouldn't be defensible.

Instead, classify it:

**A. Reported financial loss**

A source explicitly says:

> Estimated damage RM15,000.

Record:

`RM15,000 — reported by [source]`

**B. Known repair/insurance value**

If a reliable source provides a repair estimate, record it.

**C. Damage observed but no monetary value**

Record:

> `Vehicle severely damaged — monetary loss unknown`

**D. Economic impact**

Keep this separate from direct property damage.

For example:

* vehicle damage
* road infrastructure damage
* medical treatment
* lost working time
* towing/recovery

Unless you have a defensible methodology for calculating these, don't convert them into RM.

That prevents **Balai Rempit** from producing fake precision.

---

## 3. Motorcycle identification methodology

I'd create a hierarchy here too.

### Manufacturer + model known

> Yamaha Y15ZR

**Confidence: High**

### Manufacturer known, model uncertain

> Yamaha — underbone motorcycle, model unidentified

**Confidence: Medium**

### Only visual category identifiable

> Underbone motorcycle

**Confidence: Low**

### Don't know

> Motorcycle — model unidentified

Don't guess the model from a blurry video.

You could eventually have a separate field:

`Motorcycle identification confidence`

with:

* High
* Medium
* Low
* Unknown

---

## 4. Accident description methodology

This should be **descriptive rather than accusatory**.

Instead of:

> "Mat rempit rider recklessly crashed into innocent car."

Use:

> "A motorcycle travelling alongside several motorcycles appears to collide with a sedan. The motorcycle subsequently falls onto the roadway. Two people are reported injured."

Separate **what the video shows** from **what authorities report**.

For example:

**Visual observation**

> Motorcycle appears to lose control and fall.

**Official information**

> PDRM reported that the rider was arrested and investigated under [relevant law].

That separation is extremely valuable for the credibility of the project.

---

## 5. I would add an "Impact" framework

Rather than just:

> Impact: 5 casualties

use categories:

### Human impact

* Fatalities
* Serious injuries
* Minor injuries
* Number of people affected

### Vehicle impact

* Motorcycle damaged
* Car damaged
* Multiple vehicles damaged
* Total vehicles involved

### Infrastructure impact

* Road furniture
* Barriers
* Signs
* Buildings
* Other property

### Public impact

* Road closure
* Traffic disruption
* Noise complaint
* Public safety concern

### Enforcement impact

* Arrest
* Summons
* Investigation
* Vehicle seizure
* Court action
* No official action reported

This will eventually make your spreadsheet much more useful for analysis.

---

## 6. One very important field: **"Claim vs Verified Fact"**

I'd actually make this mandatory.

For every significant claim:

| Claim        | Source             | Verification |
| ------------ | ------------------ | ------------ |
| 5 injured    | TikTok caption     | Unverified   |
| 5 injured    | PDRM statement     | Verified     |
| RM30k damage | Facebook comment   | Unverified   |
| RM30k damage | Police/news report | Verified     |

This protects the project from becoming a collection of viral claims.

---

### So the overall structure becomes

**BALAI REMPIT**

**Purpose:**

> A public-data catalogue documenting incidents associated with illegal street riding, their consequences, and enforcement responses in Malaysia.

**Data collection begins:**

> **7 September 2026**

**Pipeline:**

```text
PUBLIC SOCIAL MEDIA POSTS
          │
          ▼
     FIND INCIDENT
          │
          ▼
   CREATE RECORD
          │
          ├── Source
          ├── Date
          ├── Location
          ├── Motorcycle
          ├── Incident
          └── Video description
          │
          ▼
   VERIFY CONSEQUENCES
          │
          ├── Police
          ├── News
          ├── Authorities
          └── Other sources
          │
          ▼
      IMPACT DATA
          │
          ├── Casualties
          ├── Vehicle damage
          ├── Property damage
          └── Economic loss
          │
          ▼
     CONFIDENCE SCORE
          │
          ▼
       GOOGLE SHEET
          │
          ▼
    FUTURE BALAI REMPIT
        APPLICATION
```

