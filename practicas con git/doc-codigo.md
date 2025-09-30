# Guía de Documentación de Código: Python, JavaScript y PHP

## 1. Introducción
La documentación del código es fundamental para garantizar su mantenibilidad, comprensión y escalabilidad.  

En esta guía se resumen las principales prácticas de documentación en Python, JavaScript y PHP, junto con herramientas recomendadas y ejemplos de aplicación.

---

## 2. Documentación en Python

### 2.1 Comentarios
Los comentarios deben ser breves, claros y explicar por qué se hace algo y lo que hace el código.

- **En línea**:
  ```python
  x = x + 1  # Incrementa el valor de x en 1
  ```

- **De bloque**:
  ```python
  # Este bloque de código implementa el cálculo
  # del promedio de una lista de números.
  suma = sum(lista)
  promedio = suma / len(lista)
  ```

### 2.2 Docstrings
Los docstrings documentan módulos, clases, funciones y métodos.  

Ejemplo:
```python
def suma(a: int, b: int) -> int:
    """
    Suma dos números enteros.

    Args:
        a (int): Primer número.
        b (int): Segundo número.

    Returns:
        int: Resultado de la suma.

    Example:
        >>> suma(2, 3)
        5
    """
    return a + b
```

### 2.3 Herramientas
- **Sphinx**: estándar para generar documentación en HTML/PDF.  
- **pdoc**: genera documentación automática a partir de docstrings.  
- **MkDocs**: útil para documentar proyectos completos con estilo moderno.  

---

## 3. Documentación en JavaScript

### 3.1 Comentarios
- **En línea**:
  ```js
  let count = 0; // contador inicial
  ```

- **De bloque**:
  ```js
  /*
   * Este módulo gestiona la autenticación de usuarios
   * y valida sus credenciales.
   */
  ```

### 3.2 JSDoc
JSDoc es el estándar de facto para documentar JavaScript.  
Permite agregar anotaciones que luego se pueden procesar para generar documentación.

Ejemplo:
```js
/**
 * Calcula el área de un rectángulo.
 * @param {number} ancho - El ancho del rectángulo.
 * @param {number} alto - El alto del rectángulo.
 * @returns {number} El área calculada.
 *
 * @example
 * // devuelve 20
 * areaRectangulo(4, 5);
 */
function areaRectangulo(ancho, alto) {
  return ancho * alto;
}
```

### 3.3 Herramientas
- **JSDoc**: genera documentación web a partir de comentarios estructurados.  
- **TypeDoc**: recomendado si se utiliza TypeScript.  

---

## 4. Documentación en PHP

### 4.1 Comentarios
- **En línea**:
  ```php
  $total = 0; // Inicializa el total
  ```

- **De bloque**:
  ```php
  /*
   * Este script procesa las órdenes
   * y actualiza el inventario.
   */
  ```

### 4.2 PHPDoc
El estándar PHPDoc permite describir funciones, clases y métodos en detalle.

Ejemplo:
```php
/**
 * Calcula el precio con IVA.
 *
 * @param float $precio Precio base.
 * @param float $iva Porcentaje de IVA.
 * @return float Precio final con IVA.
 *
 * @example
 * precioConIVA(100, 21); // 121.0
 */
function precioConIVA(float $precio, float $iva): float {
    return $precio * (1 + $iva / 100);
}
```

### 4.3 Herramientas
- **phpDocumentor**: la herramienta más usada para generar documentación automática.  
- **Doctum**: alternativa moderna y ligera.  

---

## 5. Conclusión
La documentación es tan importante como el código mismo, un proyecto bien documentado se entiende, se mantiene y evoluciona con mayor facilidad.