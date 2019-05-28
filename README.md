# ct_repo

A repo containing a collection of constant-time code I encountered in the wild (mostly comparison):

1. [tinyssh](https://github.com/janmojzis/tinyssh): file [sshcrypto_kex_curve25519.c](https://github.com/janmojzis/tinyssh/blob/e4db2a2181c104c7780e9f077923e2368a4386ee/tinyssh/sshcrypto_kex_curve25519.c), see function curve25519_dh()

2. [dropbear](https://github.com/mkj/dropbear): file [dbutil.c](https://github.com/mkj/dropbear/blob/d740dc548924f2faf0934e5f9a4b83d2b5d6902d/dbutil.c), see
function constant_time_memcmp()

3. [wireguard](https://github.com/WireGuard/WireGuard): file [memneq.c](https://github.com/WireGuard/WireGuard/blob/282eec313e6a46dac5fc9d279391b3177286381e/src/compat/memneq/memneq.c), see function \_\_crypto_memneq()

4. [NSS](https://github.com/nss-dev/nss): file [secport.c](https://github.com/nss-dev/nss/blob/30903daa5b544819ac3f233ceada392919096271/lib/util/secport.c), 
see function NSS_SecureMemcmpZero()

5. [libressl](https://github.com/libressl-portable/openbsd): file [timingsafe_memcmp.c](https://github.com/libressl-portable/openbsd/blob/8344ab14a2f6b4aa84db9a7076626906bfbc9645/src/lib/libc/string/timingsafe_memcmp.c), see function timingsafe_memcmp()

6. [libsodium](https://github.com/jedisct1/libsodium) : file [scalarmult_curve25519.c](https://github.com/jedisct1/libsodium/blob/cfb0f94704841f943a5a11d9e335da409c55d58a/src/libsodium/crypto_scalarmult/curve25519/scalarmult_curve25519.c), see function crypto_scalarmult_curve25519()

7. [openssl](https://github.com/openssl/openssl): file [cryptlib.c](https://github.com/openssl/openssl/blob/master/crypto/cryptlib.c), see 
function CRYPTO_memcmp(). Many others in file [constant_time_locl.h](https://github.com/openssl/openssl/blob/master/include/internal/constant_time_locl.h)

