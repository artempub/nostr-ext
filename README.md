### Nostr Signer

Use this to sign [Nostr](https://github.com/nostr-protocol/nostr) events on web-apps without having to give them your keys.


```
async window.nostr.getPublicKey(): string // returns your public key as hex
async window.nostr.signEvent(event): Event // returns the full event object signed
async window.nostr.getRelays(): { [url: string]: RelayPolicy } // returns a map of relays
async window.nostr.nip04.encrypt(pubkey, plaintext): string // returns ciphertext+iv as specified in nip04
async window.nostr.nip04.decrypt(pubkey, ciphertext): string // takes ciphertext+iv as specified in nip04
```

### Develop

To run the plugin from this code:

```
git clone https://github.com/fiatjaf/nos2x
cd nos2x
yarn
yarn run build
```

then

1. go to chrome://extensions;
2. ensure developer mode is enabled on the top right
3. click on Load unpackaged
4. select the extension folder of this repository
