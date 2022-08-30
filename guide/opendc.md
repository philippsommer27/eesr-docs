# OpenDC

EESR is expected to be used with OpenDC as a source trace. We implement a basic `ComputeMonitor` called [`EEWriter`](https://github.com/philippsommer27/opendc/blob/master/opendc-experiments/opendc-experiments-ees/src/main/kotlin/writer/EEWriter.kt) which records the IT energy usage of a simulated data center as an example of how this can be achieved. The writer records the energy usage of each host, which is then aggregated in the EESR OpenDC preprocessing stage.

As a long term goal we plan to migrate the functionalities of EESR directly into OpenDC.
