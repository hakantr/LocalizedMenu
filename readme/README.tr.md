### LocalizedMenu
Sublime Text 2/3/4 Son Kullanıcı için Yerelleştirme Aracı ve Yerelleştirilmiş Menü

- Yeni diller eklemek için kolay bir yol sağlar
- Birden fazla sürüm/platformu destekler
- Ortak menüleri paylaşmayı destekler
- Yerel menülerin otomatik yedeğini alır
- Yeni sürüm İngilizce menülerini otomatik olarak açar

### README.md
- de_DE [Almanca](readme/README.de_DE.md)
- en [İngilizce](README.md)
- es_ES [İspanyolca](readme/README.es_ES.md)
- fr_FR [Fransızca](readme/README.fr_FR.md)
- hu [Macarca](readme/README.hu.md)
- hy [Ermenice](readme/README.hy.md)
- pt_BR [Brezilya Portekizcesi](readme/README.pt_BR.md)
- ru [Rusça](readme/README.ru.md)
- sv_SE [İsveççe](readme/README.sv_SE.md)
- tr [Türkçe](readme/README.tr.md)
- zh_CN [Basitleştirilmiş Çince](readme/README.zh_CN.md)
- zh_TW [Geleneksel Çince](readme/README.zh_TW.md)

### Bu proje ayrıca şu adreslerde barındırılmaktadır:
- [GitHub](https://github.com/zam1024t/LocalizedMenu)
- [Gitee](https://gitee.com/zam1024t/LocalizedMenu)

### Ekran Görüntüleri
#### Windows'da Çalışır
![Windows'da Çalışır](https://raw.githubusercontent.com/zam1024t/LocalizedMenu/shots/shots/LocalizedMenu_win.gif)
#### OS X'de Çalışır
![OS X'de Çalışır](https://raw.githubusercontent.com/zam1024t/LocalizedMenu/shots/shots/LocalizedMenu_osx.gif)
#### Ubuntu'da Çalışır
![Ubuntu'da Çalışır](https://raw.githubusercontent.com/zam1024t/LocalizedMenu/shots/shots/LocalizedMenu_linux.gif)

### Kurulum
- Paket Kontrolü ile
	- [Paket Kontrolü](https://packagecontrol.io/installation) yükleyin
	- `LocalizedMenu` arayın
- Manuel olarak
	- [master.zip](https://github.com/zam1024t/LocalizedMenu/archive/master.zip) indirin, `Packages` klasörüne açın, ardından `LocalizedMenu-master` klasörünü `LocalizedMenu` olarak yeniden adlandırın
	- `Packages` klasörüne git kopyalayın
  ```bash
  git clone https://github.com/zam1024t/LocalizedMenu
  ```

### Kullanım
- Menüden değiştirme
	- `Preference` -> `Languages` yoluyla
- Komut panelinden değiştirme
	- `Ctrl+Shift+P` tuşlarına basın, `lmxx` (*xx* yerel koddur) yazarak değiştirin

### Bir Dil Ekleyin
- `locale/en/en.json` dosyasını `locale/<locale>/<locale>.json` olarak kopyalayın, dilinize göre yerelleştirin
- `menu/<version>/en/*` dosyalarını `menu/<version>/<locale>/*` olarak kopyalayın, dilinize göre yerelleştirin
- Örneğin, şimdi Sublime Text Build 3999 için `my` adlı bir yerel ekleyin
	- `LocalizedMenu` dizinini açın, `Preference` -> `Languages` -> `Add a language` yoluyla
	- `locale` klasörüne girin, `en` klasörünü `my` olarak kopyalayın
	- `my` klasörüne girin, `en.json` dosyasını `my.json` olarak yeniden adlandırın ve şu şekilde düzenleyin:

	  ```JavaScript
      {
        "link": "",
        "hidden": false,
        "caption": "BenimDilim",
        "mnemonic": "b"
      }
      ```

	- `menu/3999` klasörüne girin, `en` klasörünü `my` olarak kopyalayın ve menü dosyalarındaki tüm `caption`ları çevirin
	- `Preference` -> `Languages` -> `Detect` yoluyla dili algılayın, ardından `BenimDilim (my)` görünecek

  > **Yerel yapılandırmalar**<br>
  > link: hedef yerel<br>
  > hidden: menü öğesini gizle<br>
  > caption: dil adı, yerel kod otomatik olarak eklenecek<br>
  > mnemonic: kısayol tuşu, isteğe bağlı, kısayolun `caption` içinde olduğundan emin olun, büyük/küçük harfe duyarlı

### Bir Dil Gönderin
- Yerel ad `<languageCode>` veya `<languageCode>_<countryCode>` olarak adlandırılmalıdır
	- `<languageCode>` küçük harf, `<countryCode>` büyük harf, (yerelde çalışıyorsanız bunu göz ardı edin)
	- Dil: https://www.wikipedia.org/wiki/ISO_639-1
	- Ülke: https://www.wikipedia.org/wiki/ISO_3166-1
- Depoyu çatalayın
- Pull request yapın

### Yereller ve Katkıda Bulunanlar
- de_DE Almanca *by [Standarduser](https://github.com/Standarduser)*
- es İspanyolca *by [Christopher](https://t.me/Azriel_7589)*
- es_ES İspanyolca *by [Dastillero](https://github.com/dap39)*
- fr_FR Fransızca *by [fxbenard](https://github.com/fxbenard)*
- hu Macarca *by [Tamás Balog](https://github.com/picimako)*
- hy Ermenice *by [Arman High Foundation](https://github.com/ArmanHigh)*
- pt Brezilya Portekizcesi *by [JNylson](https://github.com/jnylson)*
- ru Rusça *by [Dimox](http://dimox.name) & [Ant0sh](https://github.com/Ant0sh) & [Maksim Arhipov](https://github.com/OSPanel)*
- sv_SE İsveççe *by [H2SO4JB](https://github.com/H2SO4JB)*
- tr Türkçe *by [hakantr](https://github.com/hakantr)*
- zh_CN Basitleştirilmiş Çince *by [Zam](https://github.com/zam1024t)*
- zh_TW Geleneksel Çince *by [Zam](https://github.com/zam1024t)*

### İlgili Tartışma
- https://github.com/wbond/package_control_channel/pull/5665
- https://github.com/rexdf/ChineseLocalization/issues/10

### Lisans
[MIT Lisansı](LICENSE)
