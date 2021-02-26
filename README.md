# MaSVF Example

This is MaSVF Example, a small example [MaSVF wiki](https://github.com/peterkaminski/masvf-wiki).

[It does not present as a wiki at the link above, it just looks like a repository of Markdown files.  You need to use a MaSVF-ish tool to wikify it (see the "Specific Tool Support" section below); or, you can just read the Markdown and "follow" the links in double-brackets by hand.]

MaSVF is short for "Markdown and Shared Versioned Files". It is pronounced somewhere between "massive" and "massif".

This wiki consists of a few arbitrary pages taken from the [Creative Commons Wiki](https://wiki.creativecommons.org/wiki/Main_Page), for the purposes of illustrating a few interlinked pages of a normal wiki.  Please visit the Creative Commons Wiki for updated, complete content.

Not all features of the original MediaWiki pages were duplicated in this version, and there may have been link translation errors. Caveat lector.

The pages in MaSVF Example:

- [[CC0]]
- [[Cultivating the Public Domain]]
- [[Public domain]]
- [[Public Domain Symbol Version 1.0]]
- README (this page)
- [[United States]]

## Specific Tool Support

### Obsidian

Obsidian can read and write the files that comprise this wiki.  Sharing, syncing, and syndicating the wiki files with a MaSVF repo is not included in Obsidian's base features.

There is a third-party plugin, [Obsidian Git](https://github.com/denolehov/obsidian-git), to "backup your [Obsidian.md](https://obsidian.md/) vault to a remote git repository...".  There are also how-tos available on the web for syncing an Obsidian repo with a remote git respository.

Obsidian stores its settings and working metadata about the wiki in the `.obsidian` directory.  To facilitate MaSVF sharing via **git**, `.gitignore`  entries are used to create the directory as needed, and to avoid syndicating the settings and metadata.

### Gollum

Gollum can read and write the files that comprise this wiki.  Note that pages have to be committed via Git before Gollum will know about them.

This wiki contains a [[Home]] page specifically for Gollum.  The preferred home page for MaSVF wikis is [[README]].

If you are familiar with Docker, and you have cloned this repo from GitHub, you can quickly start a Gollum instance pointed to the current working directory with a command like this:

```shell
docker run --rm -v `pwd`:/wiki -p4567:4567 gollumorg/gollum --ref main
```

When Gollum is running, visit [http://localhost:4567/](http://localhost:4567/) (or other port as appropriate from your command).

Use Control-C to stop Gollum.

If you want to run Gollum detached, use the `-d` flag in the `run` command, and `docker stop <container_name>` to stop Gollum.  Find the container name with `docker ps`, or specify it in the `run` command with `--name`.
