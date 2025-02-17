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
9. Edit your local copy as desired. Then do the steps in #4 (with a NEW branch name) to commit your latest changes.


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
6. When you save edits to the web page files,
   http://localhost:1313/ will reload seconds later so you can instantly see the changes!


#### Seeing images on localhost

At the moment (2025-02-12), the images live in a separate repo,
https://github.com/OBF/wp-content/. If you want to view images in the
web pages on localhost:1313, you will need to clone that repo and then
make a symbolic link to it in the content directory of your
checked-out copy of OBF.github.io.

This may change.

#### Some Hugo tips

- To set up a URL redirect, add an alias to the page you want to
  redirect *to*. This goes in the header part of the .md (the part
  between the three dashes) and looks like this:
```
 aliases:
  - /events/bosc/
```

  - To include an image, you can use this markdown format:
  ```
  ![alt text](image-path)
```

- Images take up the full width of the page. If you want to scale an
image, use this html:
```
<img src="image-path" style="width:75%" alt="alt text" />
```

- When testing changes on localhost:1313, note that changes that
  involve .pngs take effect right away, but for some reason, if you're
  using .jpg or .jpeg images, it takes a while (20 min or so?) for
  them to show up on localhost. No idea why.
  - To enclose a section of text in a gray box use
  ```
  <div class="well">
  ```
  
- To make two columns (e.g. to run text next to an image), use
"columns" (look for an example in one of our .mds)
- You can make a button like this:
```
<a href="URL" class="btn btn-lg btn-primary">text on button</a>
```

## Steps taken to port content from old WP site

1. Create XML export of existing WP site with all pages & posts
2. Run the conversion script [wp2hugo](https://github.com/ashishb/wp2hugo) in the following way `/wp2hugo -source obf.WordPress.2025-01-30.xml -output obf-test-hugo -download-media -continue-on-media-download-error`
3. update the `hugo.yaml` to use the correct base page (as currently
   not deployed on open-bio.org). (For now, the first line of
   hugo.yaml should say "baseURL: https://OBF.github.io" but that will
   change later)
   


