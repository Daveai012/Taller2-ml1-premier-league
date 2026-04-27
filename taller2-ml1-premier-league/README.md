# 🏆 The Oracle: Premier League AI Analytics
### Taller 2 — Machine Learning I (2026-I)
**Universidad Externado de Colombia**

Este proyecto presenta un ecosistema completo de análisis predictivo para la Premier League, combinando modelos estadísticos avanzados con un dashboard interactivo de alto rendimiento.

---

## 👥 Integrantes
- **David Castro**
- **Miguel Melo**
- **Santiago Rincon**

---

## 🚀 Dashboard Desplegado
El dashboard interactivo está disponible en:
👉 **[https://the-oracle-pl.netlify.app/](https://the-oracle-pl.netlify.app/)** 
*(O el URL proporcionado en la entrega)*

---

## 🧠 Arquitectura del Proyecto

### 1. Modelo xG (Goles Esperados)
Utilizamos una **Regresión Logística** entrenada con más de 7,000 tiros. 
- **Features clave:** Distancia al arco, ángulo, Big Chance, situación de contraataque, parte del cuerpo y zona del campo.
- **Métrica:** AUC-ROC de ~0.785, superando significativamente el baseline ingenuo.

### 2. Match Predictor (H/D/A)
Un sistema híbrido que combina:
- **Regresión Lineal:** Para proyectar la cantidad total de goles esperados por equipo.
- **Regresión Logística Multiclase:** Para predecir el resultado final (Victoria Local, Empate, Victoria Visitante).
- **Benchmark:** Diseñado para competir con el acierto del 49.8% de Bet365.

---

## 📂 Estructura del Repositorio
- `notebooks/`: Contiene los archivos `.ipynb` con el EDA y entrenamiento.
  - `modelo1_xg.ipynb`: Desarrollo del modelo de Goles Esperados.
  - `modelo2_match_predictor.ipynb`: Lógica del predictor de partidos.
  - `generar_datos_dashboard.ipynb`: Pipeline de exportación de datos.
- `dashboard/`: Código fuente de la interfaz web (HTML/CSS/JS).
- `data/`: Almacenamiento de datasets locales (CSV/JSON).
- `models/`: Modelos entrenados y escaladores serializados (`.pkl`).

---

## 🛠️ Cómo ejecutar el proyecto localmente

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tu-usuario/taller2-ml1-premier-league.git
   cd taller2-ml1-premier-league
   ```

2. **Configurar el entorno:**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

3. **Ejecutar Notebooks:**
   Puedes abrir los archivos en `notebooks/` usando Jupyter o VS Code para re-entrenar los modelos.

4. **Ver el Dashboard:**
   Simplemente abre `dashboard/index.html` en cualquier navegador moderno. Soporta carga offline de datos vía `data/data.js`.

---

## 📝 Reflexión
*"El fútbol es como una Regresión Logística: tienes todas las variables controladas hasta que un defensa central decide intentar una chilena desde el mediocampo."* ⚽✨
