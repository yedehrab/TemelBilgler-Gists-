# Heroku Git Komutları

[Buraya tıklayarak detaylı bilgileri alabilirsin](https://devcenter.heroku.com/articles/getting-started-with-nodejs)

## Bu komutların çalışması için heroku-cli'nin yüklü olması lazım

```cmd 
npm install -g heroku
```
> Npm üzerinden heroku yükleme işlemi


### Heroku'ya giriş yapma

```cmd
heroku login
```

> Email ve şifre istenecektir. Siteye kayıt olduğunuz bilgileri girin

### Depo (repository) kopyalama işlemi

```cmd
heroku git:clone -a [herokudaki uygulama adı] [kopyalanacağı dizin yolu]
cd [kopyalanacağı dizin yolu]
```

* herokudaki uygulama adı: mytempsite
* kopyalanacağı dizin yolu: C:\Desktop\Temp

> Heroku'da bulunan uygulamayı istediğimiz dizinin içine kopyalıyoruz. Sonrasında kopyalama işleminin olduğu dizine giriyoruz.

### Değişiklikleri karşıya yükleme

```cmd
git add .
git commit -am "Mesaj"
git push heroku master
```

> Değişkliklikler heroku uygulmamıza eklenecektir.

### Uygulamayı başlatma

```cmd
heroku open
```

### Ek not

> Heroku aldığı node.js uygulamasındaki **start scriptini** çalıştırır. Yani "npm run start" komutunu işler.
> Bu sebeple **package.json** dosyası olmak zorunda ve **start scriptini** içermek zorundadır.

Örnek package.json dosyası 

```javascript
{
  "name": "temp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "directories": {
    "lib": "lib"
  },
  "scripts": {
    "start": "node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
```