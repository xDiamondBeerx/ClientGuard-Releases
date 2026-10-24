# ClientGuard downloads

Public downloads for ClientGuard. Plugin source and build logs are maintained in a separate private repository.

## Download

Get **BmcClientGuard.jar** from [Releases](https://github.com/xDiamondBeerx/ClientGuard-Releases/releases/latest). Requires **Paper/Purpur 26.2 and Java 25**. The checksum is provided as SHA256SUMS.txt.

Stop the server, install the JAR in plugins, and start the server. Keep only one ClientGuard JAR. The internal plugin/data folder name remains BmcClientGuard for compatibility.

## Use

Open `/cg`. Grant `bmcclientguard.staff` to staff members. Actual OPs can manage settings, tests and updates. New installations have Discord disabled; configure your own guild/channel before enabling it. No anticheat plugin is required. All plugin text is English.

ClientGuard recognizes available client/mod signals; it cannot guarantee a full installed mod list. Findings need staff review and do not prove a forbidden feature was used. No automatic bans are issued.

## Automatic updates

Version 1.12.0 and newer check this public repository after startup and every six hours. No user token is needed. OP Administration → Plugin updates controls checks and automatic downloads.

Verified updates are staged for the next normal server restart. ClientGuard does not restart the server or replace the running JAR. OPs receive a ready/available notice and one saved confirmation after an installed upgrade starts successfully. Notifications ON/OFF also controls these messages. Version tracking starts with 1.12.0; the initial installation does not invent an update receipt.

Back up plugin data before upgrading. Keep your current server API version compatible with the release requirements.
