# NEXORA: prototipo navegable

Prototipo de alta fidelidad de una plataforma de operación de seguridad para propiedad horizontal. Es un solo archivo, `index.html` (o `nexora.html`), sin instalación ni dependencias. Se abre con doble clic o se publica con GitHub Pages.

Las tipografías Inter y Plus Jakarta Sans se cargan desde Google Fonts. Sin internet se usa la tipografía del sistema.

## Cómo probarlo

1. Abre el archivo e inicia sesión. Los PIN de demostración aparecen en pantalla (hay cuentas de administración y una cuenta por guarda) y el código de segundo factor se muestra al pedirlo.
2. Cambia entre Dashboard, App móvil, Kiosco y Residente con las pestañas superiores.
3. Pulsa **Recorrido** en la barra superior (o el botón del inicio de sesión) para ver una guía de 3 minutos con 12 pasos.
4. Cada rol ve distintas vistas. El Consejo, por ejemplo, no ve la app, el kiosco ni el botón de pánico.

## Qué incluye

- **Dashboard:** resumen en vivo, personas dentro con permanencia, incidencias con responsable, evidencia, conversación y cierre, trazabilidad comparada (por tiempo, guarda, zona y tipo), unidades residenciales (apartamentos y casas) con residentes, autorizados, vehículos e instrucciones permanentes, personas restringidas, correspondencia, reportes, configuración de protocolos y bitácora con cadena de hashes.
- **App del guarda:** cada guarda entra con su propia cuenta, registro en pasos cortos, vehículos de residentes (por placa) separados de los de visitantes, entrega de turno, salida, protocolos por tipo de ingreso, códigos temporales, paquetes, rondas, novedades, pánico y cola sin conexión.
- **Kiosco:** consentimiento de datos, selección de apartamento o casa, autorización del residente en vivo y modo contingencia.
- **Residente:** se puede ver como residente de cualquier unidad. Autoriza o rechaza, programa visitas (empleados, familiares, mudanzas, eventos), genera códigos, recibe paquetes con constancia, elige su canal de aviso y deja instrucciones para la portería.
- **Comparativo de unidades:** para administradores. Ranking por unidad, promedio de su zona, período anterior y comparación lado a lado de hasta cuatro unidades.
- **Convivencia, rondas verificadas, notificaciones y piloto con guardas:** tiempos de respuesta de los residentes, rondas con etiqueta NFC simulada, registro de avisos enviados y una guía para probar la app con guardas.
- **Anulaciones y correcciones:** el guarda corrige o anula lo suyo de los últimos 10 minutos, con motivo. Un supervisor o la administración corrige el resto. Nada se borra: queda en la bitácora. Las salidas hechas por error se pueden deshacer.
- **Varias puertas:** cada copropiedad define sus puertas (mixta, vehicular o peatonal) y el puesto de cada guarda. La trazabilidad se ve también por puerta.
- **En el celular:** el dashboard usa un menú plegable y las tablas se desplazan. La app del guarda ocupa toda la pantalla.
- **Avisos masivos:** circulares, cortes de servicio y citaciones a todas las unidades o a una zona, con plantillas, seguimiento de lecturas, confirmación y recordatorios. El residente los ve en su app.
- **Calendario de turnos:** rotación de tres semanas, edición por celda, cobertura requerida por turno y alertas (turno sin cubrir, noche a mañana sin descanso, más de seis días seguidos). Cada guarda ve sus próximos turnos.
- **Informes en PDF:** se generan en el navegador y se pueden descargar o compartir por correo desde el teléfono. El envío automático programado necesita un servidor de correo.
- **Portafolio:** varias copropiedades, cada una con sus propios datos, y asistente para crear una nueva.
- **Valor, Cobertura y Producción:** calculadora con cronómetro de piloto, contraste contra el documento de negocio y lista de preparación para producción.

## Importante

- **Los datos son sintéticos.** Se generan con una semilla fija y no representan clientes.
- **El inicio de sesión es una simulación.** Los PIN están en el código. No lo uses para proteger nada.
- **Se guarda en el navegador** (localStorage): bitácora, configuración y operaciones. El botón "Restablecer demostración" en Configuración lo borra.
- **Accesibilidad:** la página tiene regiones, etiquetas, foco gestionado en ventanas, uso completo con teclado y descripciones de los gráficos. Una revisión automática con axe-core no encontró problemas en 14 pantallas, pero falta probarla con lectores de pantalla y con personas usuarias.
- **Las descargas** usan un enlace del navegador. Dentro de Claude usan la capacidad de descargas.
- **La firma de informes y el sellado de la bitácora son simulados.** SHA-256 encadenado demuestra el concepto, no tiene valor probatorio por sí solo.

## Falta para producción

Servidor con autenticación verificada, aislamiento por copropiedad, cifrado, bitácora con sellado de tiempo de un tercero, política de datos personales revisada por un abogado, escalamiento de pánico por SMS y llamada, resolución de conflictos sin conexión y pruebas con guardas. El detalle está en la vista "Producción" del dashboard.

Marcos a confirmar con asesoría jurídica: Ley 1581 de 2012, Ley 675 de 2001 y Ley 527 de 1999. Esta lista no es un concepto legal.

## Demostración de 3 minutos

1. Abre la página y pulsa **Ver el recorrido guiado**.
2. **Resumen:** quién está dentro, incidencias, cupos y correcciones del día.
3. **App del guarda:** cada registro queda a nombre de quien lo hizo y de su puerta.
4. **Visitante:** documento, destino y motivo. La solicitud llega al residente.
5. **Residente:** autoriza, programa visitas y deja instrucciones. Puedes verlo como cualquier unidad.
6. **Vehículos:** la placa de un residente se reconoce sin pedir autorización.
7. **Corregir:** anula o corrige con motivo y comprueba que el original sigue en la bitácora.
8. **Kiosco:** consentimiento de datos y espera de la respuesta del residente.
9. **Trazabilidad y comparativo de unidades:** por período, guarda, zona, puerta y tipo.
10. **Auditoría:** usa Simular alteración y luego Verificar integridad.
11. **Cobertura:** qué está cubierto, qué es hipótesis y qué falta.
