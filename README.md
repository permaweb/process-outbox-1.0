# `process-outbox@1.0`

HyperBEAM Forge package for AO process outbox and subscription behavior.

The package root device is `process-outbox@1.0`. It appends outbound messages to
`results/outbox`, forwards `x-` request keys into notices, and can fan out
notifications to subscribers registered by action and target.

## published package

```bash
device publish: process-outbox@1.0 

spec=Oi9kpETC0JcNgb38Fn8W-lcRNXlp1USfcy2dHw3cmQ0 

impl=HOcPV7wxMHYb3rSQ3EfykQhHx_b8waRWhXolhcBNgHo 

signer=vZY2XY1RD9HIfWi8ift-1_DnHLDadZMWrufSh-_rKF0
```

## build

```sh
rebar3 compile
rebar3 device verify
rebar3 device package
```


## test

```sh
HB_PORT=0 rebar3 device test
rebar3 eunit-all
```

## license
this package is licensed under the [MIT License](./LICENSE)