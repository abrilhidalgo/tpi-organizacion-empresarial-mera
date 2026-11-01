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
