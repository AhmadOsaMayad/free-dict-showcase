# Pre-publish checklist

This folder is a **standalone repository in waiting**. When it's time to
publish, everything below should take under five minutes.

## Steps

1. **Move the folder** out of this project onto its own location, e.g.

   ```bash
   mv free_dict_showcase ~/projects/free-dict-showcase
   cd ~/projects/free-dict-showcase
   ```

2. **Create the GitHub repo** (public), e.g. `AhmadOsaMayad/free-dict-showcase`.

3. **Push it:**

   ```bash
   git init -b main
   git add .
   git commit -m "Initial showcase: README, screenshots, release v1.0.0"
   git remote add origin https://github.com/AhmadOsaMayad/free-dict-showcase.git
   git push -u origin main
   ```

4. **On GitHub, in the new repo** (Settings → General):
   - Set the description: *The offline English dictionary that actually
     explains words like a person would — idioms, IPA, homographs, 108k+
     entries, zero internet.*
   - Add topics: `dictionary`, `offline`, `flutter`, `android`,
     `english-dictionary`, `mobile-app`, `showcase`.
   - Upload a **social preview** image (Settings → General → Social
     preview) — good choice: `screenshots/word-details-view-midside-dark.png`
     on a background, or the app logo.

5. **Optional — download button polish:** replace the README's direct-APK
   badge link with a
   `https://github.com/<user>/<repo>/releases/latest/download/free_dict.apk`
   URL once you upload `free_dict.apk` to the new repo's first Release.
   That keeps the badge working across future versions.

## Before every new release

- Drop the new APK into `release/` (replacing the old one).
- Update `release/RELEASE_NOTES.md`.
- Update the SHA-256 in `release/RELEASE_NOTES.md` **and** the collapsed
  checksum block in `README.md`.
- Update the version number in the README download badge.
- Optionally refresh screenshots if the UI changed.

## Don't forget

- The APK in `release/` is ~32 MB — normal for a full offline dictionary;
  GitHub's 100 MB per-file limit is respected.
- Source code stays out of this repo on purpose (see README → FAQ →
  *Is the source code available?*).
