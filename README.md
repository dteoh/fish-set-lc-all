# fish-set-lc-all

Do you get errors like these?

```
Warning: Failed to set locale category LC_NUMERIC to en_JP.
Warning: Failed to set locale category LC_TIME to en_JP.
Warning: Failed to set locale category LC_COLLATE to en_JP.
Warning: Failed to set locale category LC_MONETARY to en_JP.
Warning: Failed to set locale category LC_MESSAGES to en_JP.
Warning: Failed to set locale category LC_NUMERIC to en_JP.
Warning: Failed to set locale category LC_TIME to en_JP.
Warning: Failed to set locale category LC_COLLATE to en_JP.
Warning: Failed to set locale category LC_MONETARY to en_JP.
Warning: Failed to set locale category LC_MESSAGES to en_JP.
```

This error happens because `en_JP` is not a valid locale. I think this mainly
affects people who use the English language on their OS, but live in a country
where English is not an official language, so we get stuck with a locale
construction not recognized by some programs.

This plugin sets the `LC_ALL` environment variable to `en_US.UTF-8`.

## Install

Assuming that you are using a fish shell plugin manager such as [Fisher][1]:

```
$ fisher install dteoh/fish-set-lc-all
```

... then start a new shell.

[1]: https://github.com/jorgebucaran/fisher
