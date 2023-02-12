name: Default metrics
uses: midixx/metrics@latest
with:
  filename: metrics.base.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: header, activity, community, repositories, metadata
