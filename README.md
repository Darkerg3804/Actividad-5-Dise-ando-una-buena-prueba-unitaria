# Actividad 5: Pruebas Unitarias con TDD

## Descripción

Este proyecto tiene como objetivo aplicar los principios de diseño de una buena prueba en el desarrollo guiado por pruebas (*Test-Driven Development*, TDD), mediante la implementación de una función que calcula el precio final de un producto después de aplicar un descuento porcentual.

Se busca demostrar el uso de pruebas unitarias y aserciones, así como las características de independencia, repetibilidad, atomicidad, claridad y automatización.

## Objetivos

- Aplicar el enfoque TDD durante el desarrollo de una función.
- Diseñar y ejecutar pruebas unitarias antes de implementar la solución.
- Comprobar los resultados mediante aserciones.
- Garantizar la independencia y repetibilidad de las pruebas.
- Mejorar la claridad y organización del código de prueba.

## Funcionalidad

La función `calcularDescuento()` recibe el precio de un producto y el porcentaje de descuento, y devuelve el precio final después de aplicar el descuento.

**Ejemplo:**

```python
calcularDescuento(1000, 10)  # Resultado: 900
```

## Casos de prueba

| Caso | Precio | Descuento | Resultado esperado |
|---|---:|---:|---:|
| Sin descuento | 1000 | 0 % | 1000 |
| Descuento del 10 % | 1000 | 10 % | 900 |
| Descuento del 20 % | 500 | 20 % | 400 |
| Precio cero | 0 | 10 % | 0 |
| Descuento máximo permitido | 1000 | 100 % | 0 |

## Tecnologías utilizadas

- Python 3
- pytest
- Git y GitHub

## Estructura del proyecto

```text
Actividad5-TDD/
├── calcular_descuento.py
├── test_calcular_descuento.py
├── README.md
└── evidencia/
    ├── pruebas-fallidas.png
    └── pruebas-exitosas.png
```

## Instalación y ejecución

**1. Instalar Python 3**, si todavía no está instalado.

**2. Instalar pytest:**

```bash
python -m pip install pytest
```

**3. Ejecutar las pruebas:**

```bash
python -m pytest -v
```

El comando ejecuta las pruebas unitarias y muestra el resultado de cada una.

## Metodología TDD

El desarrollo sigue las siguientes etapas:

1. **Red:** escribir las pruebas y comprobar que fallen antes de implementar la función.
2. **Green:** implementar la funcionalidad mínima necesaria para que las pruebas pasen.
3. **Refactor:** mejorar la claridad y organización del código sin alterar su comportamiento.

## Principios de diseño de pruebas aplicados

- **Independencia:** cada prueba puede ejecutarse sin depender de las demás.
- **Repetibilidad:** las pruebas producen resultados consistentes cuando se ejecutan nuevamente bajo las mismas condiciones.
- **Atomicidad:** cada prueba verifica un comportamiento específico.
- **Claridad:** los nombres de las pruebas describen el comportamiento evaluado.
- **Automatización:** pytest ejecuta las pruebas y verifica los resultados automáticamente mediante aserciones.

## Evidencias

La carpeta `evidencia/` contiene capturas de la ejecución de las pruebas antes y después de implementar la función, mostrando el proceso TDD y la ejecución exitosa de los casos de prueba.

## Autor

Estudiante: Juan Emmanuel Rodríguez García

Asignatura: Desarrollo Basado en Pruebas

Facilitador: Ing. Carlos Rafael Luna Vargas, MGI, MGC

Actividad: 5 — Diseño de pruebas en TDD
