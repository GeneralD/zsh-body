# zsh-body

Tiny zsh plugin providing a single `body` function: print a line range
of a file, like a combined head/tail (`body [START],[END] [FILE]`,
implemented as a thin wrapper around `sed -n "${range}p"`).

- Language/stack: pure zsh, no dependencies, no build step.
- Entry point: `body.plugin.zsh` (the entire implementation, ~15 lines).
- Loadable by any zsh plugin manager (oh-my-zsh, zplug, antigen, ...).
- Status: legacy/minimal utility; no tests, no CI, no LICENSE file.
- To try it: `source body.plugin.zsh` then `body 2,5 somefile`.
  Omitting START defaults to line 1; omitting END defaults to EOF.
