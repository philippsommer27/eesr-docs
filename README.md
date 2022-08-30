# What is EESR?

The Energy Sustainability and Efficiency Reporting (EESR) instrument aims to provide a complete report generation solution for data center (DC) energy efficiency. Featuring a curated library of reporting metrics and visualizations, EESR prioritizes ease of use while maintaining high configurability for all audiences. Additionally, EESR consists of a grid analysis module which provides insight into the sustainability of a data center's energy profile given its energy use over a time period.

{% hint style="warning" %}
The name of the instrument is not final. EESR was originally designed as a component of OpenDC and as such was named 'OpenDC Energy Sustainability and Efficiency Reporting'. However as a standalone product, EESR is too generic and does not properly communicate its scope.&#x20;
{% endhint %}

### Why?

Why the need for EESR? Data centers energy efficiency research is a crucial part of our fight against climate change. Data center's consume a significant amount of electricity, of which the generation is not always green. To improve the efficiency of our data center, we must first deeply understand their current state. Furthermore, we must also be able to effectively communicate data center efficiency to the multitudes of stakeholders that are directly or indirectly involved with data centers.

### Features

EESR comes equip with a range of features for DC grid analysis and DC energy efficiency and sustainability reporting.&#x20;

#### EESR Reporting Module

The reporting module allows one to generate DC sustainability and energy efficiency reports. Reports feature metric values, source metadata and optionally graphs. Users can choose between different formats, reporting profiles and customize the entirety of the report should they wish to do so. The report is generated as a HTML file which can easily be modified and viewed. For easier distribution the module can also produce a PDF and PNG export.

#### EESR Grid Analysis Module

The grid analysis module derives various metrics and data from a given DC energy trace. By connecting to the [ENTSO-E](https://transparency.entsoe.eu/) API it can infer information about the source of the energy consumption and further deduce global warming impact through CO2 output calculation. The module is particularly suited for experiments as the timeframe, DC country and energy source model can be configured by the user. The results of an analysis can easily be turned into a report.

### Growing Knowledge Base

The real value of this instrument is beyond its fairly simply single page HTML builder. Rather, its in the wide and deep research of the DC energy efficiency reporting landscape in order to determine **how** to best report this subject. The culmination and findings of this research is described in the [metrics ](library/metrics/)and [graphs ](library/graphs/)library as well as a research paper. This work not only attempts to consolidate the most important knowledge on the topic in one place, but also encourage the community to further research in DC energy efficiency by highlighting its importance.&#x20;

EESR hopes to expand with the community and stay up to date with the latest findings. As such we encourage pull requests and issue submissions for this documentation and the [source code](https://github.com/philippsommer27/opendc-eesr).
