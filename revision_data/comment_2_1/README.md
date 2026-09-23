# Comment 2.1 experiment evidence

`results.csv` contains all 270 method evaluations (54 matched snapshot instances).
`summary.json` records all three configurations and their paired comparisons.
Fig. 5(a)/(b) use one fixed population per configuration at six times. The
two-shell panel uses the first predetermined minimum-span selection (index 0),
with 30 evaluations over six snapshots; it performs no averaging or shading.
All other selections, including unfavorable results, remain in the archived
data and the supporting three-configuration plot. No experiments were rerun.

`manifest.json` records the selected satellite IDs, source/input hashes, frozen
checkpoint and protocol. `geometry_checks.json` and `validation.json` record the
Skyfield comparisons and matched-input checks. `simulation_settings.json` records
physical parameters and software versions. `execution.json`, `pilot_status.json`
and `full_status.json` describe the successful RTX 5090 workstation execution.
Wall times include setup/validation and concurrent execution; they are not the
paper's dedicated runtime measurements.

The accompanying `implementation.patch` applies to the leo-sat-flow Git revision
recorded in the manifest. It contains the opt-in loader, experiment driver,
plotter, focused regression tests, and reproduction instructions. The full raw
per-method JSON and execution logs are retained in the code repository's ignored
`sim_alg_v1_res/test_tcom_multishell/comment-2-1-20260922-ail/` run directory and on
the isolated workstation run at `/home/zhouyou/tcom-comment21-ail/`.
