![Header](https://github.com/midixx/midixx/blob/main/assets/matrix-code.gif)

## I'm a programmer, novice hacker and designer in the IT world.

Latest Telegram articles

### Languages and Tools
![Python](https://img.shields.io/badge/-Python-323334?style=for-the-badge&logo=python)
![C++](https://img.shields.io/badge/-C++-4e9442?style=for-the-badge&logo=C%2b%2b)
![HTML5](https://img.shields.io/badge/-html5-323334?style=for-the-badge&logo=html5)
![CSS3](https://img.shields.io/badge/-css3-4e9442?style=for-the-badge&logo=css3)
![JavaScript](https://img.shields.io/badge/-JavaScript-323334?style=for-the-badge&logo=Javascript)
![Photoshop](https://img.shields.io/badge/-Photoshop-4e9442?style=for-the-badge&logo=photoshop)


- uses: Platane/snk@v2
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


Follow me