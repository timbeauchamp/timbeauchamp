# MUST DO: fix full-audition preference buttons

The preference buttons can remain disabled after switching to full auditions and listening. Investigate and fix this before the next release.

- [ ] Reproduce the final-round playback recognition failure.
- [ ] Verify both full clips unlock the preference buttons, including pause/resume, completion, and switching audition lengths.
- [ ] Ensure delayed playback events do not discard listening credit and seeking alone does not grant it.
- [ ] Preserve saved choices and compatibility with existing session exports.
- [ ] Run regression tests and verify the fix in a browser.
- [ ] Prepare the updated static build for review.
- [ ] Obtain explicit approval from Tim before deploying or merging into the GitHub Pages publishing branch.
- [ ] Verify the hosted app after the approved deployment.

Status: a candidate fix has been prepared locally; final browser verification and deployment remain outstanding. No fix has been published.
