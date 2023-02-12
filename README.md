<!-- name: Default metrics
uses: midixx/metrics@latest
with:
  filename: metrics.base.svg
  token: ${{ ![Metrics](https://metrics.lecoq.io/midixx?template=classic&isocalendar=1&stargazers=1&followup=1&sponsors=1&discussions=1&base=header%2C%20activity%2C%20community%2C%20repositories%2C%20metadata&base.indepth=false&base.hireable=false&base.skip=false&isocalendar=false&isocalendar.duration=half-year&stargazers=false&stargazers.charts=true&stargazers.charts.type=classic&stargazers.worldmap=false&stargazers.worldmap.sample=0&followup=false&followup.sections=repositories&followup.indepth=false&followup.archived=true&sponsors=false&sponsors.sections=goal%2C%20list%2C%20about&sponsors.past=false&sponsors.size=24&sponsors.title=Sponsor%20Me!&discussions=false&discussions.categories=true&discussions.categories.limit=0&config.timezone=Asia%2FNovokuznetsk) }}
  base: header, activity, community, repositories, metadata

  - uses: midixx/metrics@latest
  with:
    config_timezone: Russia/Moskow -->



# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on: 
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ https://metrics.lecoq.io/midixx?template=classic&isocalendar=1&anilist=1&base=header%2C%20activity%2C%20community%2C%20repositories%2C%20metadata&base.indepth=false&base.hireable=false&base.skip=false&isocalendar=false&isocalendar.duration=half-year&anilist=false&anilist.user=psqkill&anilist.medias=manga&anilist.sections=favorites&anilist.limit=2&anilist.limit.characters=22&anilist.shuffle=true&config.timezone=Asia%2FNovokuznetsk }}

          # Options
          user: midixx
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Novokuznetsk
          plugin_anilist: yes
          plugin_anilist_limit: 2
          plugin_anilist_limit_characters: 22
          plugin_anilist_medias: manga
          plugin_anilist_sections: favorites
          plugin_anilist_shuffle: yes
          plugin_anilist_user: psqkill
          plugin_isocalendar: yes
          plugin_isocalendar_duration: half-year