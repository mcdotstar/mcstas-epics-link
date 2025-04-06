# Send instrument variables to EPICS 

| Variant            | Description                                                           |
|--------------------|-----------------------------------------------------------------------|
| `Epics.comp`       | The original, send named parameter values to EPICS                    |
| `EpicsEcho.comp`   | Only echo to STDOUT information about parameters for EPICS            |
| `EpicsIndex.comp`  | Send named parameters, or *all* instrument parameters to EPICS        |
| `UpdateEPICS.comp` | `EpicxIndex` but combines all updates into a single command execution |

Of the available variants, `UpdateEPICS` offers the best performance if the `put` command
accepts multiple whitespace separated `address` `value` pairs in one call.
Otherwise, `EpicsIndex` has the same flexibility to automatically send all values, one at a time.
