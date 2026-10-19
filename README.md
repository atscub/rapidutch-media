# RapiDutch media

Images and reels for RapiDutch's social posts, served at **https://abrahamtoledo.dev/rapidutch-media/<path>** so Buffer can fetch them (`atscub.github.io/rapidutch-media/…` redirects there: the account's Pages domain). Buffer takes media only by a public URL that stays up until the post publishes. The Head of Growth adds files here; see ADR-0122 in the app's repository.

- **Media only:** `.png`, `.jpg`, `.jpeg`, `.webp`, `.gif`, `.mp4`. The Pages workflow publishes nothing else, so no page, script or document is ever served from here.
- **Nothing personal, ever:** no learner's data and no private document. This repository is public.
- **Push a file only when its post goes into Buffer** (as a draft at Stage 0), not before: anything here is public at once.
- **`health.png`** is a 1-pixel check that the site serves.
- **Layout:** `cards/<series>/<file>`, `reels/<file>`. A file's URL never changes once a post uses it.
- **Size:** Pages serves at most 1 GB, and the workflow stops at 900 MB. Delete files 30 days after their post has published (the platforms keep their own copy).
- **Commits use GitHub's no-reply address** (`29891965+atscub@users.noreply.github.com`), set in this clone's `.git/config`. A public repository shows every commit's email, and the pre-push hook refuses any other.
