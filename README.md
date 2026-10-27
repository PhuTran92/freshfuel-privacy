# FreshFuel — privacy and support site

Static, no-build site publishing the FreshFuel privacy policy and support page in
English and Vietnamese.

**Live URL:** <https://phutran92.github.io/freshfuel-privacy/>

The mobile app opens this URL from the `PRIVACY_POLICY_URL` constant in
`Freshfuel-Mobile-Apps/composeApp/src/commonMain/kotlin/com/freshfuel/presentation/settings/SettingsScreen.kt`.

## Files

| Path | Purpose |
|---|---|
| `index.html` | English privacy policy |
| `support.html` | English support page |
| `vi/index.html` | Vietnamese privacy policy |
| `vi/support.html` | Vietnamese support page |

There is no build step. Each page is self-contained HTML with inline CSS and a
light/dark colour scheme. Language switching uses relative links, so keep the `vi/`
structure intact.

## Preview locally

```bash
cd Freshfuel-privacy-github
python3 -m http.server 8080
```

Open <http://localhost:8080/> for English and <http://localhost:8080/vi/> for Vietnamese.

## Deploy

The site is published with GitHub Pages at the live URL above. Publish the contents of
this folder at the Pages site root: `index.html` at `/`, Vietnamese pages under `/vi/`.
No Jekyll, build tool, or server-side code is required.

## Version control

This folder has no `.git` directory in this workspace. Treat the files here as the only
copy and keep an external backup until the site is placed under version control.
