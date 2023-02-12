<!-- name: Default metrics
uses: midixx/metrics@latest
with:
  filename: metrics.base.svg
  token: ${{ ![Metrics](https://metrics.lecoq.io/midixx?template=classic&isocalendar=1&stargazers=1&followup=1&sponsors=1&discussions=1&base=header%2C%20activity%2C%20community%2C%20repositories%2C%20metadata&base.indepth=false&base.hireable=false&base.skip=false&isocalendar=false&isocalendar.duration=half-year&stargazers=false&stargazers.charts=true&stargazers.charts.type=classic&stargazers.worldmap=false&stargazers.worldmap.sample=0&followup=false&followup.sections=repositories&followup.indepth=false&followup.archived=true&sponsors=false&sponsors.sections=goal%2C%20list%2C%20about&sponsors.past=false&sponsors.size=24&sponsors.title=Sponsor%20Me!&discussions=false&discussions.categories=true&discussions.categories.limit=0&config.timezone=Asia%2FNovokuznetsk) }}
  base: header, activity, community, repositories, metadata

  - uses: midixx/metrics@latest
  with:
    config_timezone: Russia/Moskow -->




- uses: midixx/midixx
  with:
    # github user name to read the contribution graph from (**required**)
    # using action context var `github.repository_owner` or specified user
    github_user_name: ${{ github.repository_owner }}

    # list of files to generate.
    # one file per line. Each output can be customized with options as query string.
    #
    #  supported options:
    #  - palette:     A preset of color, one of [github, github-dark, github-light]
    #  - color_snake: Color of the snake
    #  - color_dots:  Coma separated list of dots color.
    #                 The first one is 0 contribution, then it goes from the low contribution to the highest.
    #                 Exactly 5 colors are expected.
    outputs: |
      dist/github-snake.svg
      dist/github-snake-dark.svg?palette=github-dark
      dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9