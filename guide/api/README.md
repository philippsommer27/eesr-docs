# API

### Interface

The _interface_ module provides all the basic functionality of EESR.

#### read\_data()

Read the .json file containing the metrics and metadata.

```python
def read_data(data_path)
```

| Parameter                | Description                        |
| ------------------------ | ---------------------------------- |
| **data\_path**: _String_ | Path to JSON file containing data. |

#### generate\_standard\_profile()

{% code overflow="wrap" %}
```python
def generate_standard_profile(data_path, profile_name, path="compact_report.html", generate_domain=False)
```
{% endcode %}

| Parameter                   | Description                                                  |
| --------------------------- | ------------------------------------------------------------ |
| **data\_path**: _String_    | Path to JSON file containing data.                           |
| **profile\_name:** _String_ | Choice between "std\_prof", "sus\_prof", and "ee\_prof".     |
| **graph\_data**             | Data for graph generation.                                   |
| **path:** _String_          | Output path.                                                 |
| **generate\_domain:** bool  | Whether to include additional data from input file in report |

#### generate\_compact\_profile()

Same as above, except no **graph\_data.**

#### **to\_pdf() & to\_image()**

Export a HTML report as pdf or image.

```python
def to_image(report, out=None)

def to_pdf(report, out=None)
```

| Parameter            | Description                                                                        |
| -------------------- | ---------------------------------------------------------------------------------- |
| **report**: _String_ | Path to HTML report.                                                               |
| **out:** _String_    | Output path. If left as default, output file will use path and name of input file. |

#### **opendc\_grid\_analysis()**

Perform grid analysis for an OpenDC simulation using EEWriter.

{% code overflow="wrap" %}
```python
def opendc_grid_analysis(dc_path, key_path, start, country, out, tz="Europe/Amsterdam", caching=True, green_ratio=None, PUE=1.59)
```
{% endcode %}

| Parameter                     | Description                                                                                                                                                                                                  |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **dc\_path:** _String_        | Path to input energy trace file.                                                                                                                                                                             |
| **key\_path:** _String_       | Path to .txt file containing ENTSO-E API key. Can be obtained by requesting from [ENSTO-E](https://transparency.entsoe.eu/content/static\_content/download?path=/Static%20content/API-Token-Management.pdf). |
| **start:** _pandas.Timestamp_ | The start time of the DC energy trace. Does not have to match the start time in the trace file.                                                                                                              |
| **country:** _String_         | Bidding zone (country) where the DC is located. Possible bidding zones can be found on the [ENTSO-E transparency website](https://transparency.entsoe.eu/dashboard/show).                                    |
| **out:** _String_             | Output path of analysis.                                                                                                                                                                                     |
| **tz:** _String_              | [TZ Database name](https://en.wikipedia.org/wiki/List\_of\_tz\_database\_time\_zones).                                                                                                                       |
| **caching:** _bool_           | Whether to enable caching for data fetching.                                                                                                                                                                 |
| **green\_ratio:** _float_     | Percentage of green energy to assume when calculating energy by type. If left blank, naive model is used where proportionality on the grid is kept.                                                          |
| **PUE:** _float_              | The PUE value of the DC, used for preprocessing.                                                                                                                                                             |
