# Descripción metodológica

El análisis parte de cuatro series financieras diarias: USD/MXN, S&P 500, VIX y Treasury a 10 años. Para evitar relaciones espurias entre niveles no estacionarios, los precios se transforman a cambios diarios antes de la estimación. En el caso del tipo de cambio y del S&P 500 se utilizan rendimientos logarítmicos; para el VIX y el Treasury se emplean primeras diferencias.

Primero se revisan estadísticos descriptivos, correlaciones y la prueba Dickey-Fuller aumentada. Después se estima un ARIMA sobre el rendimiento del USD/MXN y se compara con un SARIMAX que incorpora factores financieros externos. La muestra se divide cronológicamente en 80% para estimación y 20% para validación. El desempeño se compara mediante MAE y RMSE frente a un benchmark de rendimiento esperado igual a cero.

Finalmente se estima una regresión OLS con errores estándar HAC para medir la sensibilidad contemporánea del USD/MXN al S&P 500, VIX y Treasury, incluyendo un rezago del propio rendimiento cambiario. La beta móvil de 60 sesiones se utiliza únicamente como medida descriptiva de sensibilidad temporal y no como beta CAPM de una acción.
