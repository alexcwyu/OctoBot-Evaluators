# Tentacles manager compatibility source

This LGPL-licensed source is [OctoBot-Tentacles-Manager 2.10.0](https://github.com/Drakkar-Software/OctoBot-Tentacles-Manager/tree/8c0fbebc4393739b498ef66d3170b2d7937049c3), commit `8c0fbebc4393739b498ef66d3170b2d7937049c3`. Current monorepo manager APIs require OctoBot-Commons 3.x and cannot replace this manager in the separately released Commons 1.10 library ecosystem.

Runtime repairs replace removed distutils version parsing with packaging.version.Version and close both scandir iterators on early matches instead of leaving generator-owned directory handles open. This fixes strict existing evaluator fixtures on current Python. Packaging uses an explicit `src` layout and current direct/optional dependencies, retaining the Commons 1.10 API constraint. Original license and copyright notices remain. Remove the compatibility source once a compatible upstream release includes the resource fix.
