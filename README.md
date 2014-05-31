MemSpikeFix
=====================

Fixes the memory spike which happens when large mods are enabled, which happens due to all mod assets being loaded to RAM regardless of them being used or not.

Most notably, this fixes the crash that may happen when large mods are enabled, due to the total RAM usage exceeding the available RAM (this is most notable in the Windows version of Don't Starve, since it is limited to using at most 2GB of RAM). This crash may present itself with one of the following errors (printed to log.txt):

	Error processing render buffer command GenerateMap

or

	ERROR: HWTexture::DeserializeTexture failed on MinimapBG. glGetError returned 0x505

or

	out of memory

but may also happen silently, with the game simply crashing with no meaningful information printed to log.txt.

As a side effect, this fix also prevents the large slowdown in the game's startup time caused by having large mods enabled.
