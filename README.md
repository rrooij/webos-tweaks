# webos tweaks

Soms simple tweaks for rooted WebOS LG TVs. For now I only have a simple init script
that blocks the default voice app (it uses ~190Mb of RAM even if you don't use it). And
recent research showed that it logs voice input of the user.

To install the init script(s), put them in:

/var/lib/webosbrew/init.d

Note that I had to use python2 since it is the only one installed...

## Init scripts

- 020-overwrite-bin overwrites the /usr/bin/com.webos.app.voice binary. It takes about 200Mb of memory and it is used
  to capture voice input, sometimes without the user knowing.
- 030-block-apps kills the voice app in case it already started
