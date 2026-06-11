# `process-outbox@1.0`

HyperBEAM Forge package for AO process outbox and subscription behavior.

The package root device is `process-outbox@1.0`. It appends outbound messages to
`results/outbox`, forwards `x-` request keys into notices, and can fan out
notifications to subscribers registered by action and target.

## published package

```
device publish: process-outbox@1.0 
spec=JrNExiF73kCs6hCyxLXB8BmPzegJUAsO5BBKaHxI3hQ impl=IgFctN6dNiwIoQrONi__4trJ70bkamBXXp9ipyW3SQI
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
