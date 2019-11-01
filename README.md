# Toronto Police CAD

I've got a tool for grabbing the Toronto Fire service computer aided
dispatch (CAD) data feed; I wanted something similar for the TPS
(Toronto Police Services), thus this.

## Installation

`crontab` entry:

```
*/2     * *   *   *     ~gnomon/src/toronto-police-CAD/toronto-police-CAD
  # added 2019-10-18T17:23:47-04:00
0       3 *   *   0     ~gnomon/src/toronto-police-CAD/toronto-police-CAD-archive
  # FIXME: got to write and enable this...
  # 2019-11-01T15:38:59-04:00 - manually tested then enabled this job
```

## Todo

- add ulimit / flock / timeout controls around cron jobs
- increase documentation
- remove hardcoded configuration paths
- capture / handle errors better
- add verbosity tweaking options
