<!-- <div id="header" align="center">
  <img src="img/animation.gif.gif">
</div>

<div id="badges" align="center">
  <a href="https://t.me/PSQ_official">
    <img src="https://img.shields.io/badge/Telegram-blue?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram Badge"/>
  </a>
  <a href="https://www.instagram.com/btxkis">
    <img src="https://img.shields.io/badge/Instagram-red?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram Badge"/>
  </a>
  <a href="your-twitter-URL">
    <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
  </a>
</div>

<div align="center">
    <img src="https://komarev.com/ghpvc/?username=midixx&style=flat-square&color=blue" alt=""/>
</div>

___________________________________________________________________________________________________________________________________________________________________________________

GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG GG
___________________________________________________________________________________________________________________________________________________________________________________ -->

<!--<div align="center">
    <h1>
    hey there
    <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px" align="center"/>
    </h1>
</div>

<div align="center">
  <img src="https://media.giphy.com/media/7uDtQm2jKdS0VGLg46/giphy.gif" width="600" height="300"/>
</div>

### :woman_technologist: About Me :
I am a python and web development <img src="https://media.giphy.com/media/l3nW3jtbBROj5XIC4/giphy.gif" width="30"> from Tokio.
- :telescope: I work as a software engineer and participate in the creation of software to improve life.

- :seedling: Learning to write technical content.

- :zap: In my free time I solve problems on GeeksforGeeks and read technical articles.

- :mailbox:How to reach me: [![Linkedin Badge](https://img.shields.io/badge/Telegram-blue?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/PSQ_official)


### :hammer_and_wrench: Languages and Tools :
<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/arduino/arduino-original.svg" title="Arduino" alt="Arduino" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/bootstrap/bootstrap-original.svg" title="Bootstrap" alt="Bootstrap" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/fedora/fedora-original.svg" title="Fedora" alt="Fedora" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg" title="Python" alt="Python " width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/css3/css3-plain-wordmark.svg"  title="CSS3" alt="CSS" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/html5/html5-original.svg" title="HTML5" alt="HTML" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="MySQL"  alt="MySQL" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/nodejs/nodejs-original-wordmark.svg" title="NodeJS" alt="NodeJS" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/git/git-original-wordmark.svg" title="Git" **alt="Git" width="40" height="40"/>
</div> -->

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
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: midixx
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Novokuznetsk
          plugin_isocalendar: yes
          plugin_isocalendar_duration: half-year