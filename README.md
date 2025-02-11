# conversion of the obf website to GitHub pages

Migration of the OBF WP site to a static site generator (Hugo)

## Running hugo server locally

### Setting up a GitHub fork so you can make changes on your desktop
(Instructions for those who are not git gurus)

1. To make changes to web pages on your desktop and commit them from the command line to GH, you will need a
[GitHub personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).
2. Go to https://github.com/OBF/OBF.github.io and make a fork
3. Then on your desktop (from the shell) do:
```
git clone  https://github.com/YOUR_GITHUB_ID/OBF.github.io
```
4. After you edit files on your desktop as desired, do:
```
cd OBF.github.io
git checkout -b BRANCH_NAME
git add FILES
git commit -m "my changes"
git push    (or you might need to do git push --set-upstream origin BRANCH_NAME)
```

5. Then go to https://github.com/YOUR_GITHUB_ID/OBF.github.io to make a PR
6. Once the PR is merged, your changes should be visible on
[https://obf.github.io/](https://obf.github.io/)

7. Next time you want to make more changes, first update your fork
(because others may have committed changes). Go to
https://github.com/YOUR_GITHUB_ID/OBF.github.io and click the "Sync
fork" button.

8. Then update your local copy to get the latest version.
```
git checkout main
git pull
```
9. Edit your local copy as desired. Then do the steps in #4 (with a new branch name) to commit your latest changes.


### Using hugo
0. Hugo documentation: https://gohugo.io/getting-started/quick-start/
1. [Install hugo](https://gohugo.io/installation/)
2. Initialize hugo
```
git submodule init
git submodule update
```
4. Run `hugo server` from the root folder of the project to launch a local server that automatically rebuilds:
```
hugo server &
```
5. View the site in your web browser by going to [http://localhost:1313/](http://localhost:1313/)
6. When you make changes, you should be able to reload http://localhost:1313/ to instantly see the changes!


## Steps taken to port content from old WP site

1. Create XML export of existing WP site with all pages & posts
2. Run the conversion script [wp2hugo](https://github.com/ashishb/wp2hugo) in the following way `/wp2hugo -source obf.WordPress.2025-01-30.xml -output obf-test-hugo -download-media -continue-on-media-download-error`
3. update the `hugo.yaml` to use the correct base page (as currently
   not deployed on open-bio.org). (For now, the first line of
   hugo.yaml should say "baseURL: https://OBF.github.io" but that will
   change later)
   


