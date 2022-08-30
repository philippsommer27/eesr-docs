# ⚡ TUE

Total-power Usage Effectiveness, proposed by Patterson et al., is an attempt to add a level of depth to measuring data center equipment energy efficiency. To do this, the authors first define IT Usage Effectiveness (ITUE). In essence, it is a metric similar to PUE, but for the servers of the facility. It aims to report how much of the energy going into the IT equipment is spent on computing versus cooling, power delivery.

<details>

<summary>Details</summary>

Unit: **NA**

Minimum: **1.0**

Maximum: **∞**

Ideal: **1.0**

Industry Average: NA

****

</details>

## Formula

The formula for ITUE is:

$$
ITUE = \frac{\text{\textit{Total Energy into the IT Equipment}}}{\text{\textit{Total Energy into the Compute Components}}}
$$

The total for the numerator should be measured at the power supply level for the com- puter, whereas the denominator should be measured at the component level (perhaps 22 3.2 Energy Efficiency Metrics through software).

ITUE is then used for TUE:

$$
TUE = ITUE \times PUE
$$

## Evaluation

TUE provides a finer grained insight into the electricity usage of a data center towards providing its primary service. Unlike PUE it does not suffer as much from vagueness in measurement point as the definition clearly states that energy should be measured at the component level. The metric lacks industry wide adoption and evaluation.

## Interpretation

Like PUE, a high value indicates an inefficient DC in terms of overhead energy use, whereas a low value indicates an efficient use of the energy.&#x20;

## Improvement Strategies

Same as PUE!

## Sources

\[1] [TUE, a New Energy-Efficiency Metric Applied at ORNL’s Jaguar](https://link.springer.com/chapter/10.1007/978-3-642-38750-0\_28) [\[pdf\]](https://eta.lbl.gov/sites/default/files/downloads/isc13\_tuepaper.pdf)
