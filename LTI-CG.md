## Descripción del Sistema – LTI -BOOK-CG
## LTI -BOOK-CG (Last Tourism Integration - Booking Core Gateway)

🧠 Resumen Ejecutivo
LTI -BOOK-CG es una plataforma digital para la reserva de alojamientos turísticos orientada al mercado nacional e internacional. Su objetivo principal es conectar viajeros con anfitriones de forma rápida, segura y eficiente. Permite a los usuarios explorar ofertas en tiempo real, gestionar sus reservas, emitir valoraciones y completar pagos desde una misma interfaz, ya sea desde la web o dispositivos móviles.

🎯 Valor Añadido
Plataforma todo-en-uno: Desde búsqueda hasta pago y reseñas.

Velocidad y rendimiento: Backend en GraphQL + Node.js optimizado para respuestas ágiles.

Experiencia de usuario moderna: Interfaz clara, responsive y accesible.

Orientación internacional: Preparado para varios idiomas, monedas y viajeros extranjeros.

Seguridad y confianza: Autenticación robusta y reseñas verificadas.

Geolocalización en tiempo real: Integración con Google Maps para mejorar la toma de decisiones.

🥇 Ventajas Competitivas
Ventaja	Explicación
🔒 Seguridad Avanzada	Autenticación JWT, RBAC, validación estricta, cifrado y prevención de ataques.
🧭 UX basada en mapas	Visualización de alojamientos con filtros interactivos sobre mapas.
⚙️ Backend con GraphQL	Optimización de peticiones para mejorar rendimiento en dispositivos móviles.
💬 Reseñas y reputación	Sistema de feedback entre usuarios y anfitriones.
📱 Web + Móvil desde el inicio	Arquitectura responsiva para no depender de apps nativas.
🧾 Pasarela de pago integrada	Redsys para cobros seguros y efectivos.

🧰 Funciones Principales por Rol
👤 Viajero (Usuario)
Registro y autenticación

Buscar alojamientos con filtros y mapa

Consultar detalles de propiedades

Reservar y pagar online (Redsys)

Puntuar y comentar alojamientos

🏠 Anfitrión
Registro como propietario

Publicar alojamientos

Gestionar calendario de disponibilidad

Confirmar, rechazar y cancelar reservas

Ver ingresos y feedback de usuarios

🛡️ Administrador
Moderar alojamientos y reseñas

Gestionar usuarios y roles

Resolver disputas y quejas

Panel de estadísticas

📈 Próximas Funcionalidades (Roadmap)
Integración con pasarelas internacionales (Stripe/PayPal)

Traducción automática de descripciones

Recomendaciones basadas en IA

Sistema de fidelización con puntos

## Artefacto 2: Funciones principales + Lean Canvas

✅ Funciones principales detalladas por rol

🧩 Lean Canvas del modelo de negocio de LTI -BOOK-CG

✅ Funciones Principales – LTI -BOOK-CG
👤 Viajero
Función	Descripción
Registro e inicio de sesión	Alta de usuario con verificación por correo; login seguro con JWT.
Búsqueda de alojamientos	Por destino, fecha, tipo, precio, valoración. Integrado con Google Maps.
Vista detallada de alojamiento	Fotos, servicios, ubicación, disponibilidad, precio, políticas.
Reserva y pago online	Proceso guiado de reserva + integración con Redsys.
Gestión de reservas	Cancelaciones, cambios, historial.
Reseñas y puntuaciones	Valorar del 1 al 5 estrellas y dejar comentarios una vez completada la estancia.

🏠 Anfitrión
Función	Descripción
Registro de anfitrión	Alta de perfil con validación extra (email + documento).
Publicación de alojamientos	Crear, editar y eliminar propiedades con fotos, descripción y tarifas.
Gestión de disponibilidad	Calendario de reservas sincronizado; bloqueo de fechas.
Aceptación y cancelación de reservas	Control sobre las solicitudes y modificaciones.
Resumen de ingresos	Panel de rendimiento económico por fecha y propiedad.
Interacción con usuarios	Responder dudas o comentarios dentro de la plataforma.

🛡️ Administrador
Función	Descripción
Gestión de usuarios	Alta, baja, edición, y bloqueo de perfiles.
Moderación de contenido	Reseñas, descripciones, imágenes.
Estadísticas globales	Métricas de reservas, ingresos, actividad de usuarios.
Soporte y resolución de conflictos	Acciones administrativas sobre casos reportados.

🧩 Lean Canvas – LTI -BOOK-CG
A continuación te presento el Lean Canvas del modelo de negocio, visualmente organizado para facilitar la comprensión estratégica del sistema:

🧱 Lean Canvas (Versión Texto)
Sección	Contenido
Problema	- Dificultad para reservar alojamientos alternativos a grandes plataformas.
- Falta de herramientas adaptadas a turismo nacional e independiente.
Segmentos de cliente	- Viajeros independientes y familias.
- Anfitriones pequeños y medianos.
Propuesta de valor	- Reservas seguras y rápidas.
- Visibilidad para anfitriones independientes.
- Experiencia intuitiva y moderna.
Solución	- Plataforma web y móvil con pagos integrados.
- Filtros avanzados y mapas interactivos.
- Reseñas verificadas.
Canales	- Web App, Móvil, Redes Sociales, SEO local, Google Ads.
Fuentes de ingreso	- Comisión por reserva (10%).
- Servicios premium para anfitriones.
Estructura de costes	- Infraestructura cloud.
- Integraciones API (Google Maps, Redsys).
- Desarrollo y soporte técnico.
Métricas clave	- Tasa de conversión de visitantes a reservas.
- Valor promedio por reserva.
- Retención de anfitriones.
Ventaja competitiva	- Adaptación al mercado local e internacional.
- Alta usabilidad.
- Seguridad avanzada.

