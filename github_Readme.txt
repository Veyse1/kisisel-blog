# Git ve GitHub Kullanimi

Universitede proje yaparken ayni dosyanin bir suru versiyonu ortaya cikiyor.
`final.c`, `final2.c`, `final_son.c` gibi seyler. Bir noktadan sonra hangi dosya guncel karisiyor.
Bu problemi cozmek icin gelistiriciler **Git** kullanir.

Git kod degisikliklerini takip eden bir version control sistemidir.
Projede yapilan tum degisiklikleri kaydeder ve eski surumlere donmeye imkan verir.

Projeleri internet uzerinde saklamak ve paylasmak icin en yaygin platform ise
GitHub’dur.

Git sistemi 2005 yilinda Linux cekirdeginin yaraticisi
Linus Torvalds tarafindan gelistirilmistir.


## Git Temel Kavramlari

**Repository (Repo)**
Projenin bulundugu klasordur. Git tum gecmisi burada saklar.

**Commit**
Projede yapilan degisikliklerin kaydidir.

**Branch**
Projenin farkli bir gelistirme koludur. Yeni ozellikler genelde ayri bir branch'te gelistirilir.

**Merge**
Iki farkli branch’i birlestirme islemi.

**Remote Repository**
Internette bulunan repo (genelde GitHub).

---

## Git Kurulumu

Linux:

```bash
sudo apt install git
```

Mac:

```bash
brew install git
```

Windows icin:
https://git-scm.com/downloads

Kurulumu kontrol etmek icin:

```bash
git --version
```

---

## Yeni Bir Git Projesi Baslatma

Once bir klasor olusturulur.

```bash
mkdir proje
cd proje
```

Git deposu baslatilir.

```bash
git init
```

Bu komut klasoru Git repository haline getirir.

---

## Dosya Ekleme ve Commit

Bir dosya olusturalim.

```bash
touch main.c
```

Git'in durumunu kontrol etmek icin:

```bash
git status
```

Dosyayi Git'e ekleyelim.

```bash
git add main.c
```

Degisikligi kaydedelim.

```bash
git commit -m "ilk commit"
```

Bu noktadan sonra Git degisikligi kaydetmis olur.

---

## Branch Kullanimi

Yeni bir branch olusturmak icin:

```bash
git branch feature
```

Branch degistirmek icin:

```bash
git switch feature
```

Tekrar ana branche donmek icin:

```bash
git switch main
```

Branch birlestirme:

```bash
git merge feature
```

---

## GitHub ile Baglanti

GitHub'da once bir repo olusturulur.

https://github.com

Yerel projeyi GitHub’a baglamak icin:

```bash
git remote add origin https://github.com/kullanici/proje.git
```

Projeyi GitHub’a gondermek icin:

```bash
git push -u origin main
```

---

## Repo Klonlama

Bir projeyi indirmek icin kullanilan komut:

```bash
git clone https://github.com/kullanici/proje.git
```

Bu komut projeyi indirir ve Git gecmisini de getirir.

---

## Degisiklikleri Guncelleme

GitHub’daki son degisiklikleri almak icin:

```bash
git pull
```

---

## Gunluk Git Kullanimi

Genelde gelistiriciler su sekilde calisir:

```bash
git pull
git add .
git commit -m "degisiklik"
git push
```

---

## Faydalı Komutlar

Commit gecmisi:

```bash
git log
```

Kisa commit gecmisi:

```bash
git log --oneline
```

Dosyalar arasindaki farki gormek:

```bash
git diff
```

Bir commit’i geri almak:

```bash
git revert <commit-id>
