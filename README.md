# webos tweaks

Soms simple tweaks for rooted WebOS LG TVs. For now I only have a simple init script
that blocks the default voice app (it uses ~190Mb of RAM even if you don't use it).

To install the init script(s), put them in:

/var/lib/webosbrew/init.d


Note that I had to use python2 since it is the only one installed...

## NOTE

For some reason the voice app automatically starts when you launch the home screen. I want to run a lightweight daemon in the
background that just kills the voice app whenever it is there... Surely it would be lighter than 190Mb.

Can I maybe replace /usr/bin/com.webos.app.voice safely with an empty shell script...?
