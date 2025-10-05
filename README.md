# 1. Sobre el problema

Hoy en día los fraudes financieros en transacciones son una amenaza constante y que va en crecimiento para todo tipo de usuarios. Miles de transacciones ocurren a cada minuto y es difícil detectar de forma manual cuando hay patrones que ponen en riesgo la seguridad de estas.

Dentro de los usuarios afectados encontramos, usuarios que hacen uso de bancos o plataformas digitales, cuyos datos se pueden ver vulnerados en más de una ocasión, analistas financieros o equipos de seguridad que necesitan este tipo de herramientas para detectar irregularidades y hasta empresas financieras que buscan evitar las malas reputaciones por fraude.

Ante esto existe la necesidad de una herramienta web accesible para todo público que permita analizar datos financieros reales o simulados para detectar fraudes de manera automatizada mediante análisis estadístico.

### Objetivos principales: 
Implementar un sistema web con interfaz interactiva para cargar datasets de transacciones
Procesar datos y clasificarlos según su nivel de riesgo
Mostrar métricas, gráficos y reportes de detección de fraude.
Aplicar POO, funcional y lógica en diferentes componentes

# 2. Selección de paradigma de programación

### Programación Orientada a Objetos(POO)

Se utilizará para modelar las entidades principales del sistema, como por ejemplo:
Transacciones: monto, hora, país, usuario
Analizador de fraude: métodos para evaluar transacciones
Usuario: datos del cliente que consulta el sistema



### Programación funcional

Utilizada para el procesamiento de datos mediante funciones puras que agrupan transacciones  (map, filter, reduce) con el fin de procesar y analizar los datos de transacciones de forma limpia y segura.

Esto también permite procesar grandes volúmenes de datos de manera eficiente


### Programación Lógica

Permite definir reglas que clasificaron los hecho, en este caso de transacciones, como normales o fraudulentas, estas reglas se basarán en la siguiente información:

- Tipo de transacción (type)
- Monto (amount)
- Saldo inicial y final (oldbalanceOrg, newbalanceDest)
- Transacciones marcadas previamente (FlaggedFraud)

### Ejemplo de reglas lógicas del sistema

<img width="632" height="363" alt="image" src="https://github.com/user-attachments/assets/1fc358a9-0ef1-4110-9d66-6bc18da309f0" />









# 3. Dataset Seleccionado

### Fraudulent Transactions Data
https://www.kaggle.com/datasets/chitwanmanchanda/fraudulent-transactions-data

Este dataset es un modelo diseñado para la predicción de transacciones fraudulentas, Está en un formato CSV y tiene 6362620 filas and 10 columnas

### Licencia 
CC0: Dominio Público

## Diccionario de datos:

step: representa una unidad de tiempo en el mundo real, 1 step = 1 hora. Total steps = 744, equivalente a 30 días de simulación. TIPO: INT

type: indica tipo de transacción, CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER. TIPO: STRING

amount: monto de transacción expresado en moneda local. TIPO: FLOAT

nameOrig: Cliente que realiza la transacción. TIPO : STRING

oldbalanceOrd: Saldo inicial del cliente que inicio la transacción, antes de realizarla. TIPO: FLOAT

newbalanceOrig: Saldo después del pago. Se resta el monto de la transacción. TIPO: FLOAT

nameDest: Cuenta receptora(Comercio). TIPO: STRING

oldbalanceDest: Saldo inicial de la cuenta receptora. TIPO: FLOAT

newbalanceDest: Saldo final de la cuenta receptora. TIPO: FLOAT

isFraud: marca de si una transacción es fraudulenta, Valor: 1 = fraude, 0 = normal. TIPO: INT

isFlaggedFraud: Indica si la transacción fue marcada como ilegal por el sistema, Valor: 1 = marcada como ilegal, 0 = no marcada. TIPO: INT




# Diagrama de arquitectura

<img width="617" height="348" alt="image" src="https://github.com/user-attachments/assets/c92f9e00-ab13-46c1-9d24-6489de89c22c" />





# Prototipo

<img width="630" height="427" alt="image" src="https://github.com/user-attachments/assets/a73d87fb-c248-4a98-bd0d-28431ab6f12e" />


Prototipo que muestra como se vería la carga de datos dentro de la página web
