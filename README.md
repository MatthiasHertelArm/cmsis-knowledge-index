# CMSIS knowledge index

Releases of the core knowledge index that the
[CMSIS Developer Assistant](https://github.com/Open-CMSIS-Pack/CMSIS-Developer-Assistant)
ships as `resources/knowledge/core.db`. This repository holds no sources; it
only publishes the index.

Each release `core-<version>` has four assets:

| Asset | Content |
| --- | --- |
| `knowledge-core-<version>.db` | The index, an SQLite database |
| `knowledge-core-<version>.json` | Its build record: units, nodes, edges, licences, size and sha256 |
| `knowledge-core-<version>.sha256` | The hash of the database, `shasum -a 256` format |
| `SOURCES.md` | Every source of the index with its repository, licence and what was taken, and the copyright lines and licence texts the licences require |

The index is built only from public sources under open licences (Apache-2.0,
BSD-3-Clause, MIT) and from own summaries of public GitHub issues. Each unit is
under the licence of its source, as `SOURCES.md` lists it.

The extension pins one release in `resources/knowledge/core.lock.json`:
`npm run knowledge:update -- <version>` pins a release, and
`npm run knowledge:fetch` downloads it and checks its size and sha256.
