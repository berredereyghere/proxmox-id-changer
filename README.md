# Proxmox ID Changer

Een simpel script om snel het ID van een LXC container of VM aan te passen in Proxmox. Omdat de GUI hier geen directe knop voor heeft, automatiseert dit script het kloon- en verwijderproces.

### Wat doet het precies?
1. Checkt of het nieuwe ID nog vrij is.
2. Kijkt of de machine aanstaat. Zo ja, dan sluit hij deze netjes af.
3. Maakt een volledige kloon naar het nieuwe ID.
4. Verwijdert de oude machine (zodra de kloon gelukt is).
5. Start de nieuwe machine alleen op als de oude ook aanstond.

### Hoe gebruik je het?
Zorg dat je op je Proxmox node bent (via SSH of de console) en voer het volgende commando uit:

1. Cloned de repo en runt het script:
   `curl -sSL https://raw.githubusercontent.com/berredereyghere/proxmox-id-changer/main/change-id.sh | bash
`
