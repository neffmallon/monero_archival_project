# Archival node instructions

This document contains information about the current configuration of our VPS-based archival nodes.

## Access

`$ ssh map@xxx.xxx.xxx.43 -p PORT` (e.g. for the Tokyo node) where the PORT is a secret port communicated by SerHack.

## Hostname

MAP-NAME-NUMBER

where :
* MAP stands for Monero Archivial Project
* NAME is the name of the nearest city where the node is (example TOKYO is TOKYO)
* NUMBER is the number of the node related to that city (int, it starts from 0)


## Layout

The regular and/or archival node binaries are stored in `~/monero_node/` 

The logs are stored in `~/.bitmonero`

## Operation

The monerod daemon lives in `~/monero_node/bin/monero-v0.12.3.0` 

Please start the daemon using the command: 

`./monerod --detach --log-level 0 --hide-my-port --show-time-stats 1`

(this is contained in `start_node_background.sh`)

## Misc notes

To watch the daemon output, run:
`$ tail -f ~/.bitmonero/bitmonero.log`

Uptime is important. If you are doing work or testing that will take archival nodes offline, please contain disruptions to the Tokyo server.

If you kill monerod, please restart it before exiting (instructions above)
