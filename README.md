# Neural Network Methods for Gas Storage Valuation

Master's thesis — Mathematics-Economics, Aalborg University (Group M10-01)
Supervisor: Esben Høg | Date: 27 May 2026

A Least Squares Monte Carlo (LSMC) study comparing six continuation value
approximation methods for pricing gas storage as a stochastic control problem,
with application to a stylised Dutch salt cavern and Gas Storage Denmark (GSD).

## Methods compared

| Method | Description |
|--------|-------------|
| OLS | Polynomial basis regression (Laguerre, power, Hermite) |
| Spline | B-spline regression |
| MLP (nodewise) | Multi-Layer Perceptron fitted per inventory node |
| MLP (joint-input) | MLP with price and inventory as joint inputs |
| KAN (nodewise) | Kolmogorov-Arnold Network fitted per inventory node |
| KAN (joint-input) | KAN with price and inventory as joint inputs |

## Repository structure

```
data/
  THE_data.csv                      # TTF/THE spot price history
  THE_gas.txt                       # THE gas price data
  forward_prices.csv                # Forward curve data
  storage_utilization_IR.xlsx       # GSD injection rate utilisation
  storage_utilization_WG.xlsx       # GSD working gas utilisation
  storage_utilization_WR.xlsx       # GSD withdrawal rate utilisation

models/
  MC_OLS_v7.ipynb                   # OLS, stylised cavern
  MC_OLS_v7_GSD.ipynb               # OLS, Gas Storage Denmark
  MC_spline_v7.ipynb                # Spline, stylised cavern
  MC_spline_v7_GSD.ipynb            # Spline, GSD
  MC_MLP_v7.ipynb                   # MLP, stylised cavern
  MC_MLP_v7_GSD.ipynb               # MLP, GSD
  MC_KAN_v7_new_good.ipynb          # KAN (final), stylised cavern
  MC_KAN_v7_GSD_new.ipynb           # KAN (final), GSD
  intrinsic_valuation.ipynb         # Intrinsic value benchmark
  rolling_intrinsic_valuation.ipynb # Rolling intrinsic benchmark
  ...

spot_sim/
  spot_price_sim.ipynb              # Spot price simulation and calibration
  forward_curve_construction.ipynb  # Forward curve construction
  seasonal_component.ipynb          # Seasonal model estimation

GSD_min_max_inventory_constraints.ipynb   # GSD regulatory constraints analysis
GSD_max_storage_capacity.ipynb
GSD_IR_WR_constraints.ipynb
GSD_base_IR_WR_constraints.ipynb
```

## Author

Rasmus Sønder — [soender0201@gmail.com](mailto:soender0201@gmail.com)
Supervisor: Esben Høg, Department of Mathematical Sciences, AAU
