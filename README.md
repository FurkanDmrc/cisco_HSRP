
# 🔹 HSRP (Hot Standby Router Protocol) Lab

Bu projede Cisco Packet Tracer kullanılarak HSRP (Hot Standby Router Protocol) ile ağda yedeklilik (redundancy) ve yük dağılımı (load balancing) sağlanmıştır.

---

## 📌 Proje Senaryosu

İki farklı subnet üzerinde çalışan bir ağ ortamında, gateway yedekliliği sağlamak amacıyla HSRP yapılandırılmıştır.

- Subnet 1 → 192.168.1.0/24
- Subnet 2 → 192.168.3.0/24

Her subnet için ayrı HSRP grupları tanımlanarak:
✅ Kesintisiz ağ erişimi  
✅ Yük paylaşımı (load balancing)  
sağlanmıştır.

---

## 🧱 Topoloji

- 2 Router (HSRP yapılandırılmış)
- 2 Switch
- 2 LAN (farklı subnetler)
- 2 PC

---

## ⚙️ Kullanılan Teknolojiler

- Cisco Packet Tracer  
- HSRP (Hot Standby Router Protocol)  
- Redundancy  
- Load Balancing  
- Layer 3 Routing  

---

## 🌐 IP Adresleme

### 🔹 Subnet 1 (Sol LAN)

| Cihaz | IP |
|------|----|
| R1 | 192.168.1.1 |
| R2 | 192.168.1.2 |
| Virtual IP | 192.168.1.254 |
| PC | 192.168.1.10 |

---

### 🔹 Subnet 2 (Sağ LAN)

| Cihaz | IP |
|------|----|
| R1 | 192.168.3.1 |
| R2 | 192.168.3.2 |
| Virtual IP | 192.168.3.254 |
| PC | 192.168.3.10 |

---

## ⚙️ Konfigürasyon Özeti

### 🔹 HSRP Group 1 (192.168.1.0)

- R1 → Active
- R2 → Standby

### 🔹 HSRP Group 2 (192.168.3.0)

- R1 → Standby
- R2 → Active

👉 Bu yapı ile trafik iki router arasında paylaştırılmıştır.

---

## 🧪 Test Senaryosu

✅ Normal durumda tüm cihazlar haberleşebilmektedir  
✅ Aktif router kapatıldığında:  
- Trafik kesintisiz devam eder  
- Standby router devreye girer  

---

## 📸 Ekran Görüntüleri

Aşağıdaki testler gerçekleştirilmiştir:

- Topoloji görünümü  
- `show standby brief` çıktısı  
- Ping testleri  
- Failover testi (router shutdown sonrası)

---

## 💡 Kazanımlar

Bu proje ile:

- HSRP çalışma mantığını öğrendim  
- Gateway redundancy kavramını uyguladım  
- Load balancing yapısını deneyimledim  
- Failover senaryosunu test ettim  

---

## 🚀 Geliştirme Planı

- VLAN + HSRP entegrasyonu  
- ACL ile trafik kontrolü  
- DHCP yapılandırması  
- STP ile Layer 2 yedeklilik  

---

## 📂 Dosyalar

- `hsrp-lab.pkt` → Packet Tracer proje dosyası  
- `screenshots/` → Topoloji ve test görüntüleri  
---

## 🔗 Not

Bu proje öğrenme ve portföy geliştirme amacıyla hazırlanmıştır.
