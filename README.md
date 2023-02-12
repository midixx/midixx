name: Default metrics
uses: midixx/metrics@latest
with:
  filename: metrics.base.svg
  token: ${{ ![Metrics](https://metrics.lecoq.io/midixx?template=classic&isocalendar=1&stargazers=1&followup=1&sponsors=1&discussions=1&base=header%2C%20activity%2C%20community%2C%20repositories%2C%20metadata&base.indepth=false&base.hireable=false&base.skip=false&isocalendar=false&isocalendar.duration=half-year&stargazers=false&stargazers.charts=true&stargazers.charts.type=classic&stargazers.worldmap=false&stargazers.worldmap.sample=0&followup=false&followup.sections=repositories&followup.indepth=false&followup.archived=true&sponsors=false&sponsors.sections=goal%2C%20list%2C%20about&sponsors.past=false&sponsors.size=24&sponsors.title=Sponsor%20Me!&discussions=false&discussions.categories=true&discussions.categories.limit=0&config.timezone=Asia%2FNovokuznetsk) }}
  base: header, activity, community, repositories, metadata

  - uses: midixx/metrics@latest
  with:
    config_timezone: Russia/Moskow
