
# Proyecto de Expresiones Regulares



## 1. Introducción a las Expresiones Regulares

### ¿Qué son las Expresiones Regulares?
Las expresiones regulares son secuencias de caracteres que definen un patrón de búsqueda en texto. Son muy útiles para tareas de manipulación de texto, búsqueda y validación.

### Casos de uso:
- Validación de datos de entrada (como correos electrónicos y números de teléfono).
- Extracción de información de texto.
- Búsqueda y reemplazo en documentos o código fuente.

---

## 2. Conceptos Básicos

### Caracteres Especiales
| Carácter | Significado                   |
|----------|--------------------------------|
| `.`      | Coincide con cualquier carácter |
| `*`      | Coincide 0 o más veces          |
| `+`      | Coincide 1 o más veces          |
| `?`      | Coincide 0 o 1 vez              |
| `\d`    | Coincide con cualquier dígito   |
| `\w`    | Coincide con cualquier letra o número |
| `\s`    | Coincide con cualquier espacio en blanco |

### Ejemplos
- `\d+` : Coincide con uno o más dígitos consecutivos.
- `[a-zA-Z]`: Coincide con cualquier letra mayúscula o minúscula.
- `^\w+@\w+\.\w{2,3}$`: Valida correos electrónicos con estructura básica.

---

## 3. Construyendo Patrones

### Ejercicio 1: Validación de correos electrónicos
**Patrón:** `/^[\w\.-]+@[a-zA-Z\d-]+\.[a-zA-Z]{2,6}$/`
Explicación:
- `^[\w\.-]+`: Usuario que empieza con caracteres alfanuméricos, puntos o guiones.
- `@`: Símbolo obligatorio.
- `[a-zA-Z\d-]+`: Dominio que contiene letras, números y guiones.
- `\.[a-zA-Z]{2,6}$`: Extensión de dominio entre 2 y 6 caracteres.

### Ejercicio 2: Extracción de números de teléfono
**Patrón:** `/\(\d{3}\) \d{3}-\d{4}/`
- `\(\d{3}\)`: Código de área entre paréntesis.
- `\d{3}-\d{4}`: Número de 7 dígitos con un guion.

---

## 4. Práctica y Ejercicios

### Ejercicio 3: Buscar palabras específicas
**Patrón:** `/\b[Hh]ola\b/`
- `\b`: Marca el inicio y el final de la palabra.

### Ejercicio 4: Validación de URLs
**Patrón:** `/^https?:\/\/(www\.)?\w+\.\w{2,}(\/\w+)*$/`
- Valida URLs con o sin "www", y rutas opcionales.

---

## 5. Optimización y Buenas Prácticas

### Consejos de optimización
1. **Usa anclas:** Como `^` para el inicio y `$` para el final de línea.
2. **Evita el uso excesivo de `.*`:** Puede hacer que los patrones se vuelvan lentos.
3. **Prueba y depura:** Existen herramientas en línea como [regex101.com](https://regex101.com) para probar expresiones regulares.

---

## 6. Proyecto Final: Aplicación de Expresiones Regulares

### Descripción del Proyecto
Crear una aplicación que valide formularios de usuario donde:
- **Correo electrónico**: Se valide la estructura correcta.
- **Número de teléfono**: Se permita solo un formato específico.
- **Dirección URL**: Se asegure que sea válida y accesible.

**Ejemplo de código en JavaScript:**
```javascript
function validateEmail(email) {
    const regex = /^[\w\.-]+@[a-zA-Z\d-]+\.[a-zA-Z]{2,6}$/;
    return regex.test(email);
}

console.log(validateEmail("correo@dominio.com"));  // true o false
```

---

## 7. Conclusiones

Aprender expresiones regulares permite una manipulación avanzada de texto, con aplicaciones prácticas en programación, validación de formularios, y más. Practicar estos conceptos y experimentarlos en proyectos reales ayuda a desarrollar habilidades útiles para mejorar la eficiencia y precisión en tus proyectos.

---

## Recursos

- [Documentación de Expresiones Regulares en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Regular_Expressions)
- [Platzi - Curso de Expresiones Regulares](https://platzi.com/clases/expresiones-regulares/)
- [Herramienta Regex101](https://regex101.com/)

---

**Autor:** Barrantes
