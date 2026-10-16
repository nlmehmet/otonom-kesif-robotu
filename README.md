# Otonom Keşif Robotu

ROS 2 Humble, Gazebo Classic, SLAM ve Nav2 ile bilinmeyen bir ortamda kendi başına gezinen ve harita çıkaran mobil robot simülasyonu.

## Hedef

Simülasyondaki robot bilinmeyen bir ortamı otonom olarak keşfeder, haritayı çıkarır ve bu haritada verilen hedeflere engellerden kaçarak gider.

## Mimari

- **Simülasyon:** Gazebo Classic 11, TurtleBot3 (burger)
- **Algı ve konumlama:** LiDAR, odometri, IMU, slam_toolbox
- **Navigasyon:** Nav2 (global/local costmap, planner, controller)
- **Otonom keşif:** Frontier exploration
- **Görselleştirme:** RViz2

Veri akışı: sensörler -> SLAM -> harita + konum -> Nav2 -> `cmd_vel` -> Gazebo -> yeni sensör verisi

## Yol haritası

- [x] Ortam kurulumu ve duman testi (Gazebo, /scan, RViz2)
- [x] Manuel SLAM ile harita çıkarma (maps/ klasöründe)
- [ ] Kayıtlı haritada Nav2 ile otonom gezinme
- [ ] Frontier exploration ile otonom keşif
- [ ] Dinamik engeller ve parametre ayarı
- [ ] Ölçümler ve demo videosu

## Ortam

Ubuntu 22.04, ROS 2 Humble, Gazebo Classic 11.10.2, The Construct (bulut ortamı)

## Durum notu
Nav2 kayıtlı haritada çalışıyor, kısa hedefler başarılı. Sıradaki: daha uzun hedefler ve frontier exploration.
