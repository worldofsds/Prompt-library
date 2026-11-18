PROMPT LIBRARY — GITHUB STORAGE + OWNER MANAGEMENT

This version uses a public GitHub repository as the prompt database.
Visitors can read/copy prompts. The owner manages the data through GitHub's own sign-in and repository permissions.

SETUP
1. Create a PUBLIC GitHub repository, e.g. prompt-library.
2. Upload index.html, config.js and prompts.json to the repository root.
3. Edit config.js and set:
   repository: "YOUR_GITHUB_USERNAME/YOUR_REPOSITORY"
   branch: "main"
4. Commit the config.js change.
5. Enable GitHub Pages: Repository → Settings → Pages → Deploy from a branch → main → /(root) → Save.
6. Share the published Pages URL with visitors.

OWNER MANAGEMENT
- Click "Owner: Manage prompts on GitHub" on the website.
- Sign in to GitHub using the account that owns/has write access to the repository.
- GitHub opens the prompts.json editor. Add, edit or delete prompt objects in the JSON array, then commit changes.
- Only repository users with write permission can commit edits. Visitors only see the public read-only site.
- GitHub Pages refreshes after the commit/build completes.

ADD A PROMPT
Add an object inside prompts.json:
{
  "title": "My new prompt",
  "category": "Image Generation",
  "description": "What this prompt does",
  "prompt": "Paste the full prompt here."
}
Put a comma between objects. Keep valid JSON and use double quotes.

SECURITY / PRIVACY
- This is intentionally a public repository and public website: visitors can read/copy the prompts and also inspect the public JSON/source.
- Visitors cannot edit the repository unless you grant them write access. Never grant write access to ordinary visitors.
- GitHub itself handles owner authentication; this site does not store your GitHub password or token.
- Do not put passwords, API keys, private prompts or confidential information in a public repository.
- If you want private source files while still displaying selected prompts publicly, a separate backend/workflow is required.

The owner management button opens GitHub's native file editor. It is not an embedded dashboard; GitHub's UI performs the authenticated edits.
