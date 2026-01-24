# Mobile Commands for GitHub PR

## Quick PR Command

Run this single command to commit all changes, push to GitHub, and create a PR:

```bash
cd ~/docs && git add -A && git commit -m "$(cat <<'EOF'
Update documentation for YouTube-Floater project

Replace Mintlify starter template with YouTube-Floater specific documentation including project overview, installation guide, usage instructions, and development setup. Update branding, navigation, and all content pages to reflect the YouTube floating player application.

Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>
EOF
)" && git push -u origin claude-onthego && gh pr create --title "Update docs for YouTube-Floater" --body "$(cat <<'EOF'
## Summary
- Updated all documentation to reflect YouTube-Floater project
- Replaced Mintlify starter template with YouTube-Floater branding
- Added installation guide for macOS users
- Added development setup instructions
- Updated navigation and removed template sections

## Changes
- **docs.json**: Updated name, colors, navigation, and links
- **index.mdx**: Complete rewrite with YouTube-Floater introduction and features
- **quickstart.mdx**: Installation and usage guide for YouTube-Floater
- **development.mdx**: Local development setup and contribution guide
- **README.md**: Updated repository documentation

## Test Plan
- [ ] Preview docs locally with `mint dev`
- [ ] Verify all links work correctly
- [ ] Check mobile responsiveness
- [ ] Confirm branding matches YouTube-Floater

🤖 Generated with Claude Code
EOF
)"
```

## Step-by-Step Commands (if you prefer)

### 1. Commit changes
```bash
cd ~/docs && git add -A && git commit -m "Update documentation for YouTube-Floater project

Replace Mintlify starter template with YouTube-Floater specific documentation.

Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>"
```

### 2. Push to GitHub
```bash
git push -u origin claude-onthego
```

### 3. Create PR
```bash
gh pr create --title "Update docs for YouTube-Floater" --body "Updated all documentation to reflect YouTube-Floater project. Includes installation guide, development setup, and branding updates."
```

## Current Status

Branch: `claude-onthego`
Modified files:
- README.md
- development.mdx
- docs.json
- index.mdx
- quickstart.mdx

All changes are staged and ready to commit.
