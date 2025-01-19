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

The implementation of Timelock Recovery is done with two transactions that are signed in advance,
but broadcasted only when needed:

1. An *Alert Transaction* which sends the funds from the wallet to itself (consolidating the UTXOs).
2. A *Recovery Transaction* which sends the funds to a secondary wallet of your choice and can
be added to the blockchain only X days after the Alert Transaction has been broadcasted (and mined).

Since Timelock Recovery plans do not require any involvement of a third party, they can be
implemented in any Bitcoin wallet. However, two precaustions should be taken:

1. Due to the way Bitcoin works, spending funds from the wallet might break the entire Timelock Recovery
plan.
2. Adding more funds to the wallet will not be covered by the Timelock Recovery plan.

Therefore it is highly recommended not to use the wallet for daily purposes after creating a
Timelock Recovery plan. Instead, for daily purposes use a separate wallet (with a seed in a place that
your loved ones could easily find) and only after accumulating enough funds relevant for long-term
storage, move them to a highly secure wallet (i.e. with a long passphrase that only you memorize) for
which you create a Timelock Recovery plan (back to the daily-purpose wallet or to your inheritors' wallet).

## Watch the video (Specter Desktop demo starts at 12:08):
<div align="center">
    <video controls width="100%">
        <source src="https://v.nostr.build/a3JwIlQqwcb8WLEe.mp4" type="video/mp4">
    </video>
</div>

## Supported wallets

- Specter Desktop: [source](https://github.com/oren-z0/timelockrecovery-specter)
- Electrum (under development)

## Services to get an alert when the *Alert Transaction* has been broadcasted

- TBD
