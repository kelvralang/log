# kelvralang/log

Configurable leveled console logging for Kelvra. The canonical import is
`github.com/kelvralang/log`, and the package supports Kelvra runtime `^0.2.0`.

```bash
kelvra add github.com/kelvralang/log@v0.2.0
```

```kelvra
const log = @import("github.com/kelvralang/log")

log.setMinimumLevel(log.DEBUG)
log.info("server started")
log.debugNamed("database", "connection ready")
```

The four supported levels are `DEBUG`, `INFO`, `WARN`, and `ERROR`. Messages
below the configured minimum are suppressed. `enabled` lets callers avoid work
needed only to construct a disabled message, while `levelName` and
`isValidLevel` are useful when accepting log configuration from users.
`trySetMinimumLevel` validates a configured level and leaves the current
minimum unchanged when it returns `false`.

`write` accepts a level dynamically. `writeNamed` and the four `*Named`
helpers add a stable `[name]` prefix without introducing global logger state:

```text
INFO server started
DEBUG [database] connection ready
```

For backward compatibility, `setMinimumLevel` continues to accept custom
numeric thresholds. Dynamic writes at custom levels use the name `UNKNOWN`;
validate external configuration when named-level output is required. The
complete public contract is declared in `package.api.kel`. The package is
licensed under GPL-3.0-only; see `LICENSE`.
