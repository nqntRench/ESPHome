# ESPHome – Compteurs d’eau et de gaz

[![ESPHome](https://img.shields.io/badge/ESPHome-Device-blue.svg)](https://esphome.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

Firmware ESPHome pour ESP32 permettant de mesurer les impulsions d’un compteur d’eau et de gaz, avec conversion automatique en m³ et intégration native dans Home Assistant.

---

## Matériel

- ESP32
- Sorties impulsionnelles des compteurs
- Résistances pull-up si nécessaire

---

## GPIO utilisés

| Capteur          | GPIO |
|------------------|------|
| Compteur d’eau   | 25   |
| Compteur de gaz  | 14   |

---

## Configuration

Éditer `secrets.yaml` :

- `wifi_ssid`
- `wifi_password`
- `compteurs-eau-et-gaz_api-key`
- `compteurs-eau-et-gaz_ota-password`

Flash via USB ou OTA depuis ESPHome Dashboard.

---

## Capteurs exposés

- Consommation d’eau (m³, `total_increasing`)
- Consommation de gaz (m³, `total_increasing`)
- Signal WiFi
- Boutons d’incrément manuel
