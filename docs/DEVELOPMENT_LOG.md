# Development log

## 2026-10-25 — Yeobaek privacy and support page

Request: prepare the Yeobaek Android app for Google Play using the owner's existing GitHub website.

Change: added yeobaek.html as a separate Korean privacy/support page for dev.phoneagent.mvp. It describes the current offline alpha, local photo/video processing, optional calendar/notification/on-device voice features, storage/deletion, and the user-designated public support contact. Current builds have no ads or in-app purchase SDK; future billing is identified as a future change requiring updated disclosures. Existing game policies and styles were preserved.

Validation: reviewed the app manifest and relevant local-processing/notification/voice/storage code. Checked HTML structure and links in the local source; deployed-page and responsive visual checks follow publication. App release and payment verification are separate and were not performed by this website change.

Source: yeobaek.html was added in commit 57f1e4d3397fe45c75a2a873d50ec112f9d7e194. Expected public path: https://dr-sungworld.github.io/retro-brick-breaker-privacy/yeobaek.html . Publication success must be verified at that URL; a Git commit alone is not deployment confirmation.

Remaining: verify live page, connect the public URL in Play Console, update policy before changing actual network/SDK/payment behavior.

## 2026-10-25 — Publication verified

The public HTTPS page loaded without login in Chrome, with the Yeobaek title, package, current-alpha disclosure and user-designated support address. Desktop visual inspection passed. Page has no third-party scripts. The public URL was saved in the Yeobaek Play Console privacy-policy field; this is a saved app draft, not Google review approval. A local evidence capture is maintained with the Android project's release-preparation records.

The Android app's Settings > App info now links to the same page using ACTION_VIEW in an external browser. Local app compile/lint and JVM tests passed; actual device navigation for this new link is still unverified. No new network permission was added.
