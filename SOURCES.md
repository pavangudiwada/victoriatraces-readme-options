# Asset and content sources

Capture/review date: October 30, 2026.

## Fresh screenshots

All four screenshots were captured from the actual public playground UI at its default 1280 × 720 viewport. They are JPEG browser captures, not generated UI. No labels, results, query text, or chart values were painted into them. The screenshots demonstrate an example state, not performance benchmarks.

| Asset | Source | Visible content |
| --- | --- | --- |
| `VictoriaMetrics/assets/metrics-query.jpg` | https://play.victoriametrics.com/ | VMUI v1.155.0 playground; `sum(rate(vm_http_requests_total[5m])) by (path) > 0`, 30-minute chart. Playground is an Enterprise cluster; the shown query/graph workflow is also available in open-source VMUI. |
| `VictoriaLogs/assets/log-explorer.jpg` | https://play-vmlogs.victoriametrics.com/ | `*` query, five-minute histogram, actual log messages |
| `VictoriaTraces/assets/trace-explorer.jpg` | https://play-vtraces.victoriametrics.com/select/vmui/ | v0.12.1; actual result list and selected trace preview |
| `VictoriaTraces/assets/trace-waterfall.jpg` | Same playground | Trace `a733250ba49f9b483b51cb9672470b94`; `user_browse_product`, 199.07 ms, nine spans. Same trace as Explorer capture. |

Playground data can expire. Static images preserve the captured state; “live playground” links intentionally open the general UI instead of relying on an expiring trace URL.

## Branding and diagrams

- Logo source: user-designated Logo Pack, last updated October 21, 2026, bundled in the VictoriaMetrics Product Imagery skill. Supplied SVGs copied unchanged into each `assets` directory. Purple product lockups for light mode; supplied white lockups for dark mode. Company master-brand lockup for the organization profile.
- Diagram reference: [recent architecture alternative](https://www.figma.com/design/F1LdaG32svZb3Onx01h8pK?node-id=28955-9204). Read from Figma during this task. Reference screenshot saved in `design-source/architecture-reference.png`.
- New diagrams use Lato, thin purple connectors, light cards, and dotted column separators inspired by that reference. These are conceptual data-flow diagrams, not captured product screens.
- Editable sources: each `how-it-works.svg` and `organization/profile/assets/product-map.svg`. PNG exports are 2×: product diagrams 2016 × 800, product map 2016 × 660. SVGs retain vector logos and editable text.
- Figma tool quota prevented creating new frames. The reference file was not modified.

## Content verification

- [Metrics quick start](https://docs.victoriametrics.com/victoriametrics/quick-start/), [Metrics cluster](https://docs.victoriametrics.com/victoriametrics/cluster-victoriametrics/), [Enterprise](https://docs.victoriametrics.com/victoriametrics/enterprise/).
- [Logs quick start](https://docs.victoriametrics.com/victorialogs/quickstart/), [Logs reference](https://docs.victoriametrics.com/victorialogs/), [LogsQL](https://docs.victoriametrics.com/victorialogs/logsql/).
- [Traces quick start](https://docs.victoriametrics.com/victoriatraces/quick-start/), [OTLP ingestion](https://docs.victoriametrics.com/victoriatraces/data-ingestion/opentelemetry/), [querying](https://docs.victoriametrics.com/victoriatraces/querying/).
- Latest release tags retrieved from GitHub: Metrics `v1.155.0`, Logs `v1.53.0`, Traces `v0.12.1`.
- Upstream and reference README snapshots are in `research/`. These snapshots are comparison material, not proposed replacement files.
- `research/link-check.json` records the initial HTTP check, including the removed invalid Logs Enterprise path. Final check results are recorded separately in `research/validation.md`.
