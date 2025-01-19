<div align="center">
    <img width="80" height="80" src="assets/logo160.png" alt="Timelock Recovery Logo" />
</div>

Timelock Recovery is a mechanism which, in case of a catastrophic event
(death or lose of your master key), can send your Bitcoin to a secondary wallet of your choice
within a time-window (i.e. 90 days).

During that time-window, you can see that the Timelock Recovery mechanism has been triggered (a
transaction from your wallet to itself is created on the Bitcoin blockchain), and if this
has happened against your will, you can use your master key to cancel the process (by moving
the funds elsewhere before the time-window expires).

## Watch the video (Specter Desktop demo starts at 12:08):
[![Watch the video](https://i.nostr.build/iinTjzc6TF4uAUj9.png)](https://v.nostr.build/a3JwIlQqwcb8WLEe.mp4)

## Supported wallets

- Specter Desktop: [source](https://github.com/oren-z0/timelockrecovery-specter)
- Electrum (under development)
