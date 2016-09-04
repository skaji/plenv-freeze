# plenv freeze

This is a [plenv](https://github.com/tokuhirom/plenv) plugin,
that freeze/unfreeze your perl installations.

Sometimes, you may want to keep a perl installation vanilla,
which means you want to protect a perl installation against installation of CPAN modules.
If so, this plugin will help you.

This idea was originated by miyagawa, and I heard this from songmu.
See http://songmu.github.io/slides/gotandapm4/#6

## Install

```sh
$ git clone https://github.com/skaji/plenv-freeze ~/.plenv/plugins/plenv-freeze
```

## Usage

```sh
$ plenv freeze 5.24.0
Freezing 5.24.0 ... DONE

# You cannot install CPAN moduels to 5.24.0 anymore
$ plenv global 5.24.0
$ cpanm Plack
# FAIL!

# "unfreeze" 5.24.0, so that you can install CPAN modules to 5.24.0 again.
$ plenv unfreeze 5.24.0
Unfreezing 5.24.0 ... DONE

$ cpanm Plack
# OK
```

## Copyright and license

This software is copyright (c) 2016 by Shoichi Kaji <skaji@cpan.org>.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
