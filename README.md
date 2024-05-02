# community-pocs

* [Website](https://ronin-rb.dev)
* [Issues](https://github.com/ronin-rb/scripts/issues)
* [Discord](https://discord.gg/6WAb3PsVX9) |
  [Mastodon](https://infosec.exchange/@ronin_rb)

A community repository of PoC (Proof of Concept) exploits for [ronin-exploits].

## Install

This git repository can be installed by the [ronin-repos] command:

```shell
ronin-repos install https://github.com/postmodern/community-pocs.git
```

## Using

To list all installed exploits:

```shell
ronin-exploits list
```

To view metadata for a specific exploit:

```shell
ronin-exploits show <product>/CVE-YYYY-XXXX
```

To run an exploit from the repository:

```shell
ronin-exploits run <product>/CVE-YYYY-XXXX -p foo=bar ...
```

You can also run the exploit directly from the repository directory:

```shell
./exploits/<product>/CVE-YYYY-XXXX.rb -p foo=bar ...
```

## Requirements

* [ruby] >= 3.0.0
* [ronin-exploits] >= 1.1.0

[ruby]: https://www.ruby-lang.org/
[ronin-repos]: https://github.com/ronin-rb/ronin-repos#readme
[ronin-exploits]: https://github.com/ronin-rb/ronin-exploits#readme
