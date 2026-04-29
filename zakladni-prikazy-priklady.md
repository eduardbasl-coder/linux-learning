## ls (list)

**Definice:**  
Vypíše obsah aktuální složky  

**Poznámka:**  
Jeden ze základních a nejdůležitějších příkazů, používá se pořád  

**Příklad:**
```bash
root@raspberrypi:/home/user$ ls
Pictures  Videos  Documents
```

## cd (change directory)

**Definice:**
Změní adresář

**Poznámka:**
Jeden ze základních a možná nejdůležitější příkaz, používá se pro přesun mezi složkami, práci s daty a celovou orientaci na disku

**Příklady:**
```bash
root@raspberrypi:/home/user$ ls
Pictures  Videos  Documents
root@raspberrypi:/home/user$ cd Documents
root@raspberrypi:/home/user/documents$
```

## cd ..

**Definice:**
Změní adresář na předchozí úrověň

**Poznámka:**
Používá se při pohybu na předchozí úroveň dat, často používané, důležitý příkaz, každodenní použití (na příkladu zpátky z documents skočí na user)

**Příklady:**
```bash
root@raspberrypi:/home/user$ ls
Pictures  Videos  Documents
root@raspberrypi:/home/user$ cd Documents
root@raspberrypi:/home/user/documents$ cd ..
root@rasberrypi:/home/user$ 
```

## pwd (print working directory)

**Definice:**
Vypíše cestu k aktuálně používané složce/souboru

**Poznámka:**
Jeden ze základních příkazů, používá se při lokaci souboru a při zjišťování cesty ke kopírování a přesouvání souborů

**Příklady:**
```bash
root@raspberrypi:/home/user$ pwd
/bin/home/user
```

## cat

**Definice:**
Vypíše obsah souboru do Terminálu

**Poznámka:**
Používá se pokud potřebujete nehlédnout do souboru bez jeho otevření

**Příklady:**
```bash
root@raspberrypi:/home/user$ ls
Pictures  Videos  Documents
root@raspberrypi:/home/user/documents$ ls
dokument.txt secret.mb
root@raspberrypi:/home/user/documents$ cat secret.mb
Super, naučil jsi se nový příkaz!
```
