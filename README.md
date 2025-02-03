# test conversion of the obf website

Exploring the migration of the OBF WP site to a static site generator


## Steps taken

1. Create XML export of existing WP site with all pages & posts
2. Run the conversion script [wp2hugo](https://github.com/ashishb/wp2hugo) in the following way `/wp2hugo -source obf.WordPress.2025-01-30.xml -output obf-test-hugo -download-media -continue-on-media-download-error`
3. update the `hugo.yaml` to use the correct base page (as currently not deployed on open-bio.org)
4. remove any leading `/` in media `/wp` paths, as test site isn't deployed to open-bio.org yet: `find . -type f -name '*.md' -exec sed -i "s/image: \/wp/image: \/obf-hugo-test\/wp/g" {} +` & `find . -type f -name '*.md' -exec sed -i "s/](\//](\/obf-hugo-test\//g" {} +`
