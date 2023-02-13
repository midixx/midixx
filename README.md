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
          #  - public_repo
          #  - read:project
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ ![Metrics](https://metrics.lecoq.io/midixx?template=classic&isocalendar=1&languages=1&people=1&calendar=1&achievements=1&projects=1&anilist=1&leetcode=1&stock=1&base=header%2C%20activity%2C%20community%2C%20repositories%2C%20metadata&base.indepth=false&base.hireable=false&base.skip=false&isocalendar=false&isocalendar.duration=half-year&languages=false&languages.ignored=html%2C%20css%2C%20javascript%2C%20python&languages.limit=8&languages.threshold=0%25&languages.other=false&languages.colors=github&languages.sections=most-used&languages.indepth=false&languages.analysis.timeout=15&languages.analysis.timeout.repositories=7.5&languages.categories=markup%2C%20programming&languages.recent.categories=markup%2C%20programming&languages.recent.load=300&languages.recent.days=14&people=false&people.limit=24&people.identicons=false&people.identicons.hide=false&people.size=28&people.types=followers%2C%20following&people.shuffle=false&calendar=false&calendar.limit=1&achievements=false&achievements.threshold=C&achievements.secrets=true&achievements.display=detailed&achievements.limit=0&projects=false&projects.limit=4&projects.descriptions=false&anilist=false&anilist.user=psqkill&anilist.medias=anime%2C%20manga&anilist.sections=favorites&anilist.limit=2&anilist.limit.characters=22&anilist.shuffle=true&leetcode=false&leetcode.user=.user.login&leetcode.sections=solved&leetcode.limit.skills=10&leetcode.limit.recent=2&stock=false&stock.symbol=bitcoin&stock.duration=1d&stock.interval=5m&config.timezone=Asia%2FNovokuznetsk) }}

          # Options
          user: midixx
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Novokuznetsk
          plugin_achievements: yes
          plugin_achievements_display: detailed
          plugin_achievements_secrets: yes
          plugin_achievements_threshold: C
          plugin_anilist: yes
          plugin_anilist_limit: 2
          plugin_anilist_limit_characters: 22
          plugin_anilist_medias: anime, manga
          plugin_anilist_sections: favorites
          plugin_anilist_shuffle: yes
          plugin_anilist_user: psqkill
          plugin_calendar: yes
          plugin_calendar_limit: 1
          plugin_isocalendar: yes
          plugin_isocalendar_duration: half-year
          plugin_languages: yes
          plugin_languages_analysis_timeout: 15
          plugin_languages_analysis_timeout_repositories: 7.5
          plugin_languages_categories: markup, programming
          plugin_languages_colors: github
          plugin_languages_ignored: html, css, javascript, python
          plugin_languages_limit: 8
          plugin_languages_recent_categories: markup, programming
          plugin_languages_recent_days: 14
          plugin_languages_recent_load: 300
          plugin_languages_sections: most-used
          plugin_languages_threshold: 0%
          plugin_leetcode: yes
          plugin_leetcode_limit_recent: 2
          plugin_leetcode_limit_skills: 10
          plugin_leetcode_sections: solved
          plugin_leetcode_user: .user.login
          plugin_people: yes
          plugin_people_limit: 24
          plugin_people_size: 28
          plugin_people_types: followers, following
          plugin_projects: yes
          plugin_projects_limit: 4
          plugin_stock: yes
          plugin_stock_duration: 1d
          plugin_stock_interval: 5m
          plugin_stock_symbol: bitcoin
