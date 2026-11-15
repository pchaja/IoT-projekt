<div align="center">

# 🛡️ IoT-projekt

**Analiza wykorzystania sztucznej inteligencji w detekcji anomalii w systemach IoT**

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Anaconda](https://img.shields.io/badge/Anaconda-44A833?style=for-the-badge&logo=anaconda&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

*Politechnika Świętokrzyska · Wydział Elektrotechniki, Automatyki i Informatyki*
*Bezpieczeństwo systemów IoT · Informatyka, 2ID24A*

[O projekcie](#-o-projekcie) • [Anomalie](#%EF%B8%8F-rodzaje-anomalii) • [Metody](#-metody-detekcji) • [Autorzy](#-autorzy)

</div>

---

## 📖 O projekcie

Urządzenia IoT zbierają dane z czujników (temperatura, wilgotność, ruch, zużycie energii) i zwykle pracują bez nadzoru człowieka. Są małe, tanie i często słabo zabezpieczone, więc nietypowe odczyty trzeba wykrywać automatycznie.

**Cel:** sprawdzić, czy metody sztucznej inteligencji wykrywają anomalie lepiej niż zwykłe progi statystyczne i ile fałszywych alarmów za to płacą.

## ⚠️ Rodzaje anomalii

**Jak wyglądają w danych:**

| Typ | W skrócie | Przykład |
|-----|-----------|----------|
| 📍 Punktowa | Pojedynczy odczyt mocno odstaje | 90°C między odczytami 21°C |
| 🕐 Kontekstowa | Wartość normalna, ale nie pasuje do sytuacji | 25°C w nocy przy wyłączonym ogrzewaniu |
| 📦 Zbiorowa | Cały fragment szeregu jest nietypowy | Zawieszony czujnik pokazuje stale tę samą wartość |
| 📈 Dryf | Odczyty powoli przesuwają się w jedną stronę | Rozkalibrowany czujnik |

**Co je wywołuje:** 🔧 awaria czujnika · 📡 problemy z komunikacją · 🕵️ cyberatak · 🔥 rzeczywiste zdarzenie (np. pożar)

## 🤖 Metody detekcji

Cztery metody o rosnącej złożoności:

| # | Metoda | Rola w projekcie | Plusy | Minusy |
|---|--------|------------------|-------|--------|
| 1 | **Z-score** | Punkt odniesienia (baseline) | Prosta, szybka, bez uczenia | Słaba na dryf, dużo fałszywych alarmów przy danych cyklicznych |
| 2 | **Naiwny Bayes** | Pierwszy model uczony na danych | Szybki, mało danych, łatwy do interpretacji | Zakłada niezależność cech |
| 3 | **Random Forest** | Klasyczne uczenie maszynowe | Dokładny, odporny na szum | Trudniejszy do interpretacji, cięższy |
| 4 | **Sieć neuronowa** | Właściwe „AI" | Wychwytuje złożone wzorce | Dużo danych i strojenia, „czarna skrzynka" |

## 👥 Autorzy

- **Igor Brożyna**
- **Patryk Chaja** · [@pchaja](https://github.com/pchaja)
