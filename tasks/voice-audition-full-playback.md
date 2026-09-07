# MUST DO: fix full-audition preference buttons

Status: tested candidate build prepared on this branch. Deployment requires Tim's explicit approval. Tracks #1.

## Confirmed finding
The published final opens in Quick hello mode but requires full-clip listening credit. Reproduced A → B → A: both voices display Heard while preference buttons remain disabled. The same sequence in full mode unlocked successfully in the tested browser. An additional intermittent full-mode failure has not been reproduced.

## Changes
- Finals select full auditions and disable the ineligible preview option, including household finals.
- Credit uses browser-confirmed played ranges, including pause/end and before the player is replaced.
- Interrupted play requests are not treated as failed audio downloads.
- Voting guidance identifies missing playback credit or storage conflicts.

## Verification (2026-09-07)
- 22 automated tests and production build passed.
- 1,000 seeded playback-range simulations passed (30 updates per sequence). These are logic tests, not 1,000 browser trials.
- Six actual browser final trials passed: 12 play/pause clicks each, 72 total. Random generator seed 907; delays sampled from 50–749 milliseconds, plus browser-tool overhead. Each trial begins A/B/A, then randomly chooses either control. Each final unlocked and remained unlocked.
- A synthetic final accepted a winner and displayed results.
- An earlier-round A/B/A test retained credit through a clip-length switch, advanced successfully, and reset the next matchup's listening requirements. No browser console errors observed in that check.
- Synthetic sessions were used; no participant choices were changed or included here.

## Remaining
- [ ] Tim approves publishing this build to the existing voice-audition GitHub Pages URL.
- [ ] Merge/push the approved build to the publishing branch and verify the hosted page.
- [ ] Confirm the reported experience is resolved and close #1.

The browser checks cover one browser on this machine, not every browser or device.
