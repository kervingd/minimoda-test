# Práctica clase 01: casos del registro de MiniModa con IA

**Sitio:** https://minimoda-navy.vercel.app/registro

> Así tiene que quedar tu entrega. Reemplazá cada `___tu respuesta aquí___` con lo tuyo.

## 1. Preparación
- Navegador y fecha: ___Chrome 04.11.2026___

## 2. Superficie elegida
- Elegí (chat o cowork): ___chat___
- Por qué: ___Porque el interactuar con el agente mediante el chat de forma directa me permite tener mayor comprensión de la práctica___

## 3. Preguntas a Gemini
| # | Pregunta | Respuesta (resumen) | ¿Acierto o error/invento? |
|---|----------|---------------------|---------------------------|
| 1 | ¿Qué campos pide el formulario de registro de https://minimoda-navy.vercel.app/registro? | ___solicita nombre, correo, contraseña (mínimo 8 caracteres), confirmación de contraseña, edad (de 13 a 120 años), país y la aceptación de los términos y condiciones___ | ___Acierto___ |
| 2 | ¿Cuál es el largo mínimo de la contraseña y qué edad se permite? | ___Contraseña de mínimo 8 caracteres y edad permitida de 13 a 120 años.___ | ___Acierto___ |
| 3 | ¿Qué pasa si no acepto los términos? | ___El sistema muestra un mensaje de error indicando que es obligatorio aceptar los términos para registrarse.___ | ___tu Acierto___ |

- Un acierto: ___La IA identificó correctamente la validación solicitada en el registro___
- Un error o invento: ___Resultado no esperado o respuesta para salir del pasoe___

## 4. Primer modo
- Superficie y modo: ___Chat Gemini___
- Prompt de ejemplo:
  ```
  Sos QA. Vamos a probar el registro de https://minimoda-navy.vercel.app/registro
  Campos: nombre, email, contraseña, confirmar contraseña, edad, país y aceptar términos.
  1. Listá las reglas que se ven, los datos válidos e inválidos y los valores límite.
  2. Escribí 6 casos de prueba con: título, precondiciones, pasos con datos concretos,
     resultado esperado, prioridad (high/medium/low) y tipo (functional/negative/boundary).
  No inventes mensajes: si no sabés el texto exacto, marcalo "A VERIFICAR".
  ```
- Qué devolvió: ___: Generó una lista estructurada con las reglas de validación del formulario y 6 casos de prueba detallados (con título, pasos, resultados esperados, prioridad y tipo)___

## 5. Otra superficie: comparación en 3 líneas
1. ___Interfaz gráfica más amplia___
2. ___Interacción más fluida para el paso a paso___
3. ___No visualicé errores o inventos___

## 6. Mis 3 mejores casos (cargados en Qase, proyecto MiniModa)
Formato del título: `Registro: <qué se prueba>`
Captura de la suite en Qase con tus casos: `evidencias/qase-suite-casos.png`

### Caso 1: ___Registro de usuario con datos válidos___
- Precondiciones: ___El usuario se encuentra en la página de registro y no posee una cuenta previa.___
- Pasos: ___1. Ingresar un nombre válido. 2. Ingresar un correo electrónico válido. 3. Ingresar una contraseña de al menos 8 caracteres y confirmarla. 4. Seleccionar una edad permitida y un país. 5. Marcar la casilla de aceptar términos y condiciones. 6. Hacer clic en el botón de registrarse.___
- Resultado esperado: ___El sistema registra al usuario con éxito___
- Evidencia: `clase-01/qase-cp1 (2).png`

### Caso 2: ___Validar largo mínimo de contraseña___
- Precondiciones: ___El usuario se encuentra en el formulario de registro y cuenta con campos vacíos.í___
- Pasos: ___1. Completar los campos obligatorios con datos válidos. 2. Ingresar una contraseña de menos de 8 caracteres (ej: "Pass12"). 3. Intentar enviar el formulario.í___
- Resultado esperado: ___El sistema muestra un mensaje de error indicando que la contraseña no cumple con el largo mínimo y no permite completar el registro.___
- Evidencia: `clase-01/qase-cp2.1.png`

### Caso 3: ___tu respuesta aquí___
- Precondiciones: ___Validar límite de edad inferior no permitida___
- Pasos: ___El usuario se encuentra en el formulario de registro y cuenta con campos vacíos.___
- Resultado esperado: ___1. Completar los campos obligatorios con datos válidos. 2. Ingresar una edad menor a 13 años (ej: 12). 3. Intentar enviar el formulario.___
- Evidencia: `clase-01/qase-cp3.png`

## 7. Mapa del harness
| Pieza | En lo que usé |
|-------|---------------|
| Modelo | ___Gemini___ |
| App | ___Chat de Gemini___ |
| Harness | ___Interfaz chat navegador___ |
| MCP | ___tu respuesta aquí___ |
| Skill | ___tu respuesta aquí___ |

## 8. Entrega
- Link de tu repo (pegalo también en el Telegram): ___https://github.com/kervingd/minimoda-test/blob/main/clase-01/practica.md)___
