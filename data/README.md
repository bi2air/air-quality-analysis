# Data notes

This folder contains the PM2.5, meteorological, NOAA ISD, MERRA-2, and combined CSV files used across the notebooks.

## 2026 AI-assisted modeling update

The 2026 modeling update in `3.3 AI-assisted modeling 2026.ipynb` uses:

- `comb_PM25_wind_Hanoi_2018_v3.csv`

Target:

- `PM2.5`

Original weather-feature model inputs after dropping weak or redundant fields:

- `T2MDEW`
- `T2M`
- `PS`
- `TQV`
- `TQL`
- `H1000`
- `HLML`
- `RHOA`
- `CIG`
- `WS`

Dropped fields in the 2026 modeling update:

- `CLDCR`
- `v_2m`
- `v_50m`
- `v_850`
- `FRCAN`
- `DISPH`

Feature-scope note:

- Weather-only models keep the original meteorological prediction task.
- Timestamp features add hour/day/season information.
- Lagged PM2.5 and rolling PM2.5 features require recent observed PM2.5, so those results should be described as short-horizon forecasting or nowcasting rather than pure weather-only prediction.
