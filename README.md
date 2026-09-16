🏭 Dynamic Capacity & Production Scheduler (Operations Research)

1. El Desafío del Negocio (Business Context)

En la manufactura automotriz Tier-1, operar un sistema de pintura continuo con una mezcla de alta volatilidad (804 SKUs para clientes como Tesla, Ford, Toyota, Nissan y Honda) genera una inestabilidad extrema en el balanceo de personal.

El modelo de asignación empírico reaccionaba a los picos de demanda de manera reactiva, requiriendo entre 8 y 10 operadores por turno y generando una alta fluctuación. Tras un análisis de tiempos y movimientos (MAFACT), se desmitificaron las restricciones del sistema:

Falsa restricción (Color Change): El cambio de color no requiere detener la línea; el robot solo necesita 2 pallets vacíos (1.57% de pérdida de capacidad) para purga.

Restricción Real (Rack Overspray): El verdadero cuello de botella es el engrosamiento de pintura en los pallets, lo que dificulta la carga/descarga e incrementa los tiempos estándar de forma variable.

2. Solución: Analítica Prescriptiva & Operations Research

Se desarrolló un modelo matemático de Scheduling Óptimo en Python que abandona la asignación empírica y utiliza optimización heurística.

El algoritmo secuencia los lotes agrupando densidades similares (piezas por rack) para estabilizar la carga de trabajo ergonómica.

Ordena los lotes para minimizar los saltos de color y la purga del robot.

3. Impacto Financiero y Operativo (ROI)

Estabilización de Plantilla: La fluctuación reactiva de personal (de 8 a 10 operadores) se eliminó por completo, logrando una línea balanceada y predecible.

Eficiencia Laboral (Ahorro del 22.7%): El modelo matemático demostró que la producción se puede sacar con una plantilla fija de 7 operadores. Esto incluye 6 operadores base + 1 Operador Comodín (Buffer OEE / Relief) para absorber de forma realista los micro-paros, rotación de descansos y variabilidad de la línea.

Gestión del Cambio: La optimización no implica despidos, sino la reubicación estratégica del exceso de personal hacia otros cuellos de botella en ensamble y la reducción sistemática de horas extras.

4. Arquitectura y Ciberseguridad

Data Privacy: Se utilizan entornos virtuales aislados y generadores de datos dummy para proteger el secreto industrial (NDA) y la topología de la cadena de suministro de los OEMs.

Stack: Python, Pandas (Data Manipulation), Matplotlib/Seaborn (Data Visualization), Programación Orientada a Objetos (OOP).