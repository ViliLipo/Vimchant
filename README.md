# Vimchant
This fork has been adapted to work with Ubuntu 20.4 and Neovim 0.4.4. 


## Original REAMDE
This is a mirror of http://www.vim.org/scripts/script.php?script_id=2345

Vim 7.0 introduced excellent spell-checking features which made external
spell-checker plugins pretty much obsolete. Unfortunately not all languages can
be supported through vims dictionary format. Either the language is
morphologically too complex or better custom solutions exist already for some
languagessolutions which are not compatible with vims spelling checker.
Finnish, for example, is a language which doesnt currently benefit from
vims spell-checking features.

This plugin (vimchant) provides a simple but fast on-the-fly spelling checker
which uses enchant as its back-end program. Enchant is a spell-checker library
and utility included in modern gnu/linux systems. Enchant itself is only a
front-end for many different spell-checkers, including voikko, zemberek,
hunspell, hspell, uspell, myspell, aspell and ispell. All the spell-checkers
and languages which can be supported through enchant are available to Vim
through this plugin.

Manual for vimchant is included, just type

    :help vimchant.txt

The most interesting commands are \ss (spell-checker on/off) and \sl (change language). The default interval period before running the spell-check is rather long (4 seconds). To make the spell-checker respond faster (1 second, for example) add the following line to your .vimrc file:

    set updatetime=1000

See the manual for more info. See also the Enchant homepage:

    http://www.abisource.com/projects/enchant/

## How to get up and running with Finnish spell checking in Neovim in Ubuntu 20.04

It is assumed that you have Neovim and Vim plug already installed.

```
apt install libenchant-2-2 libenchant-2-voikko voikko-fi
```

Add  `Plug 'ViliLipo/Vimchant'`, and `let g:vimchant_spellcheck_lang='fi'` to
your `~/.config/nvim/init.vim`
Then run Vim command `: source %` and `:PlugInstall`.
After that you can enable spell checking as described on the original REAMDE section.



