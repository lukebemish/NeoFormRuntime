# NeoForm Runtime (NFRT)

This project implements a standalone commandline interface to create artifacts used to compile mods against Minecraft.
It is usually used as part of a Gradle plugin.

It uses data from the [NeoForm project](https://github.com/neoforged/NeoForm) to deobfuscate, merge and patch the
sources and finally recompile them.

Since it is used as part of the NeoForge toolchain, it extends NeoForm by adding direct support to
apply [NeoForge](https://github.com/neoforged/NeoForge) patches and produces the necessary artifacts to compile against
the NeoForge APIs.

## Examples

```
--use-eclipse-compiler --neoform "net.neoforged:neoform:1.20.6-20240429.153634@zip" --dist joined
```

## Usage

```
Usage: neoform-runtime [-hV] [--artifact-manifest=<artifactManifest>]
                       [--home-dir=<cacheDir>]
                       [--launcher-meta-uri=<launcherManifestUrl>] [--repository
                       [=<repositories>...]]... [COMMAND]
      --artifact-manifest=<artifactManifest>

  -h, --help      Show this help message and exit.
      --home-dir=<cacheDir>

      --launcher-meta-uri=<launcherManifestUrl>

      --repository[=<repositories>...]

  -V, --version   Print version information and exit.
Commands:
  run              Run the NeoForm engine and produce Minecraft artifacts
  download-assets  Download the client assets used to run a particular game
                     version
```
