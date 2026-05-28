# Amstrad PPC XT CF Lite
Internal CF interface for the Amstrad PPC512/640.<br>

Replaces the internal modem board with a combination ISA interface & XT-IDE/Compact Flash interface.<br> 

Heavily based on [Sergey Kiselev's design](https://github.com/skiselev/xt-cf-lite-v4).<br>

Which is apparently a remake of [James Pearce's card](http://www.lo-tech.co.uk/wiki/XT-CF-lite).<br>

Changes requires for internal mounting in the Amstrad PPC:<br>
[1] The following signals are generated directly from the internal gate arrays and should be buffered with a non-inverting buffer (i.e. 72HC244): A00 to A07, ~MEMW, ~MEMR, ~IOW, ~IOR, RESET _(there are others but irrelevant for our purposes)_<br>
[2] The data signals (D0 to D7) are at CMOS levels and should be pulled up to TTL levels with 10KΩ resistors<br>
[3] The internal modem board we are replacing is roughly 200x120mm<br>
[4] Technically the PPC should be powered by the "expansion unit" and not the other way around ... don't tell anyone<br>

Currently untested ...<br><br>
![Amstrad_PPC_Internal_Modem](Amstrad_PPC_Internal_modem.png)
![Amstrad_PPC_Internal_CF_Lite](Amstrad_PPC_Internal_PCB.png)
