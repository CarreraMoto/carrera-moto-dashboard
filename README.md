# Dashboard Royal Enfield - Carrera Moto

Este repositorio contiene un dashboard interactivo para visualizar métricas y KPIs de Carrera Moto y Royal Enfield Aguascalientes. El dashboard puede conectarse a Google Sheets para actualizar automáticamente los datos.

## Vista previa

![Dashboard Preview](https://via.placeholder.com/800x400?text=Dashboard+Royal+Enfield)

## Características

- Visualización de KPIs clave (demos, satisfacción CTA, reseñas)
- Gráficos interactivos de métricas mensuales
- Distribución de ventas por modelo
- Integración con Google Sheets para actualización automática de datos
- Diseño responsivo adaptable a diferentes dispositivos
- Sección de acciones recomendadas basadas en datos

## Requisitos previos

- Cuenta de GitHub
- Cuenta de Google
- Hoja de cálculo de Google Sheets con la estructura de datos requerida
- Proyecto en Google Cloud con API de Google Sheets habilitada

## Configuración e Instalación

### 1. Configurar Google Sheets

1. Crea una nueva hoja de cálculo en Google Sheets siguiendo la estructura descrita en [estructura-google-sheets.md](estructura-google-sheets.md)
2. Comparte la hoja con permisos de lectura pública o con una cuenta de servicio específica
3. Anota el ID de la hoja de cálculo (está en la URL: `https://docs.google.com/spreadsheets/d/[ID_DE_LA_HOJA]/edit`)

### 2. Configurar Google Cloud y API Key

1. Ve a [Google Cloud Console](https://console.cloud.google.com/)
2. Crea un nuevo proyecto o selecciona uno existente
3. Habilita la API de Google Sheets
   - Ve a "APIs y servicios" > "Biblioteca"
   - Busca "Google Sheets API" y habilítala
4. Crea una clave de API
   - Ve a "APIs y servicios" > "Credenciales"
   - Haz clic en "Crear credenciales" > "Clave de API"
   - Restringe la clave para que solo se pueda usar con la API de Google Sheets y desde tu dominio
   - Copia la clave de API generada

### 3. Configurar el repositorio en GitHub

1. Crea un nuevo repositorio en GitHub
2. Clona este repositorio en tu máquina local
3. Copia los archivos de este repositorio a tu repositorio local

### 4. Configurar la conexión con Google Sheets

1. Abre el archivo `google-sheets-connector.js`
2. Reemplaza `TU_ID_DE_HOJA_DE_CALCULO` con el ID de tu hoja de cálculo
3. Reemplaza `TU_API_KEY` con la clave de API que creaste en Google Cloud
4. Ajusta los rangos de celdas según sea necesario para que coincidan con tu hoja de cálculo

### 5. Actualizar el dashboard según tus necesidades

1. Abre el archivo `index.html` para personalizar:
   - Título y subtítulo del dashboard
   - Logos y colores
   - Estructuras de datos específicas si es necesario

### 6. Desplegar en GitHub Pages

1. Sube tus cambios al repositorio
   ```
   git add .
   git commit -m "Initial dashboard setup"
   git push origin main
   ```

2. Activa GitHub Pages:
   - Ve a la página de tu repositorio en GitHub
   - Haz clic en "Settings" > "Pages"
   - En "Source", selecciona la rama "main" y carpeta "/" (raíz)
   - Haz clic en "Save"
   - Espera unos minutos y tu dashboard estará disponible en `https://[tu-usuario].github.io/[nombre-repositorio]/`

## Actualización automática de datos

El dashboard se conectará automáticamente a Google Sheets cada vez que se cargue la página. Para configurar una actualización automática periódica:

1. Puedes usar servicios como IFTTT o Zapier para activar una actualización de tu hoja de cálculo a intervalos regulares
2. Otra opción es programar un script de Google Apps Script en tu hoja de cálculo para actualizar datos automáticamente

## Estructura de archivos

- `index.html` - El dashboard principal
- `google-sheets-connector.js` - Script para conectar con Google Sheets
- `structure.md` - Información sobre la estructura de datos requerida
- `README.md` - Este archivo
- `/assets` - Carpeta para logos, imágenes y otros recursos

## Solución de problemas

### El dashboard no muestra datos
- Verifica que la API key de Google sea válida y tenga los permisos correctos
- Asegúrate de que la hoja de cálculo sea accesible públicamente o para la cuenta que usa la API
- Revisa la consola del navegador (F12) para ver si hay errores específicos

### Los gráficos no se muestran correctamente
- Verifica que los datos en Google Sheets tengan el formato correcto (números, no texto)
- Asegúrate de que los rangos de celdas en el conector coincidan con tu hoja

## Personalización avanzada

Para personalizar aún más tu dashboard:

1. **Cambiar colores**: Modifica las clases de Tailwind CSS en el archivo HTML
2. **Agregar más gráficos**: Usa la documentación de Recharts para agregar nuevos tipos de visualizaciones
3. **Añadir secciones**: Expande el diseño agregando nuevas tarjetas o secciones según tus necesidades

## Contribuciones

Las contribuciones son bienvenidas. Si deseas mejorar este dashboard:

1. Haz un fork del repositorio
2. Crea una rama para tu característica (`git checkout -b feature/amazing-feature`)
3. Haz commit de tus cambios (`git commit -m 'Add some amazing feature'`)
4. Haz push a la rama (`git push origin feature/amazing-feature`)
5. Abre un Pull Request

## Contacto

Carrera Moto - [correo@carreramoto.com](mailto:correo@carreramoto.com)

---

**Nota**: Este dashboard está diseñado específicamente para Carrera Moto y Royal Enfield Aguascalientes.
