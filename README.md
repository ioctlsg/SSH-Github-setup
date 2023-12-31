# SSH-Github-setup for MacOS

1) cd ~   // go to home directory
2) mkdir .ssh // make default ssh directory for key and config
3) ssh-keygen -t rsa -b 4096 -C "{I.am.so.cool@your.email.com}" // create rsa key pair

```bash
The key fingerprint is:
SHA256:iMHGJn4XkVaJaIfmtA88wV88888888YeyLSTOxcZU {I.am.so.cool@your.email.com}
The key's randomart image is:
+---[RSA 4096]----+
|   o.o.+..       |
|   +X =..  .     |
|  oO*s=.  E      |
| o.aa*o o.       |
|  o ++=.S aa     |
|   + ..=+        |
|    . Xoqa       |
|     * Xo        |
|      *...       |
+----[SHA256]-----+
```

4) ls ~./ssh  // check if keypair is created
5) ssh-add ~/.ssh/id_rsa // add to your ssh
```bash
Identity added: /Users/iamsocool/.ssh/id_rsa ({I.am.so.cool@your.email.com})
```
6) less id_rsa.pub // copy your pub key to https://github.com/settings/keys
7) ssh -T git@github.com //test ssh key with github

```bash
The authenticity of host 'github.com (100.200.300.400)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbp88888880zPMSvHdkr4UvCOqU.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
Hi ioctlsg! You've successfully authenticated, but GitHub does not provide shell access.
```

Done! - now go do all you ssh git clones with ssh! enjoy.
