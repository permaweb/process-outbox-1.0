# `process-outbox@1.0`

HyperBEAM Forge package for AO process outbox and subscription behavior.

The package root device is `process-outbox@1.0`. It appends outbound messages to
`results/outbox`, forwards `x-` request keys into notices, and can fan out
notifications to subscribers registered by action and target.

## Specification

`SPEC.md` is the package-level device contract.

## Build And Verify

```sh
rebar3 compile
rebar3 device verify
rebar3 device package
```

`rebar3 device package` emits a signed archive for `process-outbox@1.0`.

## Test

```sh
HB_PORT=0 rebar3 device test
rebar3 eunit-all
```

The package-specific vectors live in
`src/preloaded/test/hb_process_outbox_test_vectors.erl` and are run by
`rebar3 device test` against the freshly preloaded `process-outbox@1.0`
archive.
