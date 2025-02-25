reference documentation online :
<https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll>

1. installing docker on windows/wsl
2. create a new jekyll site inside the current project folder

```bash
# use --force at the end to overwrite the existing files
docker run --rm -v "$PWD:/srv/jekyll" -it jekyll/jekyll jekyll new .
```

3. serving the site locally

```bash
docker run --rm -v "$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll jekyll serve
```

4. if error when running the above command

```bash
# adding webbrick to the gemfile
docker run --rm -v "$PWD:/srv/jekyll" jekyll/jekyll bundle add webrick
```
