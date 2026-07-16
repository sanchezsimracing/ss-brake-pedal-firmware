# Sanchez SimRacing Pedal de Freno: Guia de Usuario

## Contenido de la Caja

- Unidad controladora del pedal de freno
- Cable USB

---

## Instalacion

El controlador esta disenado para reemplazar el potenciometro de tu pedal de freno existente.

### Cables de Señal

El dispositivo tiene dos cables:

| Color del cable | Conectar a |
|-----------------|-----------|
| **Negro** | Cable de masa del pedal |
| **Blanco** | Cable de señal del pedal |

Conecta los cables a los pines de masa y señal que usaba el potenciometro original. Deja el **cable rojo (alimentacion)** del pedal conectado al potenciometro original; el controlador no lo utiliza.

### Alimentacion (USB)

El dispositivo se alimenta a traves de su puerto **USB**. Conectalo a:

- **Tu PC**: necesario si quieres usar el plugin de SimHub (ver [Plugin de SimHub](#plugin-de-simhub))
- **Cualquier fuente de 5 V**: como un cargador de telefono, si solo necesitas la salida analogica

> **Si el dispositivo se reinicia solo constantemente**, no esta recibiendo suficiente energia. Prueba con otro puerto USB de tu PC (los puertos traseros de la placa base suelen ser mas confiables que los frontales o los de un hub) y evita cables USB extensores. Este problema normalmente no ocurre con cargadores de telefono u otros adaptadores de energia dedicados.

---

## Primeros Pasos

### 1. Encendido

Conecta tu pedal al simulador como de costumbre. El controlador se enciende automaticamente.

### 2. Primera Configuracion Wi-Fi

El pedal crea su propia red Wi-Fi para configuracion. Se genera una nueva contraseña en el primer encendido, por lo que necesitas obtenerla una vez:

1. Manten presionado el **boton** durante **3 segundos** para entrar en modo de recuperacion. Sabras que lo mantuviste el tiempo suficiente cuando la luz comience a parpadear muy rapido; suelta el boton en ese momento (mantenerlo mas tiempo activara una restauracion de fabrica).
2. En tu telefono o PC, busca las redes Wi-Fi disponibles. Aparecera una red que comienza con **SS Brake Pedal**; conectate a ella. No se requiere contraseña en modo de recuperacion.
3. La pagina de configuracion se abre automaticamente. Tu nueva contraseña Wi-Fi aparece en pantalla. **Guardala en un lugar seguro.**

> **Consejo:** En la mayoria de telefonos y laptops aparecera automaticamente un aviso de "Iniciar sesion en la red" al conectarte. Si no aparece, abre un navegador y ve a **http://192.168.4.1**.

A partir de ahora, presiona el **boton** una vez para activar el Wi-Fi y usa la contraseña guardada para conectarte.

### 3. Calibrar (opcional)

El pedal esta listo para usar desde el primer momento: la calibracion del punto cero se realiza automaticamente en cada arranque, y el rango maximo viene configurado al 100 % (capacidad total del sensor) por defecto. Si quieres ajustar estos valores a tu configuracion, consulta la seccion [Calibracion](#calibracion).

---

## Luz de Estado

| Patron de luz | Significado |
|---------------|-------------|
| Pulso corto cada 3 s | Funcionamiento normal |
| Doble destello, pausa (repetido) | Modo de configuracion Wi-Fi activo |
| Triple destello, pausa (repetido) | Modo de recuperacion activo (sin contraseña) |
| Parpadeo rapido continuo | Problema detectado. Revisa todas las conexiones |
| Parpadeo muy rapido continuo | Conteo regresivo de restauracion de fabrica |

---

## Boton

| Pulsacion | Accion |
|-----------|--------|
| Pulsacion corta | Activar o desactivar el modo de configuracion Wi-Fi |
| Mantener 3 segundos | Iniciar **modo de recuperacion** (sin contraseña) |
| Mantener 10 segundos | **Restauracion de fabrica**: borra todos los ajustes |

---

## Modo de Configuracion Wi-Fi

El punto de acceso Wi-Fi se apaga automaticamente tras **5 minutos** sin actividad. Puedes cambiar este comportamiento en [Configuracion](#configuracion).

Para volver a conectarte en cualquier momento, presiona el boton nuevamente.

---

## Calibracion

Abre la interfaz web y desplazate hasta la seccion **Ajuste Fino** (la calibracion de cero y el rango maximo ahora estan alli, junto a la curva de respuesta y la zona muerta).

### Establecer Punto Cero

Por defecto, el pedal se calibra automaticamente en cada arranque; asegurate de que el pedal este completamente suelto durante el primer segundo o dos despues de encender el simulador.

Si prefieres un punto cero fijo que no cambie al reiniciar, puedes desactivar esta funcion en [Configuracion](#configuracion) (**Calibrar al iniciar**). Luego podras establecer el punto cero manualmente en cualquier momento:

1. Suelta completamente el pedal de freno, sin ningun tipo de presion.
2. Toca **Punto cero**.

### Establecer Rango Maximo

Por defecto el pedal utiliza el rango completo del sensor (100 %). Si tu configuracion o estilo de conduccion requiere un maximo mas liviano, puedes reducirlo:

Desliza el control de **Rango maximo** hasta el valor deseado (5–100 %) y sueltalo. El valor se guarda automaticamente. Un porcentaje menor significa que la salida de frenado al maximo se alcanza con menos fuerza fisica.

> **Vuelve a calibrar cuando:** montes el pedal en una nueva posicion, o notes que el punto cero se ha desplazado despues de calentar.

---

## Perfiles

Cuatro perfiles te permiten cambiar rapidamente entre distintas configuraciones, por ejemplo uno para carreras en circuito y otro para endurance o condiciones de lluvia.

Cada perfil almacena su propio rango maximo, curva de respuesta y zona muerta.

### Cambiar de Perfil

Toca cualquier boton de perfil. El perfil activo se resalta en rojo. Los ajustes se cargan de inmediato.

### Guardar un Perfil

Los cambios de ajuste tienen efecto inmediato, pero no se almacenan en ningun perfil hasta que guardes explicitamente. Si cambias a otro perfil y vuelves, los cambios sin guardar seran sobreescritos por lo que estaba guardado en ese slot.

Para guardar los ajustes actuales en el perfil activo:

1. Ajusta la curva de respuesta, la zona muerta y el rango maximo a tu gusto.
2. Toca **Renombrar** si quieres darle un nombre (hasta 15 caracteres).
3. Toca **Guardar**.

---

## Ajuste Fino

La seccion **Ajuste Fino** reune todo lo que define la sensacion del pedal (la curva de respuesta, la zona muerta, el rango maximo y la calibracion de cero) en un solo lugar.

### Curva de Respuesta

Controla como la fuerza del pedal se traduce en la salida de frenado. La curva tiene **seis puntos** que puedes arrastrar, en 0, 20, 40, 60, 80 y 100 % de la entrada del pedal. Cada punto define la salida de frenado (0–100 %) en esa entrada: arrastralo hacia arriba para mas salida, hacia abajo para menos. Un punto no puede cruzar a sus vecinos, asi que la respuesta siempre es suave y nunca se invierte. Un punto blanco indica donde se encuentra tu pedal en la curva en cada momento.

Los **preajustes** te dan un punto de partida con un solo toque, que luego puedes afinar arrastrando los puntos:

| Preajuste | Sensacion |
|-----------|-----------|
| **Linear** | La salida es proporcional a la entrada (1:1) |
| **S-Curve** | Mas suave en los extremos, mas firme en el centro |
| **Expo** | Mas sensibilidad al inicio del recorrido, con control fino para modular |
| **Inverse** | Mas resolucion cerca del pedal a fondo, util para un punto de frenado firme |

### Zona Muerta

Porcentaje del recorrido del pedal al inicio que se ignora. Util para evitar frenadas fantasma por flexion del pedal o vibraciones.

- **0%**: sin zona muerta; cualquier movimiento se registra
- **2–5%**: punto de partida recomendado para la mayoria de configuraciones
- **Hasta 20%**: para configuraciones muy sensibles o con mucho ruido

---

## Configuracion

| Ajuste | Que hace |
|--------|----------|
| **Detener al desconectar** | Apaga el Wi-Fi en cuanto te desconectas de la pagina de configuracion |
| **Mantener Wi-Fi activo** | Desactiva el apagado automatico; el punto de acceso permanece encendido hasta que lo desactives manualmente |
| **Calibrar al iniciar** | Recalibra automaticamente el punto cero cada vez que el dispositivo arranca |

> Si **Mantener Wi-Fi activo** esta habilitado, **Detener al desconectar** se desactiva automaticamente.

---

## Grafico de Presion en Vivo

La seccion **Presion en vivo** muestra un grafico desplazable de 6 segundos de tu entrada de freno:

- **Linea roja**: la señal de salida real enviada al simulador (con la curva de respuesta aplicada)
- **Linea tenue**: tu entrada directa del pedal como referencia

---

## Estado del Hardware

La seccion **Hardware** muestra un **✓ OK** verde cuando todo funciona correctamente. Si se muestra un codigo de error en rojo, hay una falla interna de hardware:

| Codigo | Significado |
|--------|-------------|
| **E01** | Problema con el sensor de carga |
| **E02** | Problema con la salida analogica |

Si aparece alguno de estos codigos, revisa todas las conexiones de cables y reinicia el pedal. Si el error persiste, por favor contacta a **Sanchez SimRacing** para recibir asistencia.

---

## Actualizacion de Firmware

La interfaz web incluye una seccion de **Firmware** en la parte inferior de la pagina. Muestra la version actual del firmware y permite instalar una nueva.

El Wi-Fi del pedal no provee acceso a internet. El telefono no puede descargar nada mientras esta conectado al pedal, asi que descargar el archivo e instalarlo son dos pasos separados.

**Paso 1: descargar el archivo.** Mientras todavia tienes internet, desde cualquier dispositivo, entra a:

**sanchezsimracing.com.ar/firmware**

Descarga el archivo **.bin** de la ultima version. La seccion **Firmware** de la interfaz web muestra esta misma direccion, y puedes tocarla para copiarla.

**Paso 2: instalarlo.**

1. Conectate al Wi-Fi del pedal y abre la interfaz web.
2. Toca **Seleccionar archivo .bin** y elige el archivo que descargaste.
3. Toca **Actualizar Firmware** y confirma cuando se te solicite.
4. Una barra de progreso mostrara el estado de la subida. Una vez completada, el dispositivo se reinicia automaticamente con el nuevo firmware.

> **Nota:** Solo se aceptan archivos de firmware firmados por Sanchez SimRacing. Si el archivo es invalido o no reconocido, la actualizacion sera rechazada y no se realizara ningun cambio.

---

## Plugin de SimHub

Un plugin complementario para [SimHub](https://www.simhubdash.com/) permite configurar y monitorear el pedal directamente desde tu PC, sin necesidad de Wi-Fi. El cable USB debe estar conectado a la PC.

### Instalar el Plugin

1. Descarga **SSBrakePedal.dll** desde la seccion [Releases](https://github.com/sanchezsimracing/ss-brake-pedal-simhub-plugin/releases/latest) del repositorio del plugin.
2. Copia el archivo en la carpeta de instalacion de SimHub (generalmente `C:\Program Files (x86)\SimHub\`).
3. Reinicia SimHub.

El plugin aparece en **Additional Plugins → SS Brake Pedal** en el menu izquierdo.

### Conexion

El plugin detecta automaticamente el pedal en cualquier puerto COM al iniciar SimHub. Si no se conecta automaticamente (por ejemplo, si el pedal se conecto despues de iniciar SimHub), abre el panel del plugin y haz clic en **Connect**.

> El dispositivo tarda hasta ~5 segundos en arrancar completamente al encenderse por primera vez. El plugin espera el tiempo suficiente para esto.

### Que se Puede Hacer desde SimHub

| Funcion | Descripcion |
|---------|-------------|
| **Live Brake Position** | Barras en tiempo real mostrando la salida con curva (lo que ve el juego) y la entrada lineal cruda |
| **Curva de respuesta / Deadzone / Max Range** | Los mismos controles de ajuste que la interfaz web. Arrastra un punto o elige un preajuste y los cambios se aplican al instante |
| **Set Zero** | Recalibrar el punto cero sin abrir la interfaz web |
| **Profiles** | Cargar, renombrar y guardar cualquiera de los cuatro perfiles |

> Todos los ajustes realizados desde SimHub se guardan en el dispositivo y persisten tras reiniciar; son los mismos ajustes que se ven en la interfaz web por Wi-Fi.

---

## Idioma

Toca el selector de idioma (EN / ES) en la esquina superior derecha de la pagina web. La preferencia se guarda en el dispositivo.

---

## Olvide o Cambiar la Contraseña Wi-Fi

Manten presionado el boton durante **3 segundos** para entrar en modo de recuperacion. Esto genera una nueva contraseña y abre la red Wi-Fi sin requerir la anterior. Conectate a la red **SS Brake Pedal** y la interfaz web mostrara tu nueva contraseña; guardala en un lugar seguro.

Al reiniciar, se requerira la nueva contraseña.

---

## Restauracion de Fabrica

Una restauracion de fabrica borra todos los perfiles, datos de calibracion y ajustes, y genera una nueva contraseña Wi-Fi.

**Para restaurar de fabrica:**
- Manten presionado el boton durante **10 segundos** (la luz parpadeara muy rapido como advertencia del conteo regresivo)

Tras la restauracion el dispositivo reinicia desde cero. Deberas volver a calibrar y configurarlo.

---

## Reinicio

Toca **Reiniciar** al final de la interfaz web (toca dos veces para confirmar). El dispositivo reinicia en unos segundos.

---

## Garantia

El pedal cuenta con la garantia legal de **6 meses** desde la fecha de entrega (Ley 24.240, Argentina), que cubre los defectos de fabricacion o de funcionamiento. El responsable de la garantia es **Sanchez SimRacing**.

La garantia no cubre daños causados por golpes, humedad, uso indebido, modificaciones al dispositivo o una instalacion distinta a la indicada en esta guia.

Para hacer un reclamo, contactanos a **support@sanchezsimracing.com.ar** describiendo el problema y la version de firmware que muestra la interfaz web. Evaluaremos el caso y, si el defecto esta cubierto, repararemos o reemplazaremos el dispositivo sin cargo.

Esta garantia no limita los derechos que la ley reconoce al consumidor.

---

## Devolucion de una Compra a Distancia

Si compraste el pedal por internet o por otro medio de venta a distancia, tienes derecho a revocar la compra dentro de los **10 dias corridos** desde que lo recibiste (art. 34, Ley 24.240).

Para ejercer este derecho, contactanos a **support@sanchezsimracing.com.ar** dentro de ese plazo, conservando el producto completo y en buen estado. Coordinaremos la devolucion y el reembolso.

---

## Soporte

Para cualquier consulta o problema, contactanos en:

**support@sanchezsimracing.com.ar**
