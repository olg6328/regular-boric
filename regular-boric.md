_I'd like to think this is a human-readable version of [regular-boric.json](/regular-boric.json)._

The expressions check for accented and unaccented versions of letters. Here I write the accented letters by default.

Presidents are listed in reverse chronological order. Presidents with the same first surnames are combined into one expression.

# Sebastián Piñera
Lines 4 to 31 of regular-boric.json
```
    {
      "repA": "/(Miguel\\s+Juan\\s+)?Sebasti.n\\s+Pi.era\\s+Echenique/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(Miguel\\s+Juan\\s+)?Sebasti.n\\s+Pi.era(?!\\s+Echenique)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Miguel\\s+Juan\\s+)?Sebasti.n\\s+)Pi.era(?!\\s+Echenique)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Pi.era\\s+)Echenique/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Miguel Juan Sebastián Piñera Echenique" or "Sebastián Piñera Echenique" to "Gabriel Boric Font"
  - `/(Miguel\s+Juan\s+)?Sebasti.n\s+Pi.era\s+Echenique/g`
- "Sebastián Piñera" to "Gabriel Boric"
  - `/(Miguel\s+Juan\s+)?Sebasti.n\s+Pi.era(?!\s+Echenique)/g`
- "Piñera" (on its own) to "Boric"
  - `/(?<!(Miguel\s+Juan\s+)?Sebasti.n\s+)Pi.era(?!\s+Echenique)/g`
- "Echenique" (on its own) to "Font"
  - `/(?<!Pi.era\s+)Echenique/g`

# Michelle Bachelet
Lines 32 to 59 of regular-boric.json
```
    {
      "repA": "/(Ver.nica\\s+)?Michelle\\s+Bachelet\\s+Jeria/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(Ver.nica\\s+)?Michelle\\s+Bachelet(?!\\s+Jeria)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Ver.nica\\s+)?Michelle\\s+)Bachelet(?!\\s+Jeria)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Bachelet\\s+)Jeria/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Verónica Michelle Bachelet Jeria" or "Mchelle Bachelet Jeria" to "Gabriel Boric Font"
  - `/(Ver.nica\s+)?Michelle\s+Bachelet\s+Jeria/g`
- "Michelle Bachelet" to "Gabriel Boric"
  - `/(Ver.nica\s+)?Michelle\s+Bachelet(?!\s+Jeria)/g`
- "Bachelet" (on its own) to "Boric"
  - `/(?<!(Ver.nica\s+)?Michelle\s+)Bachelet(?!\s+Jeria)/g`
- "Jeria" (on its own) to "Font"
  - `/(?<!Bachelet\s+)Jeria/g`

# Ricardo Lagos
Lines 60 to 87 of regular-boric.json
```
    {
      "repA": "/Ricardo\\s+(Froil.n\\s+)?Lagos\\s+Escobar/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Ricardo\\s+(Froil.n\\s+)?Lagos(?!\\s+Escobar)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Ricardo\\s+(Froil.n\\s+)?)Lagos(?!\\s+Escobar)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Lagos\\s+)Escobar/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Ricardo Froilán Lagos Escobar" or "Ricardo Lagos Escobar" to "Gabriel Boric Font"
  - `/Ricardo\s+(Froil.n\s+)?Lagos\s+Escobar/g`
- "Ricardo Lagos" to "Gabriel Boric"
  - `/Ricardo\s+(Froil.n\s+)?Lagos(?!\s+Escobar)/g`
- "Lagos" (on its own) to "Boric"
  - `/(?<!Ricardo\s+(Froil.n\s+)?)Lagos(?!\s+Escobar)/g`
- "Escobar" (on its own) to "Font"
  - `/(?<!Lagos\s+)Escobar/g`

# Eduardo Frei Ruiz-Tagle and Eduardo Frei Montalva
Lines 88 to 122 of regular-boric.json
```
    {
      "repA": "/Eduardo\\s+(Nicanor\\s+)?Frei\\s+Montalva|Eduardo\\s+(Alfredo\\s+Juan\\s+Bernardo\\s+)?Frei\\s+Ruiz.Tagle/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Eduardo\\s+Frei(?!(\\s+Montalva)|(\\s+Ruiz.Tagle))/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Eduardo\\s+(Nicanor\\s+)?)Frei\\s+Montalva|(?<!Eduardo\\s+(Alfredo\\s+Juan\\s+Bernardo\\s+)?)Frei\\s+Ruiz.Tagle/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Eduardo\\s+((Nicanor\\s+)|(Alfredo\\s+Juan\\s+Bernardo\\s+))?)Frei(?!(re)|(\\s+Ruiz.Tagle)|(\\s+Montalva))/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Frei\\s+)Montalva|(?<!Frei\\s+)Ruiz.Tagle/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx patterns: 
- "Eduardo Nicanor Frei Montalva" or "Eduardo Frei Montalva" or "Eduardo Alfredo Juan Bernardo Frei Ruiz-Tagle" or "Eduardo Frei Ruiz-Tagle" (with or without the hyphen) to "Gabriel Boric Font"
  - `/Eduardo\s+(Nicanor\s+)?Frei\s+Montalva|Eduardo\s+(Alfredo\s+Juan\s+Bernardo\s+)?Frei\s+Ruiz.Tagle/g`
- "Eduardo Frei" to "Gabriel Boric"
  - `/Eduardo\s+Frei(?!(\s+Montalva)|(\s+Ruiz.Tagle))/g`
- "Frei Montalva" or "Frei Ruiz-Tagle" (with or without the hyphen) to "Boric Font"
  - `/(?<!Eduardo\s+(Nicanor\s+)?)Frei\s+Montalva|(?<!Eduardo\s+(Alfredo\s+Juan\s+Bernardo\s+)?)Frei\s+Ruiz.Tagle/g`
- "Frei" (on its own) to "Boric"
  - `/(?<!Eduardo\s+((Nicanor\s+)|(Alfredo\s+Juan\s+Bernardo\s+))?)Frei(?!(re)|(\s+Ruiz.Tagle)|(\s+Montalva))/g`
  - Excludes instances of "Freire"
- "Montalva" or "Ruiz-Tagle" (with or without the hyphen) (both on their own) to "Font"
  - `/(?<!Frei\s+)Montalva|(?<!Frei\s+)Ruiz.Tagle/g`

# Patricio Aylwin
Lines 123 to 150 of regular-boric.json
```
    {
      "repA": "/(Miguel\\s+)?Patricio\\s+Aylwin\\s+Az.car/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(Miguel\\s+)?Patricio\\s+Aylwin(?!\\s+Az.car)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Miguel\\s+)?Patricio\\s+)Aylwin(?!\\s+Az.car)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Aylwin\\s+)Az.car/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Miguel Patricio Aylwin Azócar" or "Patricio Aylwin Azócar" to "Gabriel Boric Font"
  - `/(Miguel\s+)?Patricio\s+Aylwin\s+Az.car/g`
- "Patricio Aylwin" to "Gabriel Boric"
  - `/(Miguel\s+)?Patricio\s+Aylwin(?!\s+Az.car)/g`
- "Aylwin" (on its own) to "Boric"
  - `/(?<!(Miguel\s+)?Patricio\s+)Aylwin(?!\s+Az.car)/g`
- "Azócar" (on its own) to "Font"
  - `/(?<!Aylwin\s+)Az.car/g`

# Augusto Pinochet
Lines 151 to 178 of regular-boric.json
```
    {
      "repA": "/Augusto\\s+(Jos.\\s+Ram.n\\s+)?Pinochet\\s+Ugarte/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Augusto\\s+(Jos.\\s+Ram.n\\s+)?Pinochet(?!\\s+Ugarte)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Augusto\\s+(?:Jos.\\s+Ram.n\\s+)?)Pinochet(?!\\s+Ugarte)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Pinochet\\s+)Ugarte/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Augusto José Ramón Pinochet Ugarte" or "Augusto Pinochet Ugarte" to "Gabriel Boric Font"
  - `/Augusto\s+(Jos.\s+Ram.n\s+)?Pinochet\s+Ugarte/g`
- "Augusto Pinochet" to "Gabriel Boric"
  - `/Augusto\s+(Jos.\s+Ram.n\s+)?Pinochet(?!\s+Ugarte)/g`
- "Pinochet" (on its own) to "Boric"
  - `/(?<!Augusto\s+(?:Jos.\s+Ram.n\s+)?)Pinochet(?!\s+Ugarte)/g`
- "Ugarte" (on its own) to "Font"
  - `/(?<!Pinochet\s+)Ugarte/g`

# Salvador Allende
Lines 179 to 206 of regular-boric.json
```
    {
      "repA": "/Salvador\\s+(Guillermo\\s+)?Allende\\s+Gossens/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Salvador\\s+(Guillermo\\s+)?Allende(?!\\s+Gossens)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Salvador\\s+(?:Guillermo\\s+)?)Allende(?!\\s+Gossens)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Allende\\s+)Gossens/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Salvador Guillermo Allende Gossens" or "Salvador Allende Gossens" to "Gabriel Boric Font"
  - `/Salvador\s+(Guillermo\s+)?Allende\s+Gossens/g`
- "Salvador Allende" to "Gabriel Boric"
  - `/Salvador\s+(Guillermo\s+)?Allende(?!\s+Gossens)/g`
- "Allende" (on its own) to "Boric"
  - `/(?<!Salvador\s+(?:Guillermo\s+)?)Allende(?!\s+Gossens)/g`
- "Gossens" (on its own) to "Font"
  - `/(?<!Allende\s+)Gossens/g`

# Jorge Alessandri and Arturo Alessandri
Lines 207 to 241 of regular-boric.json
```
    {
      "repA": "/Arturo\\s+(Fortunato\\s+)?Alessandri\\s+Palma|Jorge\\s+(Eduardo\\s+)?Alessandri\\s+Rodr.guez/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/((Arturo\\s+)|(Jorge\\s+))Alessandri(?!(\\s+Palma)|(\\s+Rodr.guez))/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Arturo\\s+(Fortunato\\s+)?)Alessandri\\s+Palma|(?<!Jorge\\s+(Eduardo\\s+)?)Alessandri\\s+Rodr.guez/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Arturo\\s+)|(Jorge\\s+))Alessandri(?!(\\s+Palma)|(\\s+Rodr.guez))/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/((?<!Alessandri\\s+)|(?<!Montero\\s+))((Palma)|(Rodr.guez))/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx patterns: 
- "Arturo Fortunato Alessandri Palma" or "Arturo Alessandri Palma" or "Jorge Eduardo Alessandri Rodríguez" or "Jorge Alessandri Rodríguez" to "Gabriel Boric Font"
  - `/Arturo\s+(Fortunato\s+)?Alessandri\s+Palma|Jorge\s+(Eduardo\s+)?Alessandri\s+Rodr.guez/g`
- "Arturo Alessandri" or "Jorge Alessandri" to "Gabriel Boric"
  - `/((Arturo\s+)|(Jorge\s+))Alessandri(?!(\s+Palma)|(\s+Rodr.guez))/g`
- "Alessandri Palma" or "Alessandri Rodríguez" to "Boric Font"
  - `/(?<!Arturo\s+(Fortunato\s+)?)Alessandri\s+Palma|(?<!Jorge\s+(Eduardo\s+)?)Alessandri\s+Rodr.guez/g`
- "Alessandri" (on its own) to "Boric"
  - `/(?<!(Arturo\s+)|(Jorge\s+))Alessandri(?!(\s+Palma)|(\s+Rodr.guez))/g`
- "Palma" or "Rodríguez" (both on their own) to "Font"
  - `/((?<!Alessandri\\s+)|(?<!Montero\\s+))((Palma)|(Rodr.guez))/g`
  - Excludes instances of "Montero Rodríguez"

# Carlos Ibáñez del Campo
Lines 242 to 276 of regular-boric.json
```
    {
      "repA": "/Carlos\\s+Ib..ez\\s+[dD]el\\s+Campo/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Override",
      "active": true
    },
    {
      "repA": "/Carlos\\s+Ib..ez(?!\\s+[dD]el\\s+Campo)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Override",
      "active": true
    },
    {
      "repA": "/(?<!Carlos)Ib..ez\\s+[dD]el\\s+Campo/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Override",
      "active": true
    },
    {
      "repA": "/(?<!Carlos\\s+)Ib..ez(?!\\s+[dD]el\\s+Campo)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Override",
      "active": true
    },
    {
      "repA": "/(?<!Ib..ez\\s+)[dD]el\\s+Campo/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Override",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Carlos Ibáñez del Campo" (small or capital D) to "Gabriel Boric Font"
  - `/Carlos\s+Ib..ez\s+[dD]el\s+Campo/g`
- "Carlos Ibáñez" to "Gabriel Boric"
  - `/(?<!Carlos)Ib..ez\s+[dD]el\s+Campo/g`
- "Ibáñez del Campo" (small or capital D) to "Boric Font"
  - `/(?<!Carlos)Ib..ez\s+[dD]el\s+Campo/g`
- "Ibáñez" (on its own) to "Boric"
  - `/(?<!Carlos\s+)Ib..ez(?!\s+[dD]el\s+Campo)/g`
- "del Campo" (small or capital D) (on its own) to "Font"
  - `/(?<!Ib..ez\s+)[dD]el\s+Campo/g`

# Gabriel González Videla
Lines 277 to 311 of regular-boric.json
```
    {
      "repA": "/Gabriel\\s+(Enrique\\s+)?Gonz.lez\\s+Videla/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Gabriel\\s+(Enrique\\s+)?Gonz.lez(?!\\s+Videla)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Gabriel\\s+(Enrique\\s+)?)Gonz.lez\\s+Videla/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Gabriel\\s+)|(Santa\\s+Mar.a\\s+))Gonz.lez(?!\\s+Videla)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Gonz.lez\\s+)Videla/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Gabriel Enrique González Videla" or "Gabriel González Videla" to "Gabriel Boric Font"
  - `/Gabriel\s+(Enrique\s+)?Gonz.lez\s+Videla/g`
- "Gabriel González" to "Gabriel Boric"
  - `/Gabriel\s+(Enrique\s+)?Gonz.lez(?!\s+Videla)/g`
- "González Videla" to "Boric Font"
  - `/(?<!Gabriel\s+(Enrique\s+)?)Gonz.lez\s+Videla/g`
- "González" (on its own) to "Boric"
  - `/(?<!(Gabriel\s+)|(Santa\s+Mar.a\s+))Gonz.lez(?!\s+Videla)/g`
  - Excludes instances of "Santa María González"
- "Videla" (on its own) to "Font"
  - `/(?<!Gonz.lez\s+)Videla/g`

# Juan Antonio Ríos
Lines 312 to 339 of regular-boric.json
```
    {
      "repA": "/Juan\\s+Antonio\\s+R.os\\s+Morales/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Juan\\s+Antonio\\s+R.os(?!\\s+Morales)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Juan\\s+Antonio )R.os(?!\\s+Morales)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!R.os\\s+)Morales/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Juan Antonio Ríos Morales" to "Gabriel Boric Font"
  - `/Juan\s+Antonio\s+R.os\s+Morales/g`
- "Juan Antonio Ríos" to "Gabriel Boric"
  - `/Juan\s+Antonio\s+R.os(?!\s+Morales)/g`
- "Ríos" (on its own) to "Boric"
  - `/(?<!Juan\\s+Antonio )R.os(?!\\s+Morales)/g`
- "Morales" (on its own) to "Font"
  - `/(?<!R.os\\s+)Morales/g`

# Pedro Aguirre Cerda
Lines 340 to 374 of regular-boric.json
```
    {
      "repA": "/Pedro\\s+(Abelino\\s+)?Aguirre\\s+Cerda/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Pedro\\s+(Abelino\\s+)?Aguirre(?!\\s+Cerda)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Pedro\\s+(Abelino\\s+)?)Aguirre\\s+Cerda/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Pedro\\s+(Abelino\\s+)?)Aguirre(?!\\s+Cerda)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Aguirre\\s+)Cerda/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Pedro Abelino Aguirre Cerda" or "Pedro Aguirre Cerda" to "Gabriel Boric Font"
  - `/Pedro\s+(Abelino\s+)?Aguirre\s+Cerda/g`
- "Pedro Aguirre" to "Gabriel Boric"
  - `/Pedro\s+(Abelino\s+)?Aguirre(?!\s+Cerda)/g`
- "Aguirre Cerda" to "Boric Font"
  - `/(?<!Pedro\s+(Abelino\s+)?)Aguirre\s+Cerda/g`
- "Aguirre" (on its own) to "Boric"
  - `/(?<!Pedro\s+(Abelino\s+)?)Aguirre(?!\s+Cerda)/g`
- "Cerda" (on its own) to "Font"
  - `/(?<!Aguirre\s+)Cerda/g`

# Juan Esteban Montero
Lines 375 to 395 of regular-boric.json
```
    {
      "repA": "/Juan\\s+Esteban\\s+Montero\\s+Rodr.guez/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Juan\\s+Esteban\\s+Montero(?!\\s+Rodr.guez)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Juan\\s+Esteban\\s+)Montero(?!\\s+Rodr.guez)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Juan Esteban Montero Rodríguez" to "Gabriel Boric Font"
  - `/Juan\s+Esteban\s+Montero\s+Rodr.guez/g`
- "Juan Esteban Montero" to "Gabriel Boric"
  - `/Juan\s+Esteban\s+Montero(?!\s+Rodr.guez)/g`
- "Montero" (on its own) to "Boric"
  - `/(?<!Juan\s+Esteban\s+)Montero(?!\s+Rodr.guez)/g`
- "Rodríguez" (on its own) is already covered in "[Jorge Alessandri and Arturo Alessandri](#jorge-alessandri-and-arturo-alessandri)"

# Emiliano Figueroa
Lines 396 to 423 of regular-boric.json
```
    {
      "repA": "/(P.o\\s+)?Emiliano\\s+Figueroa\\s+Larra.n/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(P.o\\s+)?Emiliano\\s+Figueroa(?!\\s+Larra.n)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(P.o\\s+)?Emiliano\\s+)Figueroa(?!\\s+Larra.n)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Figueroa\\s+)Larra.n/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Pío Emiliano Figueroa Larraín" or "Emiliano Figueroa Larraín" to "Gabriel Boric Font"
  - `/(P.o\s+)?Emiliano\s+Figueroa\s+Larra.n/g`
- "Emiliano Figueroa" to "Gabriel Boric"
  - `/(P.o\s+)?Emiliano\s+Figueroa(?!\s+Larra.n)/g`
- "Figueroa" (on its own) to "Boric"
  - `/(?<!(P.o\s+)?Emiliano\s+)Figueroa(?!\s+Larra.n)/g`
- "Larraín" (on its own) to "Font"
  - `/(?<!Figueroa\s+)Larra.n/g`


# Juan Luis Sanfuentes
Lines 424 to 451 of regular-boric.json
```
    {
      "repA": "/Juan\\s+Luis\\s+Sanfuentes\\s+Andonaegui/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Juan\\s+Luis\\s+Sanfuentes(?!\\s+Andonaegui)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Juan\\s+Luis\\s+)Sanfuentes(?!\\s+Andonaegui)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Sanfuentes\\s+)Andonaegui/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Juan Luis Sanfuentes Andonaegui" to "Gabriel Boric Font"
  - `/Juan\s+Luis\s+Sanfuentes\s+Andonaegui/g`
- "Juan Luis Sanfuentes" to "Gabriel Boric"
  - `/Juan\s+Luis\s+Sanfuentes(?!\s+Andonaegui)/g`
- "Sanfuentes" (on its own) to "Boric"
  - `/(?<!Juan\s+Luis\s+)Sanfuentes(?!\s+Andonaegui)/g`
- "Andonaegui" (on its own) to "Font"
  - `/(?<!Sanfuentes\s+)Andonaegui/g`

# Ramón Barros Luco
Lines 452 to 486 of regular-boric.json
```
    {
      "repA": "/(Jos.\\s+)?Ram.n\\s+Barros\\s+Luco/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(Jos.\\s+)?Ram.n\\s+Barros(?!\\s+Luco)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Jos.\\s+)?Ram.n\\s+)Barros\\s+Luco/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Jos.\\s+)?Ram.n\\s+)Barros(?!\\s+Luco)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Barros\\s+)Luco/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "José Ramón Barros Luco" or "Ramón Barros Luco" to "Gabriel Boric Font"
  - `/(Jos.\s+)?Ram.n\s+Barros\s+Luco/g`
- "Ramón Barros" to "Gabriel Boric"
  - `/(Jos.\s+)?Ram.n\s+Barros(?!\s+Luco)/g`
- "Barros Luco" to "Boric Font"
  - `/(?<!(Jos.\s+)?Ram.n\s+)Barros\s+Luco/g`
- "Barros" (on its own) to "Boric"
  - `/(?<!(Jos.\\s+)?Ram.n\\s+)Barros(?!\\s+Luco)/g`
- "Luco" (on its own) to "Font"
  - `/(?<!Barros\s+)Luco/g`


# Pedro Montt, Jorge Montt and Manuel Montt
Lines 487 to 521 of regular-boric.json
```
    {
      "repA": "/Jorge\\s+Montt\\s+.lvarez|Pedro\\s+(El.as\\s+Pablo\\s+)?Montt\\s+Montt|Manuel\\s+(Francisco\\s+Antonio\\s+Juli.n\\s+)?Montt\\s+Torres/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Jorge\\s+Montt(?!\\s+.lvarez)|Pedro\\s+(El.as\\s+Pablo\\s+)?Montt(?!\\s+Montt)|Manuel\\s+(Francisco\\s+Antonio\\s+Juli.n\\s+)?Montt(?!\\s+Torres)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Jorge\\s+)Montt\\s+.lvarez|(?<!Pedro\\s+(El.as\\s+Pablo\\s+)?)Montt\\s+Montt|(?<!Manuel\\s+(Francisco\\s+Antonio\\s+Juli.n\\s+)?)Montt\\s+Torres/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Jorge\\s+)|(Pedro\\s+)|(?:Manuel\\s+))Montt(?!(\\s+.lvarez)|(\\s+Montt)|(\\s+Torres))/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Montt\\s+)((.lvarez)|(Torres))/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Jorge Montt Álvarez" or "Pedro Elias Pablo Montt Montt" or "Pedro Montt Montt" or "Manuel Francisco Antonio Julián Montt Torres" or "Manuel Montt Torres" to "Gabriel Boric Font"
  - `/Jorge\s+Montt\s+.lvarez|Pedro\s+(El.as\s+Pablo\s+)?Montt\s+Montt|Manuel\s+(Francisco\s+Antonio\s+Juli.n\s+)?Montt\s+Torres/g`
- "Jorge Montt" or "Pedro Montt" or "Manuel Montt" to "Gabriel Boric"
  - `/Jorge\s+Montt(?!\s+.lvarez)|Pedro\s+(El.as\s+Pablo\s+)?Montt(?!\s+Montt)|Manuel\s+(Francisco\s+Antonio\s+Juli.n\s+)?Montt(?!\s+Torres)/g`
- "Montt Álvarez" or "Montt Montt" or "Montt Torres" to "Boric Font"
  - `/(?<!Jorge\s+)Montt\s+.lvarez|(?<!Pedro\s+(El.as\s+Pablo\s+)?)Montt\s+Montt|(?<!Manuel\s+(Francisco\s+Antonio\s+Juli.n\s+)?)Montt\s+Torres/g`
- ""Montt" (on its own) to "Boric"
  - `/(?<!(Jorge\s+)|(Pedro\s+)|(?:Manuel\s+))Montt(?!(\s+.lvarez)|(\s+Montt)|(\s+Torres))/g`
- "Álvarez" or "Torres" (both on their own) to "Font"
  - `/(?<!Montt\s+)((.lvarez)|(Torres))/g`

# Germán Riesco Errázuriz
Lines 522 to 542 of regular-boric.json
```
    {
      "repA": "/Germ.n\\s+Riesco\\s+Err.zuriz/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Germ.n\\s+Riesco(?!\\s+Err.zuriz)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Germ.n\\s+)Riesco(?!\\s+Err.zuriz)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Germán Riesco Errázuriz" to "Gabriel Boric Font"
  - `/Germ.n\s+Riesco\s+Err.zuriz/g`
- "German Riesco" to "Gabriel Boric"
  - `/Germ.n\s+Riesco(?!\s+Err.zuriz)/g`
- "Riesco" (on its own) to "Boric"
  - `/(?<!Germ.n\s+)Riesco(?!\s+Err.zuriz)/g`
- "Errázuriz" (on its own) is replaced as "Boric" in [Federico Errázuriz Echaurren and Federico Errázuriz Zañartu](#federico_errázuriz_echaurren_and_federico_errázuriz_zañartu)

# Federico Errázuriz Echaurren and Federico Errázuriz Zañartu
Lines 543 to 577 of regular-boric.json
```
    {
      "repA": "/(Virginio\\s+)?Federico\\s+(Guillermo\\s+Rufino\\s+Arcadio\\s+Florentino\\s+Lamberto\\s+)?Err.zuriz\\s+Echaurren|Federico\\s+(Marcos\\s+[dD]el\\s+Rosario\\s+)?Err.zuriz\\s+Za.artu/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(Virginio\\s+)?Federico\\s+(Guillermo\\s+Rufino\\s+Arcadio\\s+Florentino\\s+Lamberto\\s+)?Err.zuriz(?!\\s+Echaurren)|Federico\\s+(Marcos\\s+[dD]el\\s+Rosario\\s+)?Err.zuriz(?!\\s+Za.artu)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Virginio\\s+)?Federico\\s+(Guillermo\\s+Rufino\\s+Arcadio\\s+Florentino\\s+Lamberto\\s+)?)Err.zuriz\\s+Echaurren|(?<!Federico\\s+(Marcos\\s+[dD]el\\s+Rosario\\s+)?)Err.zuriz\\s+Za.artu/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Virginio\\s+)?Federico\\s+(Guillermo\\s+Rufino\\s+Arcadio\\s+Florentino\\s+Lamberto\\s+)?)Err.zuriz(?!\\s+Echaurren)|(?<!Federico\\s+(Marcos\\s+[dD]el\\s+Rosario\\s+)?)Err.zuriz(?!\\s+Za.artu)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Err.zuriz\\s+)Echaurren|(?<!Err.zuriz\\s+)Za.artu/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Virginio Federico Guillermo Rufino Arcadio Florentino Lamberto Errázuriz Echaurren" or "Federico Errázuriz Echaurren" or "Federico Marcos del Rosario Errázuriz Zañartu" (small or capital D) or "Federico Errázuriz Zañartu" to "Gabriel Boric Font"
  - `/(Virginio\s+)?Federico\s+(Guillermo\s+Rufino\s+Arcadio\s+Florentino\s+Lamberto\s+)?Err.zuriz\s+Echaurren|Federico\s+(Marcos\s+[dD]el\s+Rosario\s+)?Err.zuriz\s+Za.artu/g`
- "Federico Errázuriz" to "Gabriel Boric"
  - `/(Virginio\s+)?Federico\s+(Guillermo\s+Rufino\s+Arcadio\s+Florentino\s+Lamberto\s+)?Err.zuriz(?!\s+Echaurren)|Federico\s+(Marcos\s+[dD]el\s+Rosario\s+)?Err.zuriz(?!\s+Za.artu)/g`
- "Errázuriz Echaurren" or "Errázuriz Zañartu" to "Boric Font"
  - `/(?<!(Virginio\s+)?Federico\s+(Guillermo\s+Rufino\s+Arcadio\\+Florentino\s+Lamberto\s+)?)Err.zuriz\s+Echaurren|(?<!Federico\s+(Marcos\s+[dD]el\s+Rosario\s+)?)Err.zuriz\s+Za.artu/g`
- "Errázuriz" (on its own) to "Boric"
  - `/(?<!(Virginio\s+)?Federico\s+(Guillermo\s+Rufino\s+Arcadio\s+Florentino\s+Lamberto\s+)?)Err.zuriz(?!\s+Echaurren)|(?<!Federico\s+(Marcos\s+[dD]el\s+Rosario\s+)?)Err.zuriz(?!\s+Za.artu)/g`
- "Echaurren" or "Zañartu" to "Font"
  - `/(?<!Err.zuriz\s+)Echaurren|(?<!Err.zuriz\s+)Za.artu/g`

# José Manuel Balmaceda
Lines 578 to 605 of regular-boric.json
```
    {
      "repA": "/(Jos.\\s+)?Manuel\\s+(Emiliano\\s+)?Balmaceda\\s+Fern.ndez/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(Jos.\\s+)?Manuel\\s+(Emiliano\\s+)?Balmaceda(?!\\s+Fern.ndez)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(Jos.\\s+)?Manuel\\s+(Emiliano\\s+)?)Balmaceda(?!\\s+Fern.ndez)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Balmaceda\\s+)Fern.ndez/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "José Manuel Emiliano Balmaceda Fernández" or "Jose Manuel Balmaceda Fernández" to "Gabriel Boric Font"
  - `/(Jos.\s+)?Manuel\s+(Emiliano\s+)?Balmaceda\s+Fern.ndez/g`
- "Jose Manuel Balmaceda" or "Manuel Balmaceda" to "Gabriel Boric"
  - `/(Jos.\s+)?Manuel\s+(Emiliano\s+)?Balmaceda(?!\s+Fern.ndez)/g`
- "Balmaceda" (on its own) to "Boric"
  - `/(?<!(Jos.\s+)?Manuel\s+(Emiliano\s+)?)Balmaceda(?!\s+Fern.ndez)/g`
- "Fernández" (on its own) to "Font"
  - `/(?<!Balmaceda\s+)Fern.ndez/g`

# Domingo Santa María
Lines 606 to 626 of regular-boric.json
```
    {
      "repA": "/Domingo\\s+Santa\\s+Mar.a\\s+Gonz.lez/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Domingo\\s+Santa\\s+Mar.a(?!\\s+Gonz.lez)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Domingo\\s+)Santa\\s+Mar.a(?!\\s+Gonz.lez)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Domingo Santa María González" to "Gabriel Boric Font"
  - `/Domingo\s+Santa\s+Mar.a\s+Gonz.lez/g`
- "Domingo Santa María" to "Gabriel Boric"
  - `/Domingo\s+Santa\s+Mar.a(?!\s+Gonz.lez)/g`
- "Santa María" (on its own) to "Boric"
  - `/(?<!Domingo\s+)Santa\s+Mar.a(?!\s+Gonz.lez)/g`
- "González" (on its own) is replaced as "Boric" in [Gabriel González Videla](#gabriel_gonzález_videla)

# Aníbal Pinto Garmendia and Francisco Pinto Díaz
Lines 627 to 661 of regular-boric.json
```
    {
      "repA": "/An.bal\\s+(Nicol.s\\s+)?Pinto\\s+Garmendia|Francisco\\s+(Antonio\\s+)?Pinto(?:\\s+y)?\\s+D.az(\\s+[dD]e\\s+[lL]a\\s+Puente)?/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/An.bal\\s+(Nicol.s\\s+)?Pinto(?!\\s+Garmendia)|Francisco\\s+(Antonio\\s+)?Pinto(?!((\\s+y)?\\s+D.az))/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!An.bal\\s+(Nicol.s\\s+)?)Pinto\\s+Garmendia|(?<!Francisco\\s+(Antonio\\s+)?)Pinto(\\s+y)?\\s+D.az(\\s+[dD]e\\s+[lL]a\\s+Puente)?/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!(An.bal\\s+(Nicol.s\\s+)?)|(Francisco\\s+(Antonio\\s+)?))Pinto(?!(\\s+Garmendia)|((\\s+y)?\\s+D.az))/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Pinto\\s+)((Garmendia)|(D.az(\\s+[dD]e\\s+[lL]a\\s+Puente)?))/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Aníbal Nicolás Pinto Garmendia" or "Aníbal Pinto Garmendia" or "Francisco Antonio Pinto y Díaz de la Puente" (optional "y", small or capital D and L) or "Francisco Pinto Díaz" to "Gabriel Boric Font"
  - `/An.bal\s+(Nicol.s\s+)?Pinto\s+Garmendia|Francisco\s+(Antonio\s+)?Pinto(?:\s+y)?\s+D.az(\s+[dD]e\s+[lL]a\s+Puente)?/g`
- "Aníbal Pinto" or "Francisco Pinto" to "Gabriel Boric"
  - `/An.bal\s+(Nicol.s\s+)?Pinto(?!\s+Garmendia)|Francisco\s+(Antonio\s+)?Pinto(?!((\s+y)?\s+D.az))/g`
- "Pinto Garmendia" or "Pinto Díaz" to "Boric Font"
  - `/(?<!An.bal\s+(Nicol.s\s+)?)Pinto\s+Garmendia|(?<!Francisco\s+(Antonio\s+)?)Pinto(\s+y)?\s+D.az(\s+[dD]e\s+[lL]a\s+Puente)?/g`
- "Pinto" (on its own) to "Boric"
  - `/(?<!(An.bal\s+(Nicol.s\s+)?)|(Francisco\s+(Antonio\s+)?))Pinto(?!(\s+Garmendia)|((\s+y)?\s+D.az))/g`
- "Garmendia" or "Díaz" or "Díaz de la Puente" (small or capital D and L) (both on their own) to "Font"
  - `/(?<!Pinto\s+)((Garmendia)|(D.az(\s+[dD]e\s+[lL]a\s+Puente)?))/g`


# José Joaquín Pérez
Lines 662 to 689 of regular-boric.json
```
    {
      "repA": "/Jos.\\s+Joaqu.n\\s+P.rez\\s+Mascayano/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Jos.\\s+Joaqu.n\\s+P.rez(?!\\s+Mascayano)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Jos.\\s+Joaqu.n\\s+)P.rez(?!\\s+Mascayano)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!P.rez\\s+)Mascayano/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "José Joaquín Pérez Mascayano" to "Gabriel Boric Font"
  - `/Jos.\s+Joaqu.n\s+P.rez\s+Mascayano/g`
- "José Joaquín Pérez" to "Gabriel Boric"
  - `/Jos.\s+Joaqu.n\s+P.rez(?!\s+Mascayano)/g`
- "Pérez" (on its own) to "Boric"
  - `/(?<!Jos.\s+Joaqu.n\s+)P.rez(?!\s+Mascayano)/g`
- "Mascayano" (on its own) to "Font"
  - `/(?<!P.rez\s+)Mascayano/g`


# Manuel Bulnes
Lines 690 to 710 of regular-boric.json
```
    {
      "repA": "/Manuel\\s+Bulnes\\s+Prieto/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Manuel\\s+Bulnes(?!\\s+Prieto)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Manuel\\s+)Bulnes(?!\\s+Prieto)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Manuel Bulnes Prieto" to "Gabriel Boric Font"
  - `/Manuel\s+Bulnes\s+Prieto/g`
- "Manuel Bulnes" to "Gabriel Boric"
  - `/Manuel\s+Bulnes(?!\s+Prieto)/g`
- "Bulnes" (on its own) to "Boric"
  - `/(?<!Manuel\s+)Bulnes(?!\s+Prieto)/g`
- "Prieto" (on its own) is replaced as "Boric" in [José Joaquín Prieto Vial](#josé_joaquín_prieto_vial) 

# Jose Joaquín Prieto
Lines 711 to 738 of regular-boric.json
```
    {
      "repA": "/(Jos.\\s+)?Joaqu.n\\s+Prieto\\s+Vial/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(Jos.\\s+)?Joaqu.n\\s+Prieto(?!\\s+Vial)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!((Jos.\\s+)?Joaqu.n\\s+))Prieto(?!\\s+Vial)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Prieto\\s+)Vial/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "José Joaquín Prieto Vial" or "Joaquín Prieto Vial" to "Gabriel Boric Font"
  - `/(Jos.\s+)?Joaqu.n\s+Prieto\s+Vial/g`
- "José Joaquín Prieto" or "Joaquín Prieto" to "Gabriel Boric"
  - `/(Jos.\s+)?Joaqu.n\s+Prieto(?!\s+Vial)/g`
- "Prieto" (on its own) to "Boric"
  - `/(?<!((Jos.\s+)?Joaqu.n\s+))Prieto(?!\s+Vial)/g`
- "Vial" (on its own) to "Font"
  - `/(?<!Prieto\s+)Vial/g`


# Ramón Freire
Lines 739 to 766 of regular-boric.json
```
    {
      "repA": "/Ram.n\\s+(Saturnino\\s+Andr.s\\s+)?Freire\\s+(y\\s+)?Serrano/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Ram.n\\s+(Saturnino\\s+Andr.s\\s+)?Freire(?!(\\s+y)?\\s+Serrano)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Ram.n\\s+(Saturnino\\s+Andr.s\\s+)?)Freire(?!(\\s+y)?\\s+Serrano)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Freire\\s+)Serrano/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
```
Changes and their corresponding RegEx: 
- "Ramón Saturnino Andrés Freire Serrano" or "Ramón Freire Serrano" to "Gabriel Boric Font"
  - `/Ram.n\s+(Saturnino\s+Andr.s\s+)?Freire\s+(y\\s+)?Serrano/g`
- "Ramón Freire" to "Gabriel Boric"
  - `/Ram.n\s+(Saturnino\s+Andr.s\s+)?Freire(?!(\s+y)?\s+Serrano)/g`
- ""Freire" (on its own) to "Boric"
  - `/(?<!Ram.n\s+(Saturnino\s+Andr.s\s+)?)Freire(?!(\s+y)?\s+Serrano)/g`
- "Serrano" (on its own) to "Font"
  - `/(?<!Freire\s+)Serrano/g`

# Manuel Blanco Encalada
Lines 767 to 801 of regular-boric.json
```
    {
      "repA": "/Manuel\\s+(Jos.\\s+)?Blanco(\\s+y\\s+Calvo\\s+[dD]e)?\\s+Encalada/g",
      "repB": "Gabriel Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/Manuel\\s+(Jos.\\s+)?Blanco(?!(\\s+y\\s+Calvo\\s+[dD]e)?\\s+Encalada)/g",
      "repB": "Gabriel Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Manuel\\s+(Jos.\\s+)?)Blanco(\\s+y\\s+Calvo\\s+[dD]e)?\\s+Encalada/g",
      "repB": "Boric Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Manuel\\s+(Jos.\\s+)?)Blanco(?!(\\s+y\\s+Calvo\\s+[dD]e)?\\s+Encalada)/g",
      "repB": "Boric",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    },
    {
      "repA": "/(?<!Blanco\\s+)((y\\s+)?Calvo\\s+[dD]e\\s+)?Encalada/g",
      "repB": "Font",
      "type": "RegEx",
      "case": "Maintain",
      "active": true
    }
```
Changes and their corresponding RegEx: 
- "Manuel José Blanco y Calvo de Encalada" (small or capital D) or "Manuel Blanco Encalada" to "Gabriel Boric Font"
  - `/Manuel\s+(Jos.\s+)?Blanco(\s+y\s+Calvo\s+[dD]e)?\s+Encalada/g`
- "Manuel Blanco" to "Gabriel Boric"
  - `/Manuel\s+(Jos.\s+)?Blanco(\s+y\s+Calvo\s+[dD]e)?\s+Encalada/g`
- "Blanco Encalada" to "Boric Font"
  - `(?<!Manuel\s+(Jos.\s+)?)Blanco(\s+y\s+Calvo\s+[dD]e)?\s+Encalada/g`
- ""Blanco" (on its own) to "Boric"
  - `/(?<!Manuel\s+(Jos.\s+)?)Blanco(?!(\s+y\s+Calvo\s+[dD]e)?\s+Encalada)/g`
- "y Calvo de Encalada" (optional "y", small or capital D) or "Encalada" (both on their own) to "Font"
  - `/(?<!Blanco\s+)((y\s+)?Calvo\s+[dD]e\s+)?Encalada/g`
