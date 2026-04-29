## 📂ls (list)

**Definice:**  
Vypíše obsah aktuální složky  

**Poznámka:**  
Jeden ze základních a nejdůležitějších příkazů, používá se pořád  

**Příklad:**
```bash
root@rasberrypi:/home/user$ ls
Pictures  Videos  Documents
```

## 📂cd (change directory)

**Definice:**
Změní adresář

**Poznámka:**
Jeden ze základních a možná nejdůležitější příkaz, používá se pro přesun mezi složkami, práci s daty a celovou orientaci na disku

**Příklady:**
```bash
root@rasberrypi:/home/user$ ls
Pictures  Videos  Documents
root@rasberrypi:/home/user$ cd Documents
root@rasberrypi:/home/user/documents$
```

## 📂cd ..

**Definice:**
Změní adresář na předchozí úrověň

**Poznámka:**
Používá se při pohybu na předchozí úroveň dat, často používané, důležitý příkaz, každodenní použití (na příkladu zpátky z documents skočí na user)

**Příklady:**
```bash
root@raspberrypi:/home/user$ ls
Pictures  Videos  Documents
root@rasberrypi:/home/user$ cd Documents
root@rasberrypi:/home/user/documents$ cd ..
root@rasberrypi:/home/user$ 
```

## 📍pwd (print working directory)

**Definice:**
Vypíše cestu k aktuálně používané složce/souboru

**Poznámka:**
Jeden ze základních příkazů, používá se při lokaci souboru a při zjišťování cesty ke kopírování a přesouvání souborů

**Příklady:**
```bash
root@rasberrypi:/home/user$ pwd
/bin/home/user
```

## 📄cat

**Definice:**
Vypíše obsah souboru do Terminálu

**Poznámka:**
Používá se pokud potřebujete nehlédnout do souboru bez jeho otevření

**Příklady:**
```bash
root@raspberrypi:/home/user$ ls
Pictures  Videos  Documents
root@rasberrypi:/home/user/documents$ ls
dokument.txt secret.mb
root@rasberrypi:/home/user/documents$ cat secret.mb
Super, naučil jsi se nový příkaz!
```

## 📄touch

**Definice:**
Vytvoří nový soubor

**Poznámka:**
Používá se při vytváření nových souborů a pro pokročilejší pro aktualizaci času souboru

**Příklady:**
```bash
root@rasberrypi:/home/user/documents$ ls
dokument.txt secret.mb
root@rasberrypi:/home/user/documents$ touch dalsidokument.docx
root@rasberrypi:/home/user/documents$ ls
dokument.txt secret.mb dalsidokument.docx
```

## 📄nano

**Definice:**
Otevře soubor v jednoduchém textovém editoru nano, přípradně soubor i vytvoří

**Poznámka:**
Nejjednodušší a rychlá možnost pro editování textových souborů

**Příklady:**
```bash
root@rasberrypi:/home/user/documents$ ls
dokument.txt secret.mb dalsidokument.docx
root@rasberrypi:/home/user/documents$ nano dalsidokument.docx
*otevře jednoduchý editor, zkus si sám:)*
```

## 📂cp (copy)

**Definice:**
Nakopíruje soubor/složku z uvedeného zdroje do uvedeného cíle

**Poznámka:**
Nezbytné pro přesun (kopírování) souboru mezi adresářy/disky

**Příklady:**
Chceš nakopírovat dalsidokument.docx z documents do user
```bash
root@rasberrypi:/home/user$ ls
Pictures  Videos  Documents
root@rasberrypi:/home/user$ pwd
/bin/home/user         *sem chceme kopirovat
root@rasberrypi:/home/user$ cd documents
root@rasberrypi:/home/user/documents$ ls
dokument.txt secret.mb dalsidokument.docx
root@rasberrypi:/home/user/documents$ pwd
/bin/home/user/documents        *odtud kopirujes
root@rasberrypi:/home/user/documents$ cp /bin/home/user/documents/dalsidokument.docx /bin/home/user (cp ZDROJ CIL)
root@rasberrypi:/home/user/documents$ ls
dokument.txt secret.mb dalsidokument.docx   *dalsidokument tu pořád je
cd ..                  *skocime nahoru (do user)
root@rasberrypi:/home/user$ ls
Pictures  Videos  Documents dalsidokument.docx      *je i tady (jeho kopie)
```

## 📂mv (move)

**Definice:**
Přesune soubor/složku z uvedeného zdroje do uvedeného cíle

**Poznámka:**
Nezbytné pro přesun souboru mezi adresářy/disky

**Příklady:**
Chceš přesunout dokument.txt z documents do user
```bash
root@rasberrypi:/home/user$ ls
Pictures  Videos  Documents
root@rasberrypi:/home/user$ pwd
/bin/home/user         *sem chceme přesunout
root@rasberrypi:/home/user$ cd documents
root@rasberrypi:/home/user/documents$ ls
dokument.txt secret.mb dalsidokument.docx
root@rasberrypi:/home/user/documents$ pwd
/bin/home/user/documents        *odtud přesouváš
root@rasberrypi:/home/user/documents$ mv /bin/home/user/documents/dalsidokument.docx /bin/home/user (mv ZDROJ CIL)
root@rasberrypi:/home/user/documents$ ls
secret.mb dalsidokument.docx   *dokument.txt tu již není
cd ..          *skocime nahoru (do user)
root@rasberrypi:/home/user$ ls
Pictures  Videos  Documents dalsidokument.docx dokument.txt     *ale tady už je(sem jsme ho přesunuli)
```

