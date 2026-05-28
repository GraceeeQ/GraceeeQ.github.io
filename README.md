# Yuhang Qiu Academic Website

This is the source for `GraceeeQ.github.io`, built with the al-folio Jekyll theme.

## Local preview

The local machine does not currently have Ruby installed, so Docker is the easiest way to build and preview:

```bash
docker run --rm -v "$PWD":/srv/jekyll -w /srv/jekyll -e JEKYLL_ENV=production amirpourmand/al-folio:latest bash -lc 'bundle check || bundle install --jobs 4 --retry 3; bundle exec jekyll build'
docker run --rm -p 8081:80 -v "$PWD/_site":/usr/share/nginx/html:ro nginx:alpine
```

Then open `http://localhost:8081`.

## Deploy

Create the GitHub repository `GraceeeQ/GraceeeQ.github.io`, push the `main` branch, and GitHub Actions will build and deploy the site.
