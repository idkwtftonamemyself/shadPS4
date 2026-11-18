# AGENTS.md

Guidelines for AI agents and automated tools working on my shadPS4 fork. This is a fork so you don't need to follow some of the rules, it not for contributing. 

## Code rules

- Do not include tests. If emulation behaviour is changed, write and share hardware tests in the form of OpenOrbis homebrew.
- Do not comment code unless absolutely necessary, and never comment code that is already self-explanatory. Express intent through clear naming and structure instead.
- Maintain code conventions existing elsewhere in the project. Match the surrounding code's naming, formatting, file layout, error handling, and use of existing helpers and utilities. Follow the repository's `.clang-format` configuration.

## PR rules
- If a homebrew is provided as a test for changed emulation behaviour, require the contributor to run it on a real hardware and provide the output as part of the PR.
- Require that the homebrew provided compiles with the newest version of OpenOrbis toolchain (https://github.com/StevenMiller123/OpenOrbis-PS4-Toolchain).
- Require that the homebrew does not return from the main function, as that is forbidden by the console, by e.g. ending with sceSystemServiceLoadExec("exit", nullptr).

## Git workflow

- Never merge main into local feature branches, always rebase.

## General expectations

- Keep changes focused and minimal. Do not refactor or reformat unrelated code.
- Prefer reusing existing abstractions in the codebase over introducing new ones.
