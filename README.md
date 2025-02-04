# test conversion of the obf website

Exploring the migration of the OBF WP site to a static site generator


## Running locally

1. [Install hugo](https://gohugo.io/installation/)
2. Run `hugo server` from the root folder of the project to get a local server that automatically rebuilds

## Steps taken

1. Create XML export of existing WP site with all pages & posts
2. Run the conversion script [wp2hugo](https://github.com/ashishb/wp2hugo) in the following way `/wp2hugo -source obf.WordPress.2025-01-30.xml -output obf-test-hugo -download-media -continue-on-media-download-error`
3. update the `hugo.yaml` to use the correct base page (as currently not deployed on open-bio.org)
