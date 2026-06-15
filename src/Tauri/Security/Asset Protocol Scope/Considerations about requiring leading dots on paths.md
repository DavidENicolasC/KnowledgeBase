On [[Unix]], `requireLiteralLeadingDot` defaults to **`true`**. Then wildcard tokens such as `*`, `?`, `**`, and `[...]` **do not match a path component that starts with** `.` (dotfiles and dot-directories such as `.cache` or `.ssh`).

A pattern like `$HOME/**` can allow `/home/user/Documents/file.png` but **not** `/home/user/.cache/myapp/preview.png`, because `.cache` is a dot-prefixed component. A pattern that names the segment literally (for example `$HOME/.cache/myapp/**`) **does** match.

You can [[Allow prefixed components in a broad glob]]