# Web Push scheduler

This public repository contains only the scheduler for https://upbit101.vercel.app.
It does not contain application source, exchange credentials, account data or shared secrets.

The standard GitHub-hosted Ubuntu runner invokes the authenticated endpoint every ten minutes
(at minutes 7, 17, 27, 37, 47 and 57). Each invocation checks up to two registered accounts.
The server authenticates short-lived GitHub OIDC tokens and sends Web Push to registered devices.
Logs contain only execution counts; the token is never printed. No checkout, artifact or cache is used.

GitHub schedules are best effort: they may be delayed or dropped. Public repositories' scheduled
workflows may be disabled after 60 days without repository activity. This is not a guaranteed
real-time alarm service. Standard runners in public repositories are free; no paid runner is used.

The user must enable notifications on each device. On iOS, install the web app on the Home Screen.
