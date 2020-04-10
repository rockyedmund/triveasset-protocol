A colored coin address is a convenient representation of a Bitcoin address that will be used by colored coins wallets.
The colored coins address is derived similarly to the way a Bitcoin address (and colored [coins asset IDs](Asset ID)) are derived, only we use a different version number to get the address to start with the letter `C` (Mainnet) or `o` (Testnet).

### Mainnet
```
pk = PUBLIC KEY 
extended_ripemd = `0x1c`+RIPEMD-160(SHA-256(pk))
checksum = first 4 bytes of SHA-256(SHA-256(extended_ripemd))
Mainnet Colored Coin Address = Base58check(extended_ripemd+checksum)
```
where + means concatenation.

An example of such an address is 
```
CPGpvzGPWNmi68gLLVqSt4m3uV5hNCgwbj
```

### Testnet
```
pk = PUBLIC KEY 
extended_ripemd = `0x73`+RIPEMD-160(SHA-256(pk))
checksum = first 4 bytes of SHA-256(SHA-256(extended_ripemd))
Testnet Colored Coin Address = Base58check(extended_ripemd+checksum)
```
where + means concatenation.

An example of such an address is 
```
oJoZjQ8NmbM2LoqGp78413AsfDio36irmy
```