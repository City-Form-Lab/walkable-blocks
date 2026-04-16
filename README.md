# Walkable Block Size Calculator

An interactive, browser-based calculator that determines the urban block size that maximizes pedestrian accessibility to all surrounding parcels within a given walkshed distance. Companion tool for:

> Sevtsuk, A. (2026). *Are Smaller Blocks More Walkable? Testing the Nonlinear Relationship Between Urban Block Size and Pedestrian Travel.*

**[Launch the Calculator →](https://asevtsuk.github.io/walkable-blocks/)**

## What It Does

Given parcel and street dimensions, this tool computes which block size (measured in plots per frontage) maximizes pedestrian accessibility using a Hansen gravity-based model. It tests a range of block sizes and identifies the one that best balances route efficiency against street-crossing costs.

The calculator also produces:
- An interactive **gravity curve** showing mean accessibility across all tested block sizes
- A **block grid visualization** depicting the optimal layout with streets, parcels, and entrance points

## Background

The conventional planning wisdom holds that smaller blocks are always better for walkability. This tool demonstrates why that isn't necessarily true: while shorter blocks create more intersections and route choices, they also introduce more frequent street crossings and reduce parcel density within a fixed walking radius. The result is a nonlinear, parabolic relationship where both excessively small and excessively large blocks reduce accessibility.

The optimal block size depends on local conditions — parcel frontage, parcel depth, street widths, and willingness to walk.

## Parameters

| Parameter | Description | Default |
|-----------|-------------|---------|
| Plot Frontage | Width of each parcel along the street (m) | 15 |
| Plot Depth | Depth of each parcel perpendicular to street (m) | 30 |
| Street Width X | Width of horizontal streets (m) | 15 |
| Street Width Y | Width of vertical streets (m) | 15 |
| Beta | Distance decay (willingness to walk) | 0.005 |
| Search Radius | Maximum walking distance (m) | 1000 |

## How to Use

1. Enter your parcel and street dimensions
2. Optionally adjust beta and search radius under "Advanced Parameters"
3. Click **Compute Optimal Block Size**
4. Explore the Block Grid and Gravity Curve tabs

## Running Locally

This is a single-file HTML application with no build step or dependencies. Simply open `index.html` in any modern browser.

## References

- Sevtsuk, A., Kalvo, R., & Ekmekci, O. (2016). Pedestrian accessibility in grid layouts: The role of block, plot and street dimensions. *Urban Morphology*, 20(2). [doi:10.51347/jum.v20i2.4056](https://doi.org/10.51347/jum.v20i2.4056)

## License

MIT
