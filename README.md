# TPI Organización Empresarial: Módulo de integración Avaya–Telesoft

## Descripción del sistema

Mera Solutions atiende, para Prisma Medios de Pago, a tarjetahabientes de distintos bancos. Hoy, el DNI y el número de tarjeta que el cliente ingresa en el IVR de Avaya se muestran en pantalla, pero el operador tiene que copiarlos a mano en Telesoft.

Para no descuidar la validación de identidad, el módulo propuesto completa automáticamente esos datos en Telesoft, pero mantiene la validación obligatoria por parte del operador. El proyecto lo llevarán adelante de forma conjunta Sistemas / IT, un referente de operaciones de Mera y la software factory externa simulada Devvi Sol.

## Integrante
- Hidalgo Abril Antonella (UTN, Tecnicatura Universitaria en Programación)
- Revisión de pares: @AgustinGaitan

## Enlaces
- Tablero: [Backlog TPI Mera](https://github.com/users/abrilhidalgo/projects/1)
- Diagrama BPMN: [carpeta docs/bpmn](docs/bpmn)

## Definición de "Listo"
Una historia está lista cuando su proceso está modelado en el BPMN, sus criterios de aceptación están documentados y un par los revisó.
## Pull Requests revisados
   La constancia de la revisión de pares queda en los siguientes Pull Requests:
- [PR #4: Diagrama BPMN de la atención de llamada](https://github.com/abrilhidalgo/tpi-organizacion-empresarial-mera/pull/4), revisado por @AgustinGaitan
- [PR #5: Portada, definición de Listo e indicadores de control](https://github.com/abrilhidalgo/tpi-organizacion-empresarial-mera/pull/5), revisado por @AgustinGaitan

## Indicadores de control

| Indicador | Cómo se mide | Estándar | Fuente del dato | Si hay desvío |
|---|---|---|---|---|
| Tiempo de respuesta | Segundos desde que la llamada llega al operador hasta que DNI y tarjeta aparecen en Telesoft | Menos de 2 segundos | Registro de Telesoft (`fecha_hora`) | Revisar la integración con IT y Devvi Sol |
| Precisión del autocompletado | Llamadas con datos del IVR cargadas sin errores ÷ total de llamadas con datos del IVR × 100 | Al menos 95 % | Registro de Telesoft durante el piloto | Revisar los casos con error y corregir la integración |
| Confirmación del operador | Contactos autocompletados con confirmación registrada ÷ total de contactos autocompletados × 100 | 100 % | Entidad Validación (`dato_confirmado`) | Calidad da feedback al operador y lo comunica al Team Leader 


## Declaración de Uso de IA

Usé Claude (Anthropic) como asistente durante todo el trabajo. Le fui pasando el contexto paso a paso, incluyendo los TP anteriores (Entregas 1, 2 y 3) como guía, para que sus respuestas fueran coherentes con el caso de Mera Solutions S.A.

**Qué le pedí y qué hizo:**
- **Diagrama BPMN:** le describí el flujo de la llamada y las reglas del negocio (validación antes del motivo, control del pago mínimo, registro de todo contacto en Telesoft). Claude generó el archivo base en BPMN 2.0, que importé en bpmn.io.
- **Historias de usuario:** Claude me dio un ejemplo para la primera historia, y a partir de ese modelo escribí yo las otras dos.

**Qué corregí o decidí yo:**
- En el diagrama cambié palabras, reacomodé elementos y ajusté espacios para que se lea mejor.
- Adapté la redacción de las historias y los criterios de aceptación a cómo funciona realmente la campaña.
- Los estándares de los indicadores (menos de 2 segundos, al menos 95 % de precisión y 100 % de confirmación del operador) no los inventó la IA: salen de las metas de la Entrega 2 y del diccionario de datos de la Entrega 3.
- Redacté la descripción del sistema con mis palabras y revisé que los términos coincidan con las entregas anteriores (Sistemas / IT, Team Leader, Calidad, Devvi Sol).
- Verifiqué lo que propuso la IA contra el flujo real de trabajo y los TP anteriores, y me hago responsable del contenido final.
