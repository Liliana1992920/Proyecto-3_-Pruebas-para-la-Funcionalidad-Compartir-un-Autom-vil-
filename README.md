# Informe Final del Proyecto: Pruebas para la Funcionalidad "Compartir un Automóvil"

## **Descripción del Proyecto**
Este proyecto tuvo como objetivo analizar, documentar y probar la funcionalidad **"Compartir un automóvil"** de la aplicación **Urban Routes**. Se evaluaron aspectos de diseño, funcionalidad del formulario de reserva, ventanas emergentes asociadas y la función de alquiler de automóviles en los siguientes entornos:

- **Google Chrome**: resolución de **800x600**.
- **Firefox**: resolución de **1920x1080**.

---

## **Objetivos**
1. Validar la funcionalidad de "Compartir un automóvil" en los entornos especificados.
2. Diseñar listas de comprobación y casos de prueba para los elementos clave:
   - Formulario de reserva.
   - Ventanas emergentes ("Método de pago" y "Agregar tarjeta").
   - Botón "Reservar".
   - Función de alquiler de automóviles.
3. Identificar errores y proporcionar documentación detallada para el equipo de desarrollo.

---

## **Desarrollo del Proyecto**

### **1. Lista de Comprobación: Diseño del Formulario de Reserva**
- **Validaciones realizadas:**
  - Verificación de los campos requeridos (`Nombre`, `Destino`, `Fecha y Hora`).
  - Alineación de elementos y consistencia con los diseños de Figma.
  - Apariencia correcta del botón "Reservar" (fuente, color y visibilidad).

---

### **2. Lista de Comprobación: Ventanas "Método de Pago" y "Agregar Tarjeta"**
#### **Método de Pago**
- **Pruebas positivas:**
  - Selección de métodos de pago válidos (e.g., tarjeta de crédito, PayPal).
  - Validación del método seleccionado en el resumen del viaje.
- **Pruebas negativas:**
  - Intentar reservar sin seleccionar un método de pago.
  - Selección de un método de pago no soportado.

#### **Agregar Tarjeta**
- **Pruebas positivas:**
  - Ingreso de datos válidos (16 dígitos, fecha de vencimiento correcta).
  - Guardar tarjeta como predeterminada.
- **Pruebas negativas:**
  - Ingreso de números de tarjeta inválidos (menos de 16 dígitos o caracteres alfabéticos).
  - Omitir campos obligatorios como `CVV` o `Fecha de Vencimiento`.

---

### **3. Casos de Prueba: Botón "Reservar"**
#### **Pruebas Positivas**
- Reserva exitosa con todos los campos completados correctamente.
- Confirmación mediante ventana emergente "Automóvil reservado".

#### **Pruebas Negativas**
- Reservas fallidas por campos incompletos o inválidos.
- Aparición de las ventanas emergentes:
  - "¿Seguro que quieres cancelar el viaje?" al cancelar.
  - "Viaje cancelado" tras confirmar la cancelación.

---

### **4. Casos de Prueba: Función de Alquiler de Automóviles**
#### **Pruebas Positivas**
- Selección exitosa de un automóvil disponible con fechas válidas.
- Visualización correcta del resumen del alquiler.

#### **Pruebas Negativas**
- Intentar alquilar un automóvil con fechas fuera de rango.
- Selección de un automóvil marcado como no disponible.

---

### **5. Ejecución de Pruebas**
#### **Diseño**
- **Validaciones en ambos entornos**:
  - Google Chrome (800x600): Identificación de problemas de diseño en pantallas pequeñas.
  - Firefox (1920x1080): Confirmación de diseño correcto en pantallas grandes.

#### **Funcionalidad**
- **Validaciones en Google Chrome (800x600):**
  - Pruebas de lógica para los cálculos de precio y duración.
  - Validaciones de interacción del usuario en formularios y ventanas emergentes.

---

## **Resultados de las Pruebas**

### **Errores Identificados**
1. El botón "Reservar" se desborda de la pantalla en la resolución 800x600.
2. El campo `Destino` permite caracteres especiales sin validación.
3. La ventana emergente "Agregar tarjeta" no muestra mensajes de error al dejar campos vacíos.
4. Validaciones incorrectas para números de tarjeta que incluyen caracteres alfabéticos.
5. El texto de la ventana "¿Seguro que quieres cancelar el viaje?" aparece truncado en la resolución 800x600.
6. La lista de automóviles no se actualiza al seleccionar fechas fuera de rango.

---

## **Conclusiones**
- **Diseño**: Aunque funcional en su mayoría, existen problemas significativos en pantallas pequeñas (800x600).
- **Funcionalidad**: Se detectaron errores críticos en la validación de formularios y ventanas emergentes.
- **Recomendación**: Es necesario corregir los errores reportados antes de la siguiente iteración de desarrollo.

---
**Enlace a los reportes finales:** [[[Ver Informe Final](https://drive.google.com/drive/folders/1fgv-vZKrB4jXODXDu7mLwGpBpv-sOQTK?usp=sharing)](#)
---

## **Recomendaciones**
1. Corregir las desalineaciones y errores de diseño en resoluciones pequeñas.
2. Implementar validaciones más estrictas para campos clave como `Destino` y `Número de Tarjeta`.
3. Realizar pruebas adicionales tras la corrección de errores.
4. Considerar la automatización de pruebas para validar las funcionalidades críticas en futuras actualizaciones.

---

**Equipo QA de Urban Routes**  

