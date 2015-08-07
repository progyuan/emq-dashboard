
## Overview

Dashboard for emqttd broker.

## Build

In emqttd project:

```
git submodule add https://github.com/emqtt/emqttd_dashboard.git plugins/emqttd_dashboard 

make
```

## Configure

```
[
  {emqttd_dashboard, [
    {listener, 
        {emqttd_dashboard, 18083, [
            {acceptors, 4},
            {max_clients, 512}]}}
  ]}
].
```

## Load Plugin

```
./bin/emqttd_ctl load emqttd_dashboard
```

