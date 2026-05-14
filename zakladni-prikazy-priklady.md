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

## 📂rm (remove)

**Definice:**
Odstraní soubor

**Poznámka:**
Nejjednodušší cesta smazání souborů (občas potřeba kombinase se sudo)

**Příklady:**
Chceš odstranit dalsidokument.docx z documents
```bash
root@rasberrypi:/home/user/documents$ ls
secret.mb dalsidokument.docx
root@rasberrypi:/home/user/documents$ rm dalsidokument.docx
root@rasberrypi:/home/user/documents$ ls
secret.mb
```

## 📂mkdir (make directory)

**Definice:**
Vytvoří novou složku

**Poznámka:**
Nejjednodušší cesta k vytvoření nové složky (občas potřeba kombinase se sudo)

**Příklady:**
Chceš vytvořit novou složku v user
```bash
root@rasberrypi:/home/user/documents$ cd ..
root@rasberrypi:/home/user$ ls
Pictures Videos  Documents dalsidokument.docx dokument.txt
root@rasberrypi:/home/user$ mkdir GitHub                        *vytvoří novou složku GitHub
root@rasberrypi:/home/user$ ls
Pictures  Videos  Documents dalsidokument.docx dokument.txt GitHub
```

## 📂rmdir (remove directory)

**Definice:**
Odstraní složku

**Poznámka:**
Nejjednodušší cesta smazání složky (občas potřeba kombinase se sudo)

**Příklady:**
Chceš odstranit složku Videos z user
```bash
root@rasberrypi:/home/user$ ls
Pictures Videos  Documents dalsidokument.docx dokument.txt GitHub
root@rasberrypi:/home/user$ rmdir Videos
root@rasberrypi:/home/user$ ls
Pictures Documents dalsidokument.docx dokument.txt GitHub              *uz tu Videos neni
```

## 📄echo (remove directory)

**Definice:**
Vypíše text do terminálu/vloží text do souboru

**Poznámka:**
Pokud chceš něco vypsat do terminálu nebo pokud chceš bez otevření přidat text do souboru

**Příklady:**
1. Chceš vypsat "Ahoj světe" do terminálu
```bash
root@rasberrypi:/home/user$ echo "Ahoj světe"
Ahoj světe
```
2. Chceš vložit text do souboru (přeprat celý soubor)
```bash
root@rasberrypi:/home/user/documents$ ls
secret.mb
root@rasberrypi:/home/user/documents$ cat secret.mb                *vypíše obsah souboru secret.mb
Super, naučil jsi se nový příkaz!
root@rasberrypi:/home/user/documents$ echo "Toto je nový text, už žádná pochvala" > secret.mb          *přepíše celý soubor na zadaný text  (pozor, rozdíl mezi > & >>)
root@rasberrypi:/home/user/documents$ cat secret.mb              *vypíše obsah přepsaného souboru secret.mb
Toto je nový text, už žádná pochvala                              *obsah přepsaného souboru secret.mb
```
3. Chceš vložit text do souboru (na konec souboru na další řádek)
```bash
root@rasberrypi:/home/user/documents$ ls
secret.mb
root@rasberrypi:/home/user/documents$ cat secret.mb                *vypíše obsah souboru secret.mb (ted uz zmeneny)
Toto je nový text, už žádná pochvala
root@rasberrypi:/home/user/documents$ echo "To ale neznamená, že se máš přestat učit!!" >> secret.mb          *vpíše na konec souboru zadaný text  (pozor, rozdíl mezi > & >>)
root@rasberrypi:/home/user/documents$ cat secret.mb              *vypíše obsah upraveného souboru secret.mb
Toto je nový text, už žádná pochvala
To ale neznamená, že se máš přestat učit!                          *obsah upraveného souboru secret.mb
```

## 🔑sudo (root)

**Teorie**
Pro nekteré akce, např. instalace, aktualizace je potřeba použít přístup root (pomocí příkazu sudo)

**Definice:**
Umožní spustit administrátorské akce (něco jako na Windows spustit jako zprávce)

**Poznámka:**
Sudo se používá na začátku příkazu který vyžaduje administrátorské oprávnění (aktualizace, instalace, přístup do systémových souborů)

**Příklady:**
1. Chceš nainstalovat aktualizace (nainstalované aplikace a balíčky)
```bash
root@rasberrypi:/home/user$ sudo apt update                      *zjištění nových balíčků (které jsou dostupné)
Please enter root pasworld:                                      *zadate root heslo (vaše heslo)
root@rasberrypi:/home/user$ sudo apt upgrade                     *reálně nainstaluje aktualizace všech nainstalovaných balíčků
```
2. Chceš nainstalovat nové aplikace & odistalovat
```bash
root@rasberrypi:/home/user$ sudo apt update
root@rasberrypi:/home/user$ sudo apt upgrade                      *projistotu pred instalací proveď předchozí vec (viz tady) aby to bylo aktuální)
root@rasberrypi:/home/user$ sudo apt install git                  *nainstaluje Git
root@rasberrypi:/home/user$ sudo apt install firefox              *nainstaluje prohlížeč firefox
**Funguje prakticky s čímkoli, případně hledej jak se co instaluje | pokaždé očekávej zadávání Root hesla!**
```

