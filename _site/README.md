networkboot.github.com
======================

The website https://networkboot.org/.

When you have cloned this git repository and you want to make modifications,
here are the steps you should follow to create correct pull requests.

To view the generated website, run this command to spin up a tiny web server
(or use an existing one):

```
python -m SimpleHTTPServer
```

Then you can open up the site (usually `http://localhost:8000/`) in your
browser.

Only ever modify files under `_site`, as all the files above it is
generated automatically by the build script.

To re-generate the entire site, run this command:

```
_site/compile
```

Source files in `_site` with the suffix `.tt` are written in [Template
Toolkit](https://template-toolkit.org/). They are used to generate the HTML
for the static site. To find them all, run this command:

```
find _site -type f -name \*.tt | sort
```

Make sure you always run `_site/compile` and merge in the generated files
before you submit a pull request.
