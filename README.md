# AKLİSANS PRO imzalı lisans kataloğu

Güncel DERSPLAN PRO sürümleri `licenses-v2.json` dosyasını anonim HTTPS üzerinden okur. Katalog yalnızca lisans kodu eşleştirme özeti, ürün, tarihler, durum, terminal sınırı ve imzalı anahtar geçişi içerir. Müşteri iletişim bilgileri, tam aktivasyon kodları ve özel anahtarlar yayımlanmaz.

Mevcut kök açık anahtar istemci uygulamasında sabittir. Yeni imza anahtarı ancak bu kökten doğrulanan geçiş zinciriyle kabul edilir. Katalog ve açık anahtar aynı Git commit'iyle yayımlanır.

Eski `licenses.json` dosyası önceki istemcilerin uyumluluğu için korunur. Yeni yenileme ve iptal akışını almak için DERSPLAN PRO 4.4.0 veya üzeri kullanılmalıdır. Müşterinin mevcut tek lisans kodu değişmez.

Lisans süresi yıllıktır; son başarılı çevrimiçi doğrulamadan itibaren en fazla 30 gün çevrimdışı kullanım ve lisans bitiminden sonra en fazla 3 gün ek süre uygulanır. Bu süreler birbirine eklenerek 33 günlük çevrimdışı yetki oluşturmaz. Çevrimdışı cihaz iptali ancak bağlantı kurduğunda veya mevcut çevrimdışı süresi dolduğunda öğrenebilir.