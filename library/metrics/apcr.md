# 🌿 APCr

Data centers can achieve higher sustainability by adjusting their operations to the tune of clean energy production (e.g. load shifting). DC4Cities proposed in 2014 a metric which captures how much the energy consumption profile of a data center matches the availability of renewable and green energy: Adaptability Power Curve at Renewable Energies.

<details>

<summary>Details</summary>

Unit: **NA**

Minimum: **1.0**

Maximum: -**∞**

Ideal: **1.0**

</details>

## Formula

$$
APC_{ren} = 1 - \frac{\sum_{i=1}^{n} |K E_{Ren i} - E_{DC i}|} {\sum_{i=1}^{n} E_{Ren i}}
$$

$$
K = \frac{\sum_{i=1}^{n} E_{DC i}} {\sum_{i=1}^{n} E_{Ren i}}
$$

Where

* _Ereni_ is the renewable energy production on the grid (or onsite) in kWh,
* _EDCi_ is the total energy consumption of the data center in kWh,
* _K_ serves as an adjustment factor to meaningfully compute $E\_{ren i}$ against $E\_{DC i}$,
* _i_ is the time period, and
* _n_ is the sample size

As the amount of renewable electricity on the grid is far higher than what a data center consumes, K is needed to equalize their magnitudes.

## Evaluation

Has not been used in the industry.

## Improvement Strategies

Load shifting.

## Sources

\[1] [Cluster Activities Task 3](https://www.smartcitiescluster.eu/publications/FP7ProjectCluster-NewEnergyEfficiencyMetricsforDataCentres-task3.pdf)

\[2] [Metrics for Assessing Flexibility and Sustainability of Next Generation Data Centers](https://ieeexplore.ieee.org/document/7414182) [\[pdf\]](https://www.researchgate.net/profile/Alexis-Aravanis/publication/286923163\_Metrics\_for\_Assessing\_Flexibility\_and\_Sustainability\_of\_Next\_Generation\_Data\_Centers/links/566fe20a08ae4d9a42593fc5/Metrics-for-Assessing-Flexibility-and-Sustainability-of-Next-Generation-Data-Centers.pdf)
