# Multiple Commands
There are a couple of ways to run multiple commands in the same line: `&&` and `;`.  The way in which they differ is subtle, but is definitely worth knowing.

#### `command1 && command2`

When using double ampersands, `command1` will first run. If `command1` completes with a return status of 0 (success), only then will `command2` run. You can imagine then that this is useful when chaining commands that are dependent on the success of the command(s) before to it.

#### `command1 ; command2`

When separating the commands with a semicolon, both commands will run regardless of the exit status of `command1`. The commands do not depend on the success of previous commands, so all commands will run. This is useful when running a series of commands that would otherwise be repetitive to type, enter, and repeat.

