RideLog V6.1 – Statistics, Home Battery Ring and Compact Date Selector
================================

This is an enhancement of the supplied RideLog V5 project. The V5 source ZIP was not modified.

Included files
- index.html: existing app interface with upgraded Statistics screen
- app.js: monthly/yearly analytics, per-vehicle and combined views, monthly/yearly print-to-PDF reports
- sw.js: V6 offline cache name
- manifest.json and icon.svg: app installation metadata/assets

Data preservation
- The existing localStorage key `ridelog_v2` is intentionally unchanged.
- If you deploy these files at the same website address/origin and use the same browser, the app should continue reading the existing RideLog data.
- Before replacing V5, use Profile > Export all vehicle data and keep the JSON backup safely.
- If you test V6 at a different website address/origin or in another browser/device, local browser data will not automatically move; use Profile > Import backup there.
- Keep the original V5 ZIP as a rollback copy.

V6.1 additions
- Monthly summary: distance, energy, charging cost, efficiency, ride count and estimated savings.
- Yearly summary and month-by-month distance chart.
- Best and lowest efficiency months for the selected year.
- Statistics can be viewed separately for each vehicle or in a third Combined view. The selection applies to charts and monthly/yearly PDF reports.
- Home screen has one two-colour battery ring: remaining battery and used battery, with only the last-charge date beside it.
- Log Ride uses compact day, month and year selectors instead of the large native calendar picker.
- Monthly and yearly report generation using the browser print dialog (choose Save as PDF).
- Historical ride energy values are no longer recalculated and overwritten on every app render.

Calculation note
Distance is calculated from chronological odometer readings for each vehicle independently. As in V5, the first saved odometer reading is treated as distance from zero because V5 does not store a separate starting odometer. Petrol-equivalent cost and savings are estimates based on each vehicle's saved petrol mileage and ride petrol price; they are not measured fuel savings.

Basic checks performed
- JavaScript syntax check passed.
- All statically referenced app element IDs were found in index.html.
