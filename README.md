# WebKit Windows build (GitHub Actions)

This repo builds the upstream WebKit Windows port on GitHub-hosted
`windows-latest` runners and publishes a ZIP to a GitHub Release when you push
a tag.

## Trigger a build

```
git tag v0.1.0
git push origin v0.1.0
```

Workflow: `.github/workflows/build-webkit.yml`
