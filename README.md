# NEXORA: prototipo navegable

Prototipo de alta fidelidad de una plataforma de operación de seguridad para propiedad horizontal. Es un solo archivo, `index.html`, sin instalación ni dependencias. Se abre con doble clic o se publica con GitHub Pages.

Las tipografías Inter y Plus Jakarta Sans se cargan desde Google Fonts. Sin internet se usa la tipografía del sistema.

## Cómo probarlo

1. Abre el archivo e inicia sesión. Los PIN de demostración aparecen en pantalla y el código de segundo factor se muestra al pedirlo.
2. Cambia entre Dashboard, App móvil, Kiosco y Residente con las pestañas superiores.
3. Cada rol ve distintas vistas. El Consejo, por ejemplo, no ve la app, el kiosco ni el botón de pánico.

## Qué incluye

- **Dashboard:** resumen en vivo, personas dentro con permanencia, incidencias con responsable, evidencia, conversación y cierre, trazabilidad comparada (por tiempo, guarda, zona y tipo), unidades por torre y casa, personas restringidas, correspondencia, reportes, configuración de protocolos y bitácora con cadena de hashes.
- **App del guarda:** registro en pasos cortos, salida, protocolos por tipo de ingreso, códigos temporales, paquetes, rondas, novedades, pánico y cola sin conexión.
- **Kiosco:** consentimiento de datos, selección de apartamento o casa, autorización del residente en vivo y modo contingencia.
- **Residente:** autoriza o rechaza, genera códigos y recibe paquetes con constancia.
- **Portafolio:** varias copropiedades, cada una con sus propios datos, y asistente para crear una nueva.
- **Valor, Cobertura y Producción:** calculadora con cronómetro de piloto, contraste contra el documento de negocio y lista de preparación para producción.

## Importante

- **Los datos son sintéticos.** Se generan con una semilla fija y no representan clientes.
- **El inicio de sesión es una simulación.** Los PIN están en el código. No lo uses para proteger nada.
- **Se guarda en el navegador** (localStorage): bitácora, configuración y operaciones. El botón "Restablecer demostración" en Configuración lo borra.
- **Las descargas** usan un enlace del navegador. Dentro de Claude usan la capacidad de descargas.
- **La firma de informes y el sellado de la bitácora son simulados.** SHA-256 encadenado demuestra el concepto, no tiene valor probatorio por sí solo.

## Falta para producción

Servidor con autenticación verificada, aislamiento por copropiedad, cifrado, bitácora con sellado de tiempo de un tercero, política de datos personales revisada por un abogado, escalamiento de pánico por SMS y llamada, resolución de conflictos sin conexión y pruebas con guardas. El detalle está en la vista "Producción" del dashboard.

Marcos a confirmar con asesoría jurídica: Ley 1581 de 2012, Ley 675 de 2001 y Ley 527 de 1999. Esta lista no es un concepto legal.
