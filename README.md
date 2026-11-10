# London collision map · standalone exploratory viewer

A browser viewer for exploring recorded London collisions and contextual fields.
It supports CSV loading, severity/year filters, feature colouring and map exports.

**For the publication, start with [London Cyclist Crash Severity Prediction](https://github.com/CycleAI/London-Cyclist-Crash-Severity-Prediction).**
That repository contains the paper package, saved results and a [documented
collision viewer](https://github.com/CycleAI/London-Cyclist-Crash-Severity-Prediction/tree/main/visualizations/collision_viewer).
This standalone map is an exploratory companion, not the final model or its evaluation.

## Files

| File | Purpose |
| --- | --- |
| [index.html](index.html) | Leaflet/Mapbox map interface and CSV controls. |
| [final_processed_with_interest.csv](final_processed_with_interest.csv) | Bundled collision/context table for exploratory viewing. |
| [london_boroughs.geojson](london_boroughs.geojson) | Borough boundaries used by the map. |

## Open locally

From this repository's root, run:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/` and use the CSV file picker to load the bundled table.
The viewer expects fields including `latitude`, `longitude`, `collision_year`
and `Severity`. The borough file is loaded from the same directory.

The page uses external JavaScript libraries and map/image providers. Mapbox
features require an appropriate public browser token; provider-dependent features
have not been revalidated as part of this documentation update. Configure your
own service access and do not commit credentials.

These maps describe recorded collisions. They do not estimate an individual
cyclist's crash probability or exposure-adjusted route risk. Do not treat this
table as the final paper cohort; see the paper repository for the analytical data
and interpretation limits.

[CycleAI research catalogue](https://github.com/CycleAI)
