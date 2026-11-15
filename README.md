> **Not:** Bu proje, 2025 yılı güz döneminde Gazi Üniversitesi BMT-209 Nesne Yönelimli Programlama dersi kapsamında geliştirilmiştir.

# Cinema Management System

![Status](https://img.shields.io/badge/Status-Completed-success.svg) ![Language](https://img.shields.io/badge/Language-Java-blue.svg) ![GUI](https://img.shields.io/badge/GUI-Swing-orange.svg) ![Database](https://img.shields.io/badge/Database-H2-lightgrey.svg)

Bu proje, sinema işletmelerinde film, salon, seans ve bilet işlemlerinin tek bir platform üzerinden yönetilmesini sağlayan masaüstü bir yazılım çözümüdür. Nesne Yönelimli Programlama (OOP) prensipleri merkeze alınarak modüler ve sürdürülebilir bir mimaride tasarlanmıştır.

## Temel Özellikler

- **Kullanıcı ve Rol Yönetimi:** Sistem; Yönetici (Manager), Gişe Personeli (Cashier) ve Müşteri (Customer) olmak üzere 3 farklı yetki seviyesi sunar.
- **Dinamik Fiyatlandırma (Polymorphism):** Seçilen filmin türüne (Standard 2D, Premium 3D, Animasyon) ve müşterinin yaş durumuna göre bilet fiyatları polimorfik olarak hesaplanır.
- **İnteraktif Biletleme:** Kullanıcılar seans seçimi yapıp salon planı üzerinden koltuk seçebilir, ödeme işlemlerini gerçekleştirebilir ve biletleri fiziksel fiş (.txt) olarak yazdırabilir.
- **Veri Kalıcılığı:** Tüm film, salon, seans ve bilet verileri dosya tabanlı H2 ilişkisel veritabanında JDBC katmanı aracılığıyla güvenli bir şekilde saklanmaktadır.

## Kullanılan Teknolojiler

- **Programlama Dili:** Java
- **Kullanıcı Arayüzü:** Java Swing
- **Veritabanı:** H2 Database & JDBC
- **Mimari:** OOP (Abstraction, Polymorphism, Inheritance, Encapsulation)

## Proje Yapısı

```text
src/
├── model/       # Kullanıcı (Manager, Customer) ve Medya (Film, Trailer) veri modelleri
├── service/     # Biletleme, fiyat hesaplama ve oturum iş mantığı
├── repository/  # Veritabanı soyutlama katmanı (Interface'ler)
├── h2/          # H2 veritabanı CRUD işlemleri 
├── ui/          # Swing tabanlı grafik arayüz panelleri (Login, SeatSelection...)
├── util/        # Fiziksel bilet yazdırma gibi I/O yardımcı araçları
└── exception/   # Kural dışı durumlar için özel hata yönetimi sınıfları