## Artefacto 3: Casos de uso principales (con diagramas UML)

##chatgpt no  ha podido crear la imagen. saltamos esta parte de momento


## Artefacto 3: Casos de uso principales, cada uno con su descripción y diagrama asociado.

A continuación se presentan los tres casos de uso más importantes del sistema LTI -BOOK-CG, enfocados en las funcionalidades clave para los usuarios y anfitriones.

1️⃣ Caso de uso: Reserva de alojamiento
🎯 Objetivo:
Permitir a un usuario (viajero) reservar un alojamiento disponible, incluyendo pago seguro mediante Redsys.

🧾 Descripción:
El usuario realiza una búsqueda, selecciona un alojamiento, elige fechas disponibles, y finaliza el proceso con el pago. El sistema genera una reserva, confirma al anfitrión, y actualiza la disponibilidad.

🖼️ Diagrama UML – Reserva de alojamiento:
lua
Copia
Modifica
Actor: Usuario (Viajero)

[Usuario] --> (Buscar alojamiento)
(Seleccionar fechas) --> (Visualizar detalles)
(Visualizar detalles) --> (Confirmar reserva)
(Confirmar reserva) --> (Pago Redsys)
(Pago Redsys) --> (Generar reserva)
(Generar reserva) --> [Sistema]
[Sistema] --> (Notificar anfitrión)
[Sistema] --> (Actualizar disponibilidad)
2️⃣ Caso de uso: Publicación de alojamiento
🎯 Objetivo:
Permitir a un anfitrión registrar una nueva propiedad en la plataforma.

🧾 Descripción:
El anfitrión accede a su panel, crea un nuevo anuncio completando los campos requeridos (ubicación, fotos, descripción, tarifas, reglas), y publica el alojamiento. El sistema valida y lo pone en línea si cumple las políticas.

🖼️ Diagrama UML – Publicar alojamiento:
lua
Copia
Modifica
Actor: Usuario (Anfitrión)

[Anfitrión] --> (Acceder a panel de anfitrión)
(Acceder a panel de anfitrión) --> (Crear nuevo alojamiento)
(Crear nuevo alojamiento) --> (Completar información)
(Completar información) --> (Adjuntar fotos)
(Completar información) --> (Definir precios y disponibilidad)
(Finalizar publicación) --> [Sistema]
[Sistema] --> (Validar datos)
[Sistema] --> (Publicar en plataforma)
3️⃣ Caso de uso: Enviar y ver reseñas
🎯 Objetivo:
Permitir a un usuario que ha completado una reserva dejar una reseña del alojamiento y visualizar comentarios de otros.

🧾 Descripción:
Una vez finalizada la estancia, el sistema permite al usuario dejar una reseña y calificación. También podrá consultar opiniones de otros usuarios desde la ficha del alojamiento.

🖼️ Diagrama UML – Reseñas:
rust
Copia
Modifica
Actor: Usuario (Viajero)

[Usuario] --> (Acceder a historial de reservas)
(Seleccionar reserva completada) --> (Dejar reseña)
(Dejar reseña) --> (Ingresar comentario y estrellas)
(Enviar reseña) --> [Sistema]
[Sistema] --> (Validar comentario)
[Sistema] --> (Publicar reseña en ficha del alojamiento)

[Usuario] --> (Consultar alojamiento)
(Consultar alojamiento) --> (Ver reseñas de otros)

## Artefacto 4: Modelo de datos (entidades, atributos y relaciones)

🧩 Artefacto 4 – Modelo de Datos (Entidades, Atributos, Relaciones)
A continuación te presento una versión textual del modelo entidad-relación que cubre los principales componentes del sistema.

🧱 Entidades y Atributos
1. Usuario
id (INT, PK, auto-incremental)

nombre (VARCHAR)

apellido (VARCHAR)

email (VARCHAR, único)

password_hash (VARCHAR)

rol (ENUM: 'viajero', 'anfitrión', 'admin')

fecha_registro (DATETIME)

estado (ENUM: 'activo', 'suspendido')

2. Alojamiento
id (INT, PK)

id_anfitrion (INT, FK → Usuario.id)

titulo (VARCHAR)

descripcion (TEXT)

direccion (VARCHAR)

latitud (DECIMAL)

longitud (DECIMAL)

precio_noche (DECIMAL)

capacidad (INT)

estado_publicacion (ENUM: 'pendiente', 'activo', 'inactivo')

fecha_creacion (DATETIME)

3. Reserva
id (INT, PK)

id_usuario (INT, FK → Usuario.id)

id_alojamiento (INT, FK → Alojamiento.id)

fecha_inicio (DATE)

fecha_fin (DATE)

estado (ENUM: 'pendiente', 'confirmada', 'cancelada', 'completada')

monto_total (DECIMAL)

fecha_reserva (DATETIME)

4. Reseña
id (INT, PK)

id_usuario (INT, FK → Usuario.id)

id_alojamiento (INT, FK → Alojamiento.id)

calificacion (INT, rango 1-5)

comentario (TEXT)

fecha_reseña (DATETIME)

5. Disponibilidad
id (INT, PK)

id_alojamiento (INT, FK → Alojamiento.id)

fecha (DATE)

disponible (BOOLEAN)

6. Pago
id (INT, PK)

id_reserva (INT, FK → Reserva.id)

metodo_pago (VARCHAR, e.g., 'Redsys')

estado_pago (ENUM: 'pendiente', 'pagado', 'fallido')

fecha_pago (DATETIME)

transaccion_id (VARCHAR)

