# little lu secret life

a [life series secret life](https://the-life-series.fandom.com/wiki/The_Life_Series_Wiki) server, ran using [the life series mod](https://modrinth.com/mod/life-series), with [velocity](https://papermc.io/software/velocity) / [simple voice chat](https://modrinth.com/plugin/simple-voice-chat/versions) etc.

using [itzg/docker-minecraft-server](https://github.com/itzg/docker-minecraft-server) and [itzg/docker-mc-proxy](https://github.com/itzg/docker-mc-proxy)

not really meant for contribs since this is basically just a place for me to put our sessions config in a space that's more than just my home server

but, it might be useful to you :)

---

things maybe to use:

- [polymania](https://github.com/Patbox/polymania)
- [nucleoidmc](https://github.com/NucleoidMC)
- [bluemap](https://bluemap.bluecolored.de/)
  - [world border](https://bluemap.bluecolored.de/community/WorldBorder.html)
- [mc-router](https://github.com/itzg/mc-router)
- [advanced portals](https://advancedportals.sekwah.com/)

---

technical notes:

while setting up simple voice chat, i had my port mappings setup to map 25577 inside the container to 25565, which i _think_ then basically reported to simple voice chat to make clients connect to 25577 for voice chat packets, which would fail to work obviously!

velocity is fine with just being put on 25565, i opted for that, and then voice chat started working, even though the internal server doesn't expose itself on any ports, yay
