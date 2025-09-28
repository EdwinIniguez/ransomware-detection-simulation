# 🛡️ AI & Cybersecurity Project: Ransomware Detection in Medical Environments (Simulation)

## 📌 Descripción
Este proyecto propone el desarrollo de un sistema basado en **Inteligencia Artificial** para identificar **equipos infectados con comportamientos similares a ransomware** en entornos hospitalarios simulados.  

> ⚠️ **Nota importante:** Todo el trabajo se realiza en **simulación controlada**.  
> No se utiliza ni distribuye código malicioso real.  
> Los comportamientos de ransomware son **emulados** de manera segura (picos de I/O, modificaciones masivas de archivos, conexiones repetitivas de red, etc.).

---

## 🎯 Objetivos
- Detectar indicadores de comportamiento de ransomware en estaciones de trabajo y servidores médicos simulados.
- Minimizar falsos positivos para no interrumpir procesos clínicos críticos.
- Probar diferentes enfoques de IA (supervisado y no supervisado).
- Demostrar la efectividad del sistema en un **laboratorio reproducible** con datos sintéticos.

---

## 🗂️ Estructura del Repositorio

```bash
├── docs/                   # Documentación del proyecto (informes, papers, etc.)
├── infra/                  # Infraestructura para simulación
│   ├── vagrant/            # Archivos de Vagrant (opcional para levantar VMs)
│   ├── docker/             # Configuración de contenedores (ELK, Zeek, etc.)
│   └── network_diagram.png # Diagrama de la red simulada
├── simulation/             # Scripts para emular tráfico y comportamientos
│   ├── benign/             # Scripts de tráfico normal
│   ├── ransomware_like/    # Scripts benignos que emulan ransomware
│   └── dataset_generator.py # Script para consolidar logs -> CSV
├── data/                   # Carpeta para datasets recolectados
│   ├── raw/                # Datos crudos (logs, capturas pcap, eventos Sysmon)
│   └── processed/          # Features extraídos listos para IA
├── notebooks/              # Notebooks Jupyter para exploración y entrenamiento
│   ├── 01_exploracion.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_modelos_baseline.ipynb
│   └── 04_explainability.ipynb
├── src/                    # Código fuente del sistema de detección
│   ├── preprocessing/      # Scripts de limpieza y extracción de features
│   ├── models/             # Entrenamiento y pruebas de IA
│   └── detection_app/      # Prototipo de app o dashboard
├── tests/                  # Pruebas unitarias y validaciones
├── requirements.txt        # Dependencias del proyecto
├── docker-compose.yml      # Levantar ELK + Zeek (si se usa contenedores)
└── README.md               # Este archivo
