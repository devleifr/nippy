<a href="https://www.taoensso.com/clojure" title="More stuff by @ptaoussanis at www.taoensso.com"><img src="https://www.taoensso.com/open-source.png" alt="Taoensso open source" width="340"/></a>  
[**Documentation**](#documentation) | [Latest releases](#latest-releases) | [Get support][GitHub issues]

# Nippy

#### The fastest serialization library for Clojure

Clojure's rich data types are awesome. And its [reader](https://clojure.org/reference/reader) allows you to take your data just about anywhere. But the reader can be painfully slow when you've got a lot of data to crunch (like when you're serializing to a database).

Nippy is an attempt to provide a reliable, high-performance **drop-in alternative to the reader**.

Used by [Carmine](https://github.com/taoensso/carmine), [Faraday](https://github.com/ptaoussanis/faraday), [PigPen](https://github.com/Netflix/PigPen), [Onyx](https://github.com/onyx-platform/onyx), [XTDB](https://github.com/xtdb/xtdb), and others.

## Latest release/s

- `2023-08-02` `3.3.0-RC1` (dev): [changes](../../releases/tag/v3.3.0-RC1)
- `2022-07-18` `3.2.0` (stable):  [changes](../../releases/tag/v3.2.0)

[![Main tests][Main tests SVG]][Main tests URL]
[![Graal tests][Graal tests SVG]][Graal tests URL]

See [here][GitHub releases] for earlier releases.

## Why Nippy?

- Small, simple **all-Clojure** library
- **Terrific performance**: the [best](#performance) for Clojure that I'm aware of
- Comprehensive support for **all standard data types**
- Easily extendable to **custom data types**
- **Robust test suite**, incl. full coverage for every supported type
- Auto fallback to Java Serializable when available
- Auto fallback to Clojure Reader for all other types (including tagged literals
- Pluggable **compression** with built-in [LZ4](https://code.google.com/p/lz4/)
- Pluggable **encryption** with built-in AES128
- Tools for easy + robust **integration into 3rd-party libraries**, etc.

## Performance

Since its earliest versions, Nippy has consistently been the **fastest serialization library for Clojure** that I'm aware of. It offers:

- Roundtrip times **>12x faster** than `tools.reader` with **60% smaller** data size.
- Roundtrip times **>2x faster** than `data.fressian` with **30% smaller** data size.

![benchmarks-png](benchmarks.png)

The [benchmark code](https://github.com/taoensso/nippy/blob/master/src/taoensso/nippy/benchmarks.clj) can be easily run in your own environment.

## Documentation

- [Full documentation][GitHub wiki] (**getting started** and more)
- Auto-generated API reference: [Codox][Codox docs], [clj-doc][clj-doc docs]

## Funding

You can [help support][sponsor] on this project, thank you!! 🙏

## License

Copyright &copy; 2012-2023 [Peter Taoussanis][].  
Licensed under [EPL 1.0](LICENSE.txt) (same as Clojure).

<!-- Common -->

[GitHub releases]: ../../releases
[GitHub issues]:   ../../issues
[GitHub wiki]:     ../../wiki

[Peter Taoussanis]: https://www.taoensso.com
[sponsor]:          https://www.taoensso.com/sponsor

<!-- Project -->

[Codox docs]:   https://taoensso.github.io/nippy/
[clj-doc docs]: https://cljdoc.org/d/com.taoensso/nippy/

[Clojars SVG]: https://img.shields.io/clojars/v/com.taoensso/nippy.svg
[Clojars URL]: https://clojars.org/com.taoensso/nippy

[Main tests SVG]:  https://github.com/taoensso/nippy/actions/workflows/main-tests.yml/badge.svg
[Main tests URL]:  https://github.com/taoensso/nippy/actions/workflows/main-tests.yml
[Graal tests SVG]: https://github.com/taoensso/nippy/actions/workflows/graal-tests.yml/badge.svg
[Graal tests URL]: https://github.com/taoensso/nippy/actions/workflows/graal-tests.yml