3. Chceš přístup do systémových souborů
```bash
root@rasberrypi:/home/user$ sudo rm /var/log/somefile.log
```

## 🗑️clear

**Definice:**
Používá se pro vyčištění terminálu (smaže úplně všechno, jako kdyby jste otevřeli nové okno)

**Poznámka:**
Používá se pokud chcete začít pracovat na novém projektu nebo když se váš terminál stává nepřehledným a máte zobrazené veci které nepotřebujete

**Příklady:**
Chceš si vyčistit terminál
```bash
**máte proste plnej terminal** (jedno čeho)
root@raspberrypi:/home/user$ apt update
root@raspberrypi:/home/user$ apt upgrade
root@raspberrypi:/home/user$ ls -la
root@raspberrypi:/home/user$ cd /etc
root@raspberrypi:/home/user$ cat config.txt
root@raspberrypi:/home/user$ mkdir test_folder
root@raspberrypi:/home/user$ rm -rf old_files
root@raspberrypi:/home/user$ systemctl status ssh
root@raspberrypi:/home/user$ ping google.com
root@raspberrypi:/home/user$ reboot
** a teď prostě dáte clear a všechno se maže a budete znovu na praznym promtu, zkus si sám! **
root@rasberrypi:/home/user$ clear
root@rasberrypi:/home/user$ *a tady normálně můžeš psát*
```

## 📜history

**Definice:**
Používá se pro zobrazení historie všech použitých příkazů v terminálu

**Poznámka:**
Udělá vám na obrazovku kompletní výpis všech použitých příkazů (pokud linux pouzíváš déle, bude to pár tisíc řádek, kombinuj s clear :) )

**Příklady:**
Chceš si vypsat historii příkazů z terminálu
```bash
root@rasberrypi:/home/user$ history
  ....
  555  mv test.rb linux-test.rb
  556  nano linux-test.rb
  557  sudo apt install cmatrix
  558  cmatrix
  559  sudo apt install cava
  560  cava
  561  exit
  562  cmatrix
  563  cava
  564  sudo apt install sl
  565  sl
  566  ls
  567  sl
  568  sudo apt install glances
  569  glances
  570  sudo apt install neofetch
  571  sl
  572  neofetcher
  ....
```

## 📜man

**Definice:**
Používá se pro zobrazení dokumentace příkazu

**Poznámka:**
Pokud znáš nějaký příkaz ale nevíš jak ho použít, nebo jsi na linuxu po delší době, tehle příkaz určitě využiješ:)

**Příklady:**
Potřebuješ zjistit jak se používá příkaz sudo (pokud by jsi to nechápal ode mě)
```bash
root@rasberrypi:/home/user$ man sudo
NAME
       sudo, sudoedit — execute a command as another user

SYNOPSIS
       sudo -h | -K | -k | -V
       sudo -v [-ABkNnS] [-g group] [-h host] [-p prompt] [-u user]
       sudo -l [-ABkNnS] [-g group] [-h host] [-p prompt] [-U user] [-u user] [command [arg ...]]
       sudo  [-ABbEHnPS]  [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-r role] [-t type]
            [-T timeout] [-u user] [VAR=value] [-i | -s] [command [arg ...]]
       sudoedit [-ABkNnS] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-r role] [-t type]
            [-T timeout] [-u user] file ...

DESCRIPTION
       sudo allows a permitted user to execute a command as the superuser or another user, as specified by the  secu‐
       rity  policy.   The invoking user's real (not effective) user-ID is used to determine the user name with which
       to query the security policy.
...
```

## 📜grep

**Definice:**
Používá se pro hledání textu v souboru

**Poznámka:**
Pokud potřebuješ najít text ve velkém souboru nebo jen nechceš otevírat nebo vypisovat soubor a zjistit, jestli se tam něo nachází nebo ne použij grep

**Příklady:**
Potřebuješ zjistit kde se nachází "Ahoj kamaráde" v souboru zprava.txt
```bash
root@rasberrypi:/home/user$ grep "Ahoj kamaráde" zprava.txt
**vyppíše kde se "Ahoj kamaráde" nachází**
```

## 🪪id

**Definice:**
Používá se pro zjískání informací o aktuálním uživateli systému

**Poznámka:**
Pokud potřebuješ zjistit detailní informace o aktuálním uživateli systému, použij tento příkaz a dozvíš se více než by jsi potřeboval

**Příklady:**
Potřebuješ zjistit aktuální informace o uživateli
```bash
root@rasberrypi:/home/user$ id
uid=1000(ed) gid=1000(ed) groups=1000(ed),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)    **např.
```
