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

## 2026-10-25 — Owner-approved compression review video

The owner explicitly approved publishing artifacts/play-store/yeobaek-compression-review.mp4 in this public repository and submitting its URL to Google Play. Added the 44.07-second, silent, redacted recording and a simple playback page. Video SHA256: 37DC4D9BEEBCBEFC814FD53B6698780959FA4B8919007175237D2CDB5EC56215; 418868 bytes. It shows user-started video transcoding, progress notification, cancellation and original preservation. Unrelated notifications and media previews are hidden; the recording still contains the selected file name and size, as disclosed to the owner before approval. Raw private recording is not published.

The recording uses local version 59; Play candidate remains version 58. The playback page discloses that distinction and the Android-version-specific foreground service types. The version 59 development record states the compression policy/service were not changed, and recording-only settings were restored. App source, APK and signing secrets are not published. Live playback, foreground-service form save and Google review submission require separate verification; this commit alone does not establish any of them.

## 2026-10-25 — Live review video and closed-track submission request verified

The public playback page loaded without login. Browser video metadata reported duration 44.066667 seconds, readyState 4 and no media error; playback advanced beyond 6 seconds while unpaused. Both media-transcoding foreground-service declarations were saved with this verified URL. The additional Advertising ID declaration was saved as not used, consistent with the version 58 bundle manifest and previously checked dependencies.

The owner-authorized version 58 closed Alpha release, South Korea targeting, two selected tester lists (22 + 1), store listing and app-content changes were saved and review transmission was confirmed. Play Console changed to reviewing changes, with pre-review automatic checks still running and forwarding to Google review conditional on successful completion. This is a submission request, not review approval or completed tester distribution. No production release or billing change was made. Closed-test participation and the required continuous testing period have not been verified.

## 2026-10-25 — Version 62 privacy clarification and review context

The owner requested registering the latest Yeobaek in Play Console. Added an explicit description of optional, default-off photo EXIF capture-location use for local album grouping. It does not obtain current device location or send capture locations to servers; the app purges cached capture locations when disabled or access is revoked. Verified this against AlbumLocation and the app manifest. Existing privacy/support text and site files are preserved. Updated the review-video page to distinguish the version 59 recording from the version 62 submission and the new in-screen photo-batch workflow; the approved MP4 is unchanged.

Local version 62 bundle creation and existing-upload-key signature verification passed. Bundle ZIP integrity passed, INTERNET and AD_ID permissions are absent, and the bundled permission set matches the previously uploaded version 60. Existing scoped build/lint/device verification for version 62 is reused; individual tester installs and Google approval of version 62 are not yet verified. Live policy/video-page verification and Play upload/submission results are recorded separately in the local app release log.
