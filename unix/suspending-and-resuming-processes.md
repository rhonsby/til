# Suspending and Resuming Processes

Suspending
-

To suspend a running process, send the `SIGSTOP` signal by using `ctrl + c`. You should see a similar output to this:

`[1]  + 1622 suspended  tail -f log/production.log`

##### Output Breakdown

* `[1]` — Unique identifier of suspended process<br>
* `1622` — PID (Process ID)<br>
* `suspended` — Status<br>
* `tail -f log/production.log` — Suspended Process

To see all suspended processes, use `jobs` to to view them in a list.

Resuming
-

There are two commands available to resume a suspended process.

`fg` — resumes last suspended process in foreground</br>
`bg` — resumes last suspended process in background

To resume a specific process, simply pass the unique identifier as an argument.

For example, `fg %1` will restart the `tail -f log/production.log` process that suspended above.
