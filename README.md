# WebKit Windows build (GitHub Actions)

This repo builds the upstream WebKit Windows port on GitHub-hosted Windows
runners and publishes a ZIP to a GitHub Release. The output is intended for
testing WebKit behavior on Windows (MiniBrowser), not as a full browser product.

## Trigger a build (tagged release)

```
git tag v0.1.0
git push origin v0.1.0
```

Workflow: `.github/workflows/build-webkit.yml`

## Package-only release (no rebuild)

If you already have a successful build run that uploaded `webkit-build-outputs`,
you can publish a new ZIP without rebuilding by running the `package-only`
workflow and providing the run ID and a new tag.

Workflow: `.github/workflows/package-only.yml`

## Usage (MiniBrowser)

1) Download the latest release ZIP and extract it.
2) Run `MiniBrowser.exe` from the extracted folder (not from inside the ZIP).
3) If Windows shows a security warning, click **More info** and then **Run anyway**.
