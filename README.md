# Consultor del Clima

Esta es una aplicación que te permite obtener el clima actual, la temperatura mínima y máxima de una ciudad y país específico utilizando la API de "Weather API". Con WeatherApp, podrás obtener de manera rápida y sencilla la información climática que necesitas para planificar tus actividades.

## Componentes

Se crearon varios componentes para brindar una experiencia de usuario fluida:

- **Alerta**: El componente `Alerta` se utiliza para mostrar mensajes de validación del formulario. Si hay algún error al buscar la ciudad y el país, este componente mostrará una alerta para informar al usuario sobre el problema.

- **Clima**: El componente `Clima` muestra la respuesta obtenida de la API de "Weather API". Aquí se presenta el clima actual, la temperatura mínima y máxima para la ciudad y país seleccionados.

- **Formulario**: El componente `Formulario` permite al usuario ingresar la ciudad y el país que desea consultar para obtener la información climática. Al enviar el formulario, se realizará la solicitud a la API para obtener los datos correspondientes.

- **Spinner**: El componente `Spinner` es una animación de carga (loading) que se muestra mientras se espera la respuesta de la API. Proporciona una experiencia visual agradable mientras la aplicación está realizando la solicitud.

## Composables

Se ha utilizado el composable `useClima` para encapsular toda la lógica de la petición a la API "Weather API". Este composable maneja la solicitud HTTP utilizando Axios y procesa la respuesta para obtener la información climática necesaria.

## Variables de Entorno

Para mantener la seguridad de la API key utilizada en la solicitud a la API "Weather API", se ha empleado el uso de variables de entorno. De esta manera, la clave de acceso se encuentra protegida y no se expone en el código fuente.

## Funcionalidades y Conceptos Reforzados

- **Emits**: Los componentes utilizan emisiones de eventos personalizados para comunicar datos entre sí. Por ejemplo, cuando el formulario se envía con la ciudad y el país seleccionados, se emite un evento para que el composable `useWeatherAPI` realice la solicitud a la API.

- **v-model**: La directiva `v-model` se ha utilizado para vincular los datos ingresados por el usuario en el formulario con el estado del componente `Formulario`.

- **Props**: El componente `Clima` recibe los datos obtenidos de la API como props para mostrar la información climática actual.

- **Conexión a la API con Axios**: Hemos utilizado Axios para realizar la solicitud a la API "Weather API" y obtener los datos climáticos en tiempo real.

- **Composables**: Hemos utilizado el composable `useClima` para encapsular y reutilizar la lógica relacionada con la petición a la API y el procesamiento de la respuesta.

- **Variables de Entorno**: Se han utilizado variables de entorno para proteger la API key y mantenerla segura dentro del código fuente.

## Instalación y Uso

Para utilizar WeatherApp en tu entorno local, sigue estos pasos:

1. Clona este repositorio: `git clone https://github.com/euss99/clima-vue.git`
2. Navega a la carpeta del proyecto: `cd clima-vue`
3. Instala las dependencias: `npm install`
4. Inicia el servidor de desarrollo: `npm run serve`
5. Abre tu navegador y visita: `http://localhost:5173`

¡Listo! Ahora puedes utilizar la app para obtener la información climática actual de cualquier ciudad y país que desees.
