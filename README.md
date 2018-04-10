![Estonian Information System Authority](https://github.com/e-gov/RIHA-Frontend/raw/master/logo/gov-CVI/lions.png "Estonian Information System Authority")

# X-tee implementation guide

X-tee help files for end-users

## Contributing specifics

- Only pages under /docs are included in the final HTML page
- The page is genereated with jekyll to x-road.ee/rakendusjuhend once a day
- New pages should be created right under /docs
- New images should be added to /docs/images folder
- [Set up the page locally](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/) to test your changes before commiting them to the master branch

### Linking

- After adding a new page, a link has to be added to index.md
- If there are several sections on a page, you can create an internal link to the specific section by using the heading's id after hashtag element in the link

### Design specifics

- All files are linked to RIHA-Help (https://abi.riha.ee/, based on https://github.com/e-gov/RIHA-Help)
