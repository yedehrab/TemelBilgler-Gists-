# Temel Git Komutları

### Git deposunu başlatma

```cmd
git init
```

> Git için gerkeli olan dosyaları oluşturur.

### Proje dosyalarımızın depoya eklenmesi

```cmd
git add .
```
> Bütün dosyalar (. dizindeki tüm dosyalar demektir.) eklenir.

### Teslim etme hazırlığı ve yorum ekleme

```cmd
git commit -m "Yorum" -m "Açıklama"
```
* -m: message anlamına gelmektedir.

> Mesaj ve açıklama ile ile depoya teslim için hazırlama

### Teslim edilecek URL'i belirleme

```cmd
git remote add origin [url]
```

* [url]: Yüklemek istediğimiz yerin adresi

> Github için, projenizin konumuna gelip, *download kısmındaki kopyalama resmine* basarak, projenizin url'ini kopyalabilirsiniz.

### Teslim Etme

```cmd
git push origin master
```

> Master olarak url'e yükleme işlemi

## Faydalı git komutları

Zaman zaman gerekebilecek git komutları

### Son hatalı yüklemeyi kaldırma

```cmd
gir reset HEAD~
```

> Son yüklemeyi kaldırır. Bu işlemden sonra tekrar commit etmeniz gerekmekte. Detay için [link](https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-commits-in-git)
