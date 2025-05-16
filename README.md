# **README: Sistema de Detección de Fraudes con Machine Learning**  

---

## **📌 Descripción del Proyecto**  
Este proyecto implementa un sistema de **detección de transacciones fraudulentas** en tarjetas de crédito utilizando técnicas avanzadas de Machine Learning. El modelo analiza patrones en datos históricos para identificar fraudes en tiempo real, con un enfoque en **alto recall** (para capturar la mayoría de los fraudes) y **precisión equilibrada** (para minimizar falsas alarmas).  

**🔍 Objetivo Principal:**  
Este proyecto tiene como finalidad desarrollar un sistema de detección de fraudes en tarjetas de crédito mediante la aplicación de modelos de Machine Learning. Para ello, se parte del análisis de un conjunto de datos reales de transacciones financieras, con el objetivo de identificar patrones característicos de operaciones anómalas que puedan indicar posibles intentos de fraude.  

---

## **📊 Dataset**  
**Origen:** [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
**Características:**  
- **284,807 transacciones** (492 fraudes = 0.172%).  
- **Variables:** V1-V28 (PCA), Time (segundos), Amount (monto), Class (0: normal, 1: fraude).  
**Desafío:** Desbalance extremo de clases.  

---

## **🛠️ Tecnologías Utilizadas**  
| **Categoría**       | **Herramientas**                                                                 |  
|----------------------|---------------------------------------------------------------------------------|  
| **Lenguaje**         | Python 3.9+                                                                     |  
| **ML/DL**            | Scikit-learn, XGBoost,                                                                      |   
| **Preprocesamiento** | Pandas, NumPy, SMOTE (imblearn), RobustScaler                                   |  
| **Visualización**    | Matplotlib, Seaborn                                                     |   
 

---

## **⚙️ Flujo de Trabajo**  
1. **Preprocesamiento:**  
   - Escalado de Time y Amount con RobustScaler.  
   - Balanceo con **SMOTE** (Synthetic Minority Oversampling Technique).  
    

2. **Entrenamiento:**  
   - Comparación de modelos (Logistic Regression, Random Forest, XGBoost).   
   

3. **Evaluación:**  
   - Métricas clave: **Recall, Precision, AUPRC, F1-Score**.  
   - Matrices de confusión y curvas Precision-Recall.  

   

---

## **📊 Resultados**  
### **Rendimiento de Modelos (Test Set)**  
| Modelo               | Recall | Precision | F1-Score   |   
|----------------------|--------|-----------|----------|   
| **XGBoost**          | 0.92   | 0.60      | 0.11     |    
| **Random Forest**    | 0.80   | 0.88     | 0.83   |   
| **Logistic Regression**              | 0.86   | 0.72      | 0.78    |   




## **🔍 Hallazgos Clave**  
- **Variables críticas:** V4, V11 (↑ riesgo), V14, V2 (↓ riesgo).  
- **Mejor modelo:** Random Forest con **80% recall** (Equilibrado en metricas).   
- **Falsos positivos:** 8 transacciones legítimas marcadas como fraude.   

---

## **🚀 Conclusiones**   
Al implementar este tipo de proyectos, podemos:
- Proteger economías
- Innovar en servicios financieros
- Crear sistemas autónomos que evolucionen con las amenazas futuras.

Además del beneficio económico, este sistema contribuye a la protección de los consumidores y al fortalecimiento de la confianza en los sistemas financieros.  

