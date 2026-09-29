# GAPS: fields not verified from a primary source (left null)

Checked 2026-09-28. Blocked pages: garmin.com product/support pages (403 or client-rendered, unreadable), stagescycling.com (403), jetblackcycling.com product pages (403), elite-it.com prices (not in page HTML).

- **wahoo-kickr-v6**: noiseClaim
- **wahoo-kickr-core-2**: flywheel, noiseClaim
- **wahoo-kickr-rollr**: noiseClaim
- **wahoo-kickr-bike-shift**: flywheel, noiseClaim
- **wahoo-kickr-bike-pro**: flywheel, noiseClaim, weight
- **tacx-neo-3m**: minSimulatedGradientPct, noiseClaim, weight, maxRiderWeight, connectivity
- **tacx-neo-2t**: claimedPowerAccuracy, maxPowerW, maxSimulatedGradientPct, minSimulatedGradientPct, flywheel, noiseClaim, weight, maxRiderWeight, connectivity, price
- **elite-justo-2**: minSimulatedGradientPct, noiseClaim, maxRiderWeight, price
- **elite-avanti**: minSimulatedGradientPct, noiseClaim, maxRiderWeight, price
- **elite-rivo**: minSimulatedGradientPct, noiseClaim, maxRiderWeight, price
- **elite-tuo**: minSimulatedGradientPct, noiseClaim, maxRiderWeight, price
- **saris-h3-plus**: minSimulatedGradientPct, weight
- **wattbike-atom**: flywheel, noiseClaim
- **jetblack-victory**: minSimulatedGradientPct, flywheel, noiseClaim, weight, price. Manufacturer store returned 403 to automated access; DC Rainmaker's review titles it a $399 trainer (secondary, not recorded as price).
- **zwift-ride-kickr-core-2**: flywheel, noiseClaim, weight, maxRiderWeight, connectivity
- **stages-sb20**: claimedPowerAccuracy, maxPowerW, maxSimulatedGradientPct, minSimulatedGradientPct, flywheel, noiseClaim, weight, maxRiderWeight, connectivity, price. Stages product pages returned 403 to automated access.

## Models in scope but not compiled (no primary source could be read)
- Tacx FLUX 2 / FLUX S, Tacx NEO Bike Smart / NEO Bike Plus (Garmin pages blocked)
- Elite Direto XR-T / Suito-T / Zumo (no longer on Elite's current smart-trainer listing on the check date; not verified as discontinued)
- Zwift Hub / Hub One: us.zwift.com/products/zwift-hub-one now serves the Wahoo KICKR CORE 2 with Zwift Cog and Click; Zwift Ride is included via its KICKR CORE 2 bundle
- Wahoo KICKR MOVE: listed 'Discontinued' on Wahoo's page (schema.org availability), so excluded from current set
- Wattbike Atom X / Proton, Saris H4/M2, JetBlack VOLT: not reached in the tool budget
- Independent findings: none found/read for Wahoo KICKR V6, KICKR ROLLR, Elite Justo 2, Elite Rivo; only DC Rainmaker read so far, no GPLama, Shane Miller or BikeRadar findings yet

## Update 2026-09-29
- **Still no price:** jetblack-victory (store gives a bot challenge; reviewers report GBP/USD 399 in Nov 2024 and Jun 2025), stages-sb20 (403; reviewers' prices are from 2022). Not bypassed.
- **Elite prices are euro only** (`priceLocal`); no USD store price was readable. The site's `usd()` helper ignores `priceCurrency`, so these records keep `price: null` on purpose.
- **Findings thin or missing:** elite-avanti (DC Rainmaker only), elite-justo-2 (The Triathlete UK repeats the claim rather than measuring), elite-tuo (Cycling Weekly may have reviewed a newer variant; only its accuracy comments are used), saris-h3-plus (predecessor H3 only), zwift-ride (no power numbers in the reviews read). GPLama and Shane Miller had no page found for these current models.
- **Not readable in full:** Cyclingnews (KICKR Bike Shift, Bike Pro, NEO 3M, Justo 2, Zwift Ride) and Velo/Triathlete (login redirect). Search snippets were not used as findings.
- **Zwift Hub:** the Zwift store's Hub One page now sells the KICKR CORE 2 with Zwift Cog and Click, already covered by the Core 2 and Zwift Ride bundle records; no separate Hub record was added.
- **apps.json:** Zwift and Wahoo platform lists not confirmed; MyWhoosh subscription price not published on the pages read.
- Unfilled spec fields from the earlier pass (noise claims, several flywheel and weight values) remain null.
