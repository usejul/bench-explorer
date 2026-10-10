# decision-bench explorer

Which typed decider (Choice / Noul / Score) holds up on **your** task? Slice the bench by decision type,
language, text length, number of options and domain; filter deciders by family, runtime, hardware and size;
or paste a jul / Jev call and let the page pick the filters (parsed in your browser, nothing is sent).

Live: https://usejul.github.io/bench-explorer/

- `index.html`: the whole site (static, [ECharts](https://echarts.apache.org)).
- `explorer.json`: aggregated counts only (correct / total and a latency histogram per slice). No bench
  item, id or prediction is published. It is pushed by CI from the (private) decision-bench repo after
  every new result.

Reading the numbers: every score comes with its 95% Wilson interval. A slice under 30 items is flagged
as unreliable. Latencies were measured on different hardware (API, Mac M4, NVIDIA A10G) and are shown
next to it.

Part of [jul](https://github.com/usejul/jul). Apache-2.0.
