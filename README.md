# UUID4.x

This repository includes the specsheets of both [UUID 4.1]() and [UUID 4.2]().

<p align="center">
  <img src="https://img.shields.io/github/license/TRC-Loop/UUID4.x?style=for-the-badge"/>
  <img src="https://img.shields.io/github/stars/TRC-Loop/UUID4.x?style=for-the-badge"/>
</p>

---

### Comparison

[UUID 4](https://www.ietf.org/rfc/rfc4122.txt) vs UUID 4.1 vs UUID 4.2

| Feature                     | UUID 4 (RFC 4122)                                   | UUID 4.1 (Base‑36)                                 | UUID 4.2 (Base‑62)                                 |
|-----------------------------|-----------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------|
| **Alphabet**                | 0‑9 + a‑f (hex)                                     | 0‑9 + a‑z (36 chars)                               | 0‑9 + a‑z + A‑Z (62 chars)                         |
| **Case‑sensitivity**       | N/A (hex is case‑insensitive)                       | Case insensitive                                    | Mixed case (A‑Z & a‑z)                             |
| **Length**                  | 32 hex chars (8‑4‑4‑4‑12) with hyphens              | 32 chars (no hyphens)                              | 32 chars (no hyphens)                              |
| **Encoding**                | 128‑bit binary → 32 hex digits                     | 128‑bit binary → 32 base‑36 digits                 | 128‑bit binary → 32 base‑62 digits                 |
| **Collision probability**  | 128‑bit entropy → ~10⁻³⁶⁴ for 1 billion IDs         | Same 128‑bit entropy → same collision odds         | Same 128‑bit entropy → same collision odds         |
| **URL‑safe**                | Yes (hex)                                           | Yes (base‑36)                                      | Yes (base‑62)                                      |
| **Hyphens / separators**   | Yes (8‑4‑4‑4‑12)                                     | Yes (7-5-4-4-12)                                                 | Yes (7-6-4-4-11)                                                 |
| **Typical use‑case**        | Standard UUIDs in databases, APIs, file names       | Shorter, all‑lowercase IDs for URLs or short keys | Shorter, case‑sensitive IDs for URLs, tokens       |

### The Idea

**The reason behind UUID4.x:** 
As most systems are mostly not limited by *HEX*, why not extend the **charset** beyond just *HEX (0-f / 0-9 + A-F)*? This is what **UUID4.x** is for. It provides better URL safety and increases the number of possible combinations.


# UUID 4.1

*Short Version of spec* [long version]()

Characters: `0-9 + a-z` / `0123456789abcdefghijklmnopqrstuvwxyz` (36 chars)

Combinations: `6.334 × 10^49` / `63340286662973277706162286946811886609896461828096` / `63 340 286 662 973 277 706 162 286 946 811 886 609 896 461 828 096
` / ≈ 63 quattuordecillion

**Pros**

- Case insensitive

## UUID 4.2

*Short Version of spec* [long version]()

Characters: `0-9 + a-z + A-Z` / `0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ` (62 chars)

Combinations: `2.27 × 10^57` / `2272657884496751345355241563627544170162852933518655225856
` / `2 272 657 884 496 751 345 355 241 563 627 544 170 162 852 933 518 655 225 856` / ≈ 2.3 octodecillion
