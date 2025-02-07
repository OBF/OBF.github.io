# conversion of the obf website to GitHub pages

Migration of the OBF WP site to a static site generator (Hugo)

## Running hugo server locally

1. [Install hugo](https://gohugo.io/installation/)
2. Clone the GH repo:
```
git clone  https://github.com/OBF/OBF.github.io
```
3. Initialize hugo
```
cd OBF.github.io
git submodule init
git submodule update
```
4. Run `hugo server` from the root folder of the project to get a
local server that automatically rebuilds:
```
hugo server &
```
5. View the site in your web browser by going to [http://localhost:1313/](http://localhost:1313/)
6. When you make changes, you should be able to reload http://localhost:1313/ to instantly see the changes!
7. To push your changes back to the live site, remember to commit
them. First you will need a
[GitHub personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens). Then do:
```
git checkout -b BRANCH_NAME
git add FILES
git commit -m "my changes"
git push    (or you might need to do git push --set-upstream origin BRANCH_NAME)
```
(Then go to https://github.com/OBF/OBF.github.io to make a PR)
8. Once the PR is merged, your changes should be visible on [https://obf.github.io/](https://obf.github.io/)


## Steps taken to port content from old WP site

1. Create XML export of existing WP site with all pages & posts
2. Run the conversion script [wp2hugo](https://github.com/ashishb/wp2hugo) in the following way `/wp2hugo -source obf.WordPress.2025-01-30.xml -output obf-test-hugo -download-media -continue-on-media-download-error`
3. update the `hugo.yaml` to use the correct base page (as currently not deployed on open-bio.org)
