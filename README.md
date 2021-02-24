# MaSVF Example

This is MaSVF Example, a small example wiki using MaSVF.

MaSVF is short for "Markdown and Shared Versioned Files". It is pronounced somewhere between "massive" and "massif".

This wiki consits of a few arbitrary pages taken from the [Creative Commons Wiki](https://wiki.creativecommons.org/wiki/Main_Page), for the purposes of illustrating a few interlinked pages of a normal wiki.  Please visit the Creative Commons Wiki for updated, complete content.

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