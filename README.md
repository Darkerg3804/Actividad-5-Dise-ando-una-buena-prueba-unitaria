# Actividad 5: Diseño de pruebas unitarias con TDD

## 1. Descripción del proyecto

Este proyecto consiste en desarrollar una función denominada `calcularDescuento()` mediante la metodología **Test-Driven Development (TDD)**.

La función recibe el precio de un producto y un porcentaje de descuento, y devuelve el precio final después de aplicar el descuento.

El propósito de la actividad es aplicar los principios de diseño de buenas pruebas unitarias: independencia, repetibilidad, atomicidad, claridad y automatización.

## 2. Tecnologías utilizadas

- Python 3.12.10
- pytest 9.1.1
- Visual Studio Code
- Git y GitHub

## 3. Estructura del proyecto

```text
Actividad5-TDD/
├── calcular_descuento.py
├── test_calcular_descuento.py
├── README.md
└── evidencia/
    ├── RED.png
    └── GREEN.png
```

## 4. Funcionalidad implementada

La función `calcularDescuento(precio, porcentaje)` calcula el descuento correspondiente y lo resta del precio original.

**Ejemplo:**

```python
calcularDescuento(1000, 10)  # Resultado: 900.0
```

La fórmula utilizada es:

\[
P_f=P-\frac{P\cdot d}{100}
\]

Donde:

- \(P_f\): precio final.
- \(P\): precio original.
- \(d\): porcentaje de descuento.

## 5. Casos de prueba

Se implementaron cinco pruebas unitarias para verificar diferentes situaciones:

| Caso de prueba | Entrada | Resultado esperado |
|---|---|---:|
| Sin descuento | `1000, 0` | 1000 |
| Descuento del 10 % | `1000, 10` | 900 |
| Descuento del 20 % | `500, 20` | 400 |
| Precio cero | `0, 10` | 0 |
| Descuento del 100 % | `1000, 100` | 0 |

Las pruebas utilizan aserciones `assert` para comparar el resultado obtenido con el resultado esperado.

## 6. Aplicación de TDD

El desarrollo se realizó siguiendo las etapas del ciclo TDD:

### Red — Pruebas fallidas

Se ejecutaron las pruebas antes de completar la implementación de la función. Las cinco pruebas fallaron, evidenciando que la funcionalidad todavía no estaba disponible correctamente.

La captura correspondiente se encuentra en `evidencia/RED.png`.

### Green — Pruebas exitosas

Se implementó la función para calcular el descuento y devolver el precio final. Posteriormente, se ejecutaron nuevamente las pruebas y los cinco casos resultaron exitosos.

La captura correspondiente se encuentra en `evidencia/GREEN.png`.

### Refactor — Mejora del código

La etapa de refactorización consiste en mejorar la estructura y legibilidad del código sin modificar su comportamiento. Las pruebas unitarias permiten verificar que los cambios mantengan los resultados esperados.

## 7. Principios de diseño de pruebas aplicados

- **Independencia:** cada prueba utiliza sus propios datos y puede ejecutarse sin depender de otra prueba.
- **Repetibilidad:** los mismos datos producen resultados consistentes en ejecuciones sucesivas.
- **Atomicidad:** cada prueba verifica un caso de comportamiento específico.
- **Claridad:** los nombres descriptivos facilitan identificar qué comportamiento verifica cada prueba.
- **Automatización:** pytest ejecuta los casos y evalúa las aserciones automáticamente.

## 8. Instalación y ejecución

Se requiere Python 3 y pytest.

Instalar pytest:

```bash
pip install pytest
```

Ejecutar las pruebas desde la raíz del proyecto:

```bash
pytest -v
```

## 9. Resultados

La ejecución final de las pruebas produjo el siguiente resultado:

```text
collected 5 items

test_calcular_descuento.py::test_sin_descuento PASSED
test_calcular_descuento.py::test_descuento_del_diez_por_ciento PASSED
test_calcular_descuento.py::test_descuento_del_veinte_por_ciento PASSED
test_calcular_descuento.py::test_precio_cero PASSED
test_calcular_descuento.py::test_descuento_maximo_del_cien_por_ciento PASSED

5 passed in 0.04s
```

Las capturas de ejecución se encuentran en la carpeta `evidencia/`.

## 10. Autor

Estudiante: Juan Emmanuel Rodríguez García
Matrícula: 2025-0316

Asignatura: Desarrollo Basado en Pruebas

Facilitador: Ing. Carlos Rafael Luna Vargas, MGI, MGC

Actividad: 5 — Diseño de pruebas en TDD
