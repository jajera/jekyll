# jekyll

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

## About The Project
My personal wiki notes on jekyll implementation

### Built With
[![Jekyll][Jekyllrb.com]][Jekyll-url]


## Getting Started

### Prerequisites

* Install jekyll and bundler

  ``` bash
  gem install jekyll bundler
  ```

* Grant permission to main branch to allow it to deploy to gh-pages branch.

  * Go to Settings page of the repository, click Environments tab and select github-pages environment then click on Edit button.

  * Under Deployment branches, click Add deployment branch rule and enter main on the Branch name pattern text then click Add rule button to apply the changes.

### Installation

1. Create a new repository.
2. Clone the newly created repository.

    ``` bash
    git clone git@github.com:<username>/<repository>.git
    ```

3. Change directory to the local repository path.
4. Create a new jekyll site.
    ``` bash
    jekyll new .
    ```
5. Update Gemfile if necessary and execute this command to update Gemfile.lock for changes to reflect.

    ``` bash
    bundle install
    ```
6. Update _config.yml accordingly.

<!-- https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll -->

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/jajera/jekyll.svg?style=for-the-badge
[contributors-url]: https://github.com/jajera/jekyll/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/jajera/jekyll.svg?style=for-the-badge
[forks-url]: https://github.com/jajera/jekyll/network/members
[stars-shield]: https://img.shields.io/github/stars/jajera/jekyll.svg?style=for-the-badge
[stars-url]: https://github.com/jajera/jekyll/stargazers
[issues-shield]: https://img.shields.io/github/issues/jajera/jekyll.svg?style=for-the-badge
[issues-url]: https://github.com/jajera/jekyll/issues
[license-shield]: https://img.shields.io/github/license/jajera/jekyll.svg?style=for-the-badge
[license-url]: https://github.com/jajera/jekyll/blob/master/LICENSE.txt
[Jekyllrb.com]: https://img.shields.io/badge/Jekyll-2B2B2B?style=for-the-badge&logo=jekyll&logoColor=B5191A
[Jekyll-url]: https://jekyllrb.com
