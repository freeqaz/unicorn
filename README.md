Unicorn Engine
==============

## freeqaz fork

This is a fork of [unicorn-engine/unicorn](https://github.com/unicorn-engine/unicorn),
maintained by [freeqaz](https://github.com/freeqaz) in support of the
[milohax](https://github.com/milohax) decomp-synth work (byte-exact
decompilation matching for Rock Band 3 / Dance Central 3, which target
PowerPC). The canonical push target for this fork's `master` is
[freeqaz/unicorn](https://github.com/freeqaz/unicorn); upstream is tracked
read-only via the `upstream` remote for pulling in updates.

Changes since upstream, grouped thematically:

- **PPC64 support**: enabled `UC_MODE_PPC64` (previously stubbed out as
  unsupported), switched the default PPC64 CPU model from POWER10 to 970
  v2.2, and added PPC64 unit tests (64-bit registers, FP, syscalls,
  loads/stores, SPRs) plus a PPC64 sample and Python/Rust binding tests.
- **Test cleanup**: aligned the PPC64 test style with the existing PPC32
  conventions.
- **CI fix**: bumped the pinned LizardByte `setup_python` action to
  unblock macOS-14 arm64 and Windows AMD64 wheel-build jobs that started
  failing after runner image updates removed the old Python versions.

[![pypi downloads](https://pepy.tech/badge/unicorn)](https://pepy.tech/project/unicorn)
[![Fuzzing Status](https://oss-fuzz-build-logs.storage.googleapis.com/badges/unicorn.svg)](https://bugs.chromium.org/p/oss-fuzz/issues/list?sort=-opened&can=1&q=proj:unicorn)

**LOOKING FOR CONTRIBUTORS!** See [this](https://github.com/unicorn-engine/unicorn/issues/2237).
==============

<p align="center">
<img width="250" src="docs/unicorn-logo.png">
</p>

Unicorn is a lightweight, multi-platform, multi-architecture CPU emulator framework, based on [QEMU](http://qemu.org).

Unicorn offers some unparalleled features:

- Multi-architecture: ARM, ARM64 (ARMv8), M68K, MIPS, PowerPC, RISCV, SPARC, S390X, TriCore and X86 (16, 32, 64-bit)
- Clean/simple/lightweight/intuitive architecture-neutral API
- Implemented in pure C language, with bindings for Crystal, Clojure, Visual Basic, Perl, Rust, Ruby, Python, Java, .NET, Go, Delphi/Free Pascal, Haskell, Pharo, Lua and Zig.
- Native support for Windows & *nix (with Mac OSX, Linux, Android, *BSD & Solaris confirmed)
- High performance via Just-In-Time compilation
- Support for fine-grained instrumentation at various levels
- Thread-safety by design
- Distributed under free software license GPLv2

Further information is available at http://www.unicorn-engine.org


License
-------

This project is released under the [GPL license](COPYING).


Compilation & Docs
------------------

See [docs/COMPILE.md](docs/COMPILE.md) file for how to compile and install Unicorn.

More documentation is available in [docs/README.md](docs/README.md).

For common questions, read [docs/FAQ.md](docs/FAQ.md) before raising an issue.

Contact
-------

[Contact us](http://www.unicorn-engine.org/contact/) via mailing list, email or twitter for any questions.


Join [our group](https://t.me/+lnNl0fPpyCYzZmVh) for instant feedback.

Contribute
----------

If you want to contribute, please pick up something from our [Github issues](https://github.com/unicorn-engine/unicorn/issues).

We also maintain a list of more challenged problems in [milestones](https://github.com/unicorn-engine/unicorn/milestones) for our regular release.

Please send pull request to our [dev branch](https://github.com/unicorn-engine/unicorn/tree/dev).

[CREDITS.TXT](CREDITS.TXT) records important contributors of our project.
