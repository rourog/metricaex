# Prueba RCP ACLS 2025

Esta rama es de evaluación. No fusionar ni desplegar en GitHub Pages antes de la evaluación del propietario.

## Cambios

- Inicio con un toque: tiempo total, ciclo de dos minutos y metrónomo.
- Patrón 30:2: treinta pulsos y dos señales durante una ventana de cuatro segundos. Los cuatro segundos son una propuesta de interfaz para evaluar, no una duración fija impuesta por las guías.
- Vía aérea avanzada confirmada: compresiones continuas y señal de ventilación cada seis segundos, sin reiniciar el ciclo.
- Clasificación de ritmo desde el inicio, controles apilados, energía ajustable y registro separado de la descarga administrada.
- Primera adrenalina según ritmo/choques; repetición pendiente a tres minutos de la última dosis y aviso de intervalo mayor de cinco minutos.
- Amiodarona pendiente tras tres descargas reales en FV/TVsp; segunda dosis de 150 mg a valorar por el líder si persiste. Lidocaína aparece como alternativa; esta prueba no incorpora su calculadora.
- RCE, cierre de sesión, Deshacer y eliminación/restauración de registros al terminar.
- Sesión recuperable en el mismo navegador. Guardado separado de la aplicación pública.
- Laboratorio para adelantar +30 segundos o +2 minutos, con exportación marcada como simulación.

## Perfil de desfibrilador

El perfil inicial de prueba es bifásico 200 J y máximo 360 J. No es una recomendación universal: ajustar inicial y máximo al fabricante/equipo antes de evaluar. Monofásico propone 360 J; equipo desconocido propone el máximo configurado. La siguiente descarga conserva la energía y permite aumentarla.

## Pruebas

Ejecutar `node --test tests/rcp.test.cjs` con Node.js. Treinta pruebas del código original de esta rama, con DOM, reloj y audio simulados. Cubren intervalos, eventos, secuencia de sonidos, recuperación y carreras de Wake Lock. No equivalen a validación clínica ni a pruebas físicas de altavoz, pantalla o navegador móvil.

## Evaluación sugerida

1. Iniciar y escuchar treinta pulsos, dos señales de ventilación y el regreso del metrónomo.
2. Abrir Laboratorio y adelantar dos minutos; verificar botones de ritmo apilados.
3. Seleccionar FV, ajustar energía y confirmar una descarga administrada; comprobar nuevo ciclo.
4. Registrar adrenalina y adelantar tres minutos para ver el recordatorio.
5. Confirmar vía aérea y escuchar las señales de ventilación sin pausa del metrónomo.
6. Deshacer una dosis o vía aérea accidental.
7. Finalizar y eliminar/restaurar una entrada antes de copiar.
8. Recargar y recuperar una sesión.

La prueba no registra Service Worker ni instala una actualización sobre la app pública. Las demás calculadoras se conservan; los errores fuera de RCP de la auditoría requieren otro cambio.

Referencia: https://cpr.heart.org/-/media/CPR-Files/CPR-Guidelines-Files/2025-Algorithms/Algorithm-ACLS-CA-250527.pdf?sc_lang=en
