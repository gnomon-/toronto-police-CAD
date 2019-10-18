# Toronto Police CAD

I've got a tool for grabbing the Toronto Fire service computer aided
dispatch (CAD) data feed; I wanted something similar for the TPS
(Toronto Police Services), thus this.

## Installation

`crontab` entry:

```
*/2     * *   *   *     ~gnomon/src/toronto-police-CAD/toronto-police-CAD
  # added 2019-10-18T17:23:47-04:00
#0       3 *   *   0     ~gnomon/src/toronto-police-CAD/toronto-police-CAD-archive
  # FIXME: got to write and enable this...
```

## Todo

- write archive job
- add ulimit / flock / timeout controls around cron jobs
- increase documentation
- remove hardcoded configuration paths
- deduplicate retrieved data since `ETag: ...` / `If-None-Match: ...`
  headers are ignored by the ARCGis server?  Or is this not worth the
  effort because the archive job will deduplicate it anyhow?
- capture / handle errors better
- add verbosity tweaking options
