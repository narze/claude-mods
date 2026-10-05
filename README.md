# claude-mods

A [Claude Code](https://claude.com/claude-code) plugin marketplace with narze's mods: games and toys that run inside the terminal.

## Install

In Claude Code:

```
/plugin marketplace add narze/claude-mods
/plugin install flappy-claude@narze-mods
/plugin install bad-apple@narze-mods
```

Or from the shell:

```sh
claude plugin marketplace add narze/claude-mods
claude plugin install flappy-claude@narze-mods
```

Get new versions with `claude plugin marketplace update narze-mods`, then `claude plugin update <name>@narze-mods`.

## Mods

| Mod | What it is | Repo |
| --- | --- | --- |
| `flappy-claude` | A Flappy Bird-like game above the prompt: fly the Claude mascot through the pipes. `/flappy-claude` to play. | [narze/flappy-claude-mod](https://github.com/narze/flappy-claude-mod) |
| `bad-apple` | Plays Bad Apple!! above the prompt or in a pane, with sound. `/bad-apple` to play. | [narze/bad-apple-claude-mod](https://github.com/narze/bad-apple-claude-mod) |

**bad-apple needs one more step:** its video frames and song are copyrighted, so they are not in its repo. After you install it, build them once with the script in the installed copy (`scripts/build-assets.sh`; needs `ffmpeg`, `python3` and `yt-dlp` or `uv`). `/bad-apple` tells you the path when the assets are missing.

## Add a mod

Add an entry to `plugins` in `.claude-plugin/marketplace.json`:

```json
{ "name": "<plugin name>", "source": { "source": "github", "repo": "narze/<repo>" }, "description": "<one line>" }
```

Then run `claude plugin validate .`.

## License

[MIT](LICENSE)
