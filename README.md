# @crowsi/interaction-transport

0.10.0. Opaque bounded JSON transport, independent of Hatter, Nuxt, sem-lang and
application field meanings. Zixcel owns the resource/action/change contracts.

The JSONL adapter owns one installed executable and its process group, serializes
requests, caps the queue and bytes, times out queued and active requests, drains
stderr, and reaps the process on cancellation/close. It never retries an invoke:
after a lost reply the caller must use the same idempotency reference with its
application handler. No arbitrary command is accepted from a browser declaration.

Transport failures have a separate `TransportError.code`; they are not fabricated
application successes or HTTP-derived business errors. Connection authorization
and selecting a trusted installed executable belong to the host. This package
does not add mandatory pairing, passkeys, or a second authentication authority.

`watch(..., {active})` checks current consumer validity before a request and again
before delivering either its result or error. The host combines visibility,
scope and current grant validity in that predicate. Invalidated watches terminate;
create a new watch when the host explicitly establishes a new scope. On scope or
grant revision changes, stop the old watch even when access is immediately
regranted; a boolean alone cannot identify a revoke/regrant ABA transition.
`stop()` aborts the request, clears the retry timer and waits for disposal.
