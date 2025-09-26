# muncs craft

a minecraft server, with:
- [velocity](https://papermc.io/software/velocity), so there can be multiple logical 'servers' if need be
- [simple voice chat](https://modrinth.com/plugin/simple-voice-chat/versions), for proximity voice chat, also works cross server

using [itzg/docker-minecraft-server](https://github.com/itzg/docker-minecraft-server) and [itzg/docker-mc-proxy](https://github.com/itzg/docker-mc-proxy)

---

things maybe to use:

- [polymania](https://github.com/Patbox/polymania)
- [nucleoidmc](https://github.com/NucleoidMC)
- [bluemap](https://bluemap.bluecolored.de/)
- [mc-router](https://github.com/itzg/mc-router)
- [advanced portals](https://advancedportals.sekwah.com/)

---

technical notes:

while setting up simple voice chat, i had my port mappings setup to map 25577 inside the container to 25565, which i _think_ then basically reported to simple voice chat to make clients connect to 25577 for voice chat packets, which would fail to work obviously!

velocity is fine with just being put on 25565, i opted for that, and then voice chat started working, even though the internal server doesn't expose itself on any ports, yay

