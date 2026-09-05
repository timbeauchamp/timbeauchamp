# Timbo voice audition deployment

This folder contains the static production build of the Timbo audition app.
Public URL: https://timbeauchamp.github.io/timbeauchamp/voice-audition/

The source project is maintained separately at `~/development/timbo-voice-audition`.
To update, run `npm --prefix web run build` there, then replace this folder with
its `web/dist/` contents. Preserve this deployment note. Review and commit the
result to this repository’s main branch; the existing GitHub Pages build publishes it.
Keep both versioned corpora available for saved sessions. Include all attribution
files and audio. Do not copy models, private reports, or participant exports.

Sessions are stored per browser/origin. Use the local app’s Back up sessions and
the hosted app’s Import a file to transfer existing choices. Household votes use
file exchange; hosting does not add automatic synchronization.
