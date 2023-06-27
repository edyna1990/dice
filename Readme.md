1 .Hogyan állítsuk be a git repo-t új gépen.

Először inicializáljuk a git-et a git init parancsel, hogy a git parancsokat futtathassuk.

>> git init

Következő lépés, hogy összekötjük a git repo-t, az adott gépen lévő mappával. A repo-hoz tartozó url a github-on a jobb felső zöld gomb "<>code" felirattal szedhető ki.

>> git remote add origin https://[TOKEN]@github.com/edyna1990/dice.git

Ha nem akarjuk a token-t beégetni (pl, idegen gépen dolgozunk), akkor csak í következő képpen adjuk meg. Viszont így minden push és pull request-nél meg kell adni a tokent.

>> git remote add origin https://token@github.com/edyna1990/dice.git

Innentől össze van kötve az adott mappa a git repóval, és pusholhatunk pullolhatunk.

2. Pull

Ha le akarjuk húzni az aktuális állapotot

git pull origin [branch neve]

A branch neve alapból master lesz

>> git pull origin master

3. Változtatások pusholása.

Ha le akarjuk kérni, hogy változott-e valami, akkor azt a status-al tehetjük meg.

>> git status

Ha semmit sem változott, akkor ezt kapjuk:
On branch master
nothing to commit, working tree clean

Egyébként kiírja hogy milyen fájlok változtak/jöttek létre

A pusholásnál először minden változtatást add-olni kell.

>> git add .

Addolás után commitoljuk a változtatásokat

>> git commit -m "[commit rovid leirasa]"

A commitnál kiírja, hogy hány sor került be és ki

Ezután pusholhatjuk a változtatásokat

>> git push origin master

Ha nem akarjuk, hogy az origin mastert meg kelljen adni, akkor adjuk meg a következő parancsot, amivel beállítjuk az alapértelmezett branchet

>> git branch --set-upstream-to=origin/master master

Nagyon szeretlek!