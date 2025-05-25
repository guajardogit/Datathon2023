# SmartVault – Hey Banco

¡Bienvenido al repositorio oficial de **SmartVault**, la propuesta ganadora del *Datathon Hey Banco 2025* para la detección y gestión de **gastos recurrentes** con Inteligencia Artificial! 🚀

---

## Tabla de contenido

1. [Descripción general](#descripción-general)  
2. [Características clave](#características-clave)  
3. [Dataset](#dataset)  
4. [Modelado y métricas](#modelado-y-métricas)  
5. [Guía rápida](#guía-rápida)  
6. [Estructura del proyecto](#estructura-del-proyecto)  
7. [Licencia](#licencia)  
8. [Equipo](#equipo)

---

## Descripción general

**SmartVault** clasifica transacciones, identifica patrones periódicos y predice el **próximo cargo recurrente** (fecha y monto). El objetivo es habilitar alertas personalizadas y fomentar hábitos de ahorro desde la app de Hey Banco.

> “Dale orden a tu dinero sin complicaciones. Te ayudamos a entender tus gastos, anticipar el futuro y construir el hábito del ahorro con IA.” – *datamigos 2.0*

---

## Características clave

* 🔍 Clasificación multiclase de transacciones (gasto, ingreso, ahorro/inversión)  
* 📅 Predicción de gastos recurrentes con modelos LSTM  
* 💰 Estimación anticipada de fecha y monto del próximo cargo  
* 🛡️ Detección de anomalías en patrones de gasto

---

## Dataset

| Archivo             | Registros | Periodo         | Descripción                        |
|---------------------|-----------|------------------|------------------------------------|
| `Transacciones.csv` | 346 k     | Ene‑24 ↔ Ene‑25 | Movimientos bancarios anonimizados |
| `Clientes.csv`      | 1 k       | –               | Datos demográficos básicos         |

> Los datos fueron proporcionados por Hey Banco exclusivamente para el *Datathon 2025* y no deben compartirse públicamente.

---

## Modelado y métricas

| Tarea                    | Algoritmo         | Métrica   | Resultado     |
|--------------------------|-------------------|-----------|---------------|
| Predicción de monto      | LSTM univariado   | MAE       | **10.86 MXN** |
| Predicción de fecha      | Heurístico + LSTM | RMSE días | **53.49**     |
| Detección de recurrentes | Regla + CV        | Acc.      | **90.11 %**   |

Entrenamiento realizado en varios 3 cuadernos Jupyther. Detalles en:*
- `Euristico/Euristico.ipynb`
- `Modelo LSTM/LSTM_predecir_Categorías.ipynb`
- `Modelo LSTM/LSTM_predecir_monto_total.ipynb`

---

## Guía rápida

### Requisitos

En caso de tener el requirements.txt

```bash
pip install -r requirements.txt
```

En caso de no tenerlo puedes instalar las librerias libremente

```bash
pip install pandas numpy matplotlib scikit-learn tensorflow jupyter
```

## Modelado y métricas

| Tarea                    | Algoritmo         | Métrica   | Resultado     |
| ------------------------ | ----------------- | --------- | ------------- |
| Predicción de monto      | LSTM univariado   | MAE       | **10.86 MXN** |
| Predicción de fecha      | Heurístico + LSTM | RMSE días | **53.49**     |
| Detección de recurrentes | Regla + CV        | Acc.      | **90.11 %**   |

---

## Roadmap

*

Contribuye via *Pull Request* y comenta en *Issues*.

---

## Contribuciones

1. Haz *fork* del repo.
2. Crea una rama (`git checkout ‑b feature/nueva‑feature`).
3. *Commit* y *push* (`git push origin feature/nueva‑feature`).
4. Abre un *Pull Request* explicando tu aporte.

> Código bajo **cobertura ≥ 90 %** + pasar `pre‑commit` hooks.

---

## Licencia

MIT © 2025 Datamigos 2.0

---

## Equipo

| Nombre           | Rol            | Carrera  |
| ---------------- | -------------- | -------- |
| César Sánchez    | Data Scientist | IDM      |
| Braulio Martínez | Data Engineer  | IDM      |
| Emilio Ramírez   | ML Engineer    | IDM      |
| Santiago Juárez  | Product & UX   | IDM      |

IDM: Ingeniería en Ciencia de Datos y Matematicas

Diseño y mantenimiento por **datamigos 2.0** – *¡Gracias por pasarte!*
