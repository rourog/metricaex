# Prueba RCP ACLS 2025

Esta rama es de evaluación. No fusionar ni desplegar en GitHub Pages antes de la evaluación del propietario.

## Cambios

- Inicio con un toque: tiempo total, ciclo de dos minutos y metrónomo.
- Patrón 30:2: treinta pulsos y dos señales durante una ventana de cuatro segundos. Los cuatro segundos son una propuesta de interfaz para evaluar, no una duración fija impuesta por las guías.
- Vía aérea avanzada confirmada: compresiones continuas y señal de ventilación cada seis segundos, sin reiniciar el ciclo.
- Evaluación automática de ritmo por ciclos, controles apilados, energía ajustable y registro de descarga administrada.
- Primera adrenalina según ritmo/choques; repetición pendiente a tres minutos de la última dosis y aviso de intervalo mayor de cinco minutos.
- Amiodarona pendiente tras tres descargas reales en FV/TVsp; segunda dosis de 150 mg a valorar por el líder si persiste. Lidocaína aparece como alternativa; esta prueba no incorpora su calculadora.
- RCE, cierre de sesión, Deshacer y eliminación/restauración de registros al terminar.
- Sesión recuperable en el mismo navegador. Guardado separado de la aplicación pública.
- Laboratorio para adelantar +30 segundos o +2 minutos, con exportación marcada como simulación.

## Interfaz compacta (segunda revisión)

- Inicio se transforma en contador con corazón rojo suave para compresiones y pulmones azules para ventilaciones. Con vía aérea: ritmo continuo y cuenta para la siguiente ventilación.
- Frecuencia inicial de 120/min.
- Decisiones de ritmo apiladas al completar cada ciclo; se retiró la evaluación manual.
- Fila amarilla `− / Descarga xxx J / +`, con registro de descarga administrada en un toque. La energía inicial es 200 J, ajustable entre 50 y 360 J; no constituye un perfil universal ni verifica capacidades del desfibrilador.
- Se retiraron panel de equipo, bloque separado de guía y textos explicativos. Bitácora plegada y confirmaciones breves.
- RCE verde; medicamentos neutros, amarillo cuando están pendientes y rojo si se supera el intervalo de cinco minutos desde adrenalina.

Antes de uso clínico final, resolver el acceso a la identificación/desfibrilación del ritmo inicial: esta revisión sigue la evaluación por ciclos solicitada y no debe interpretarse como esperar dos minutos para tratar FV/TVsp ya identificada.

## Pruebas

Ejecutar `node --test tests/rcp.test.cjs` con Node.js. Treinta y tres pruebas del código original de esta rama, con DOM, reloj y audio simulados. Cubren intervalos, eventos, secuencia de sonidos, recuperación y carreras de Wake Lock. No equivalen a validación clínica ni a pruebas físicas de altavoz, pantalla o navegador móvil.

## Evaluación sugerida

1. Iniciar y escuchar treinta pulsos, dos señales de ventilación y el regreso del metrónomo.
2. Abrir Laboratorio y adelantar dos minutos; verificar botones de ritmo apilados.
3. Ajustar energía y pulsar Descarga cuando se haya administrado; comprobar nuevo ciclo.
4. Registrar adrenalina y adelantar tres minutos para ver el recordatorio.
5. Confirmar vía aérea y escuchar las señales de ventilación sin pausa del metrónomo.
6. Deshacer una dosis o vía aérea accidental.
7. Finalizar y eliminar/restaurar una entrada antes de copiar.
8. Recargar y recuperar una sesión.

La prueba no registra Service Worker ni instala una actualización sobre la app pública. Las demás calculadoras se conservan; los errores fuera de RCP de la auditoría requieren otro cambio.

Referencia: https://cpr.heart.org/-/media/CPR-Files/CPR-Guidelines-Files/2025-Algorithms/Algorithm-ACLS-CA-250527.pdf?sc_lang=en
