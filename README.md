# Taller: Precipitación Máxima Probable (PMP)

**Autora:** Jocelyn Lugo Soza  


---

## Instrucciones para ejecutar en Google Colab

Sigue estos pasos obligatorios para configurar el entorno y los datos antes de ejecutar el código:

### 1. Descargar y descomprimir los datos
1. Descarga el archivo comprimido enviado: `Datos_taller.zip` o del enlace " https://drive.google.com/drive/folders/13qe4tEGFIoXPcOdMW4CiJVhM5i4UEcRG?usp=drive_link "
2. Descomprime el archivo en tu computadora. 
3. Obtendrás una carpeta principal llamada **`Datos taller`** que contiene todos los archivos `.nc` junto con las subcarpetas `mascara` y `shp`.

### 2. Subir la carpeta a Google Drive
1. Entra a tu **Google Drive**.
2. Dirígete a la carpeta llamada **`Colab Notebooks`** (si no existe en tu unidad, créala con ese nombre exacto, respetando las mayúsculas).
3. **Arrastra y suelta** la carpeta descompuesta **`Datos taller`** completa dentro de `Colab Notebooks`.

> **IMPORTANTE**: No alteres el nombre de ningún archivo ni subcarpeta. La estructura final en tu Google Drive debe quedar exactamente de la siguiente forma:
> ```text
> Mi Unidad/
> └── Colab Notebooks/
>     └── Datos taller/
>         ├── mascara/
>         │   └── Maipo.nc
>         ├── shp/
>         │   ├── Maipo.shp
>         │   ├── Maipo.shx
>         │   └── Maipo.dbf
>         ├── humedad_19840701.nc
>         ├── humedad_19840705.nc
>         ├── pr_CR2.nc
>         ├── pw_ejemplo.nc
>         ├── pw_horzv10.nc
>         ├── pw_tormentas.nc
>         └── tormentas.nc
> ```

### 3. Verificar la Ruta en el Notebook
Al abrir el notebook en Colab, asegúrate de que la celda de **Conexión a Drive** defina la ruta de la variable `carpeta` apuntando al directorio que acabas de subir:

```python
# Comprueba que tu celda tenga esta ruta exacta:
carpeta = '/content/drive/MyDrive/Colab Notebooks/Datos taller'
```

### 4. Ejecución del Código
1. Abre el archivo del notebook (`.ipynb`) desde este repositorio de GitHub.
2. Ejecuta la primera celda (**Configuración Inicial**) para instalar automáticamente el entorno y las librerías espaciales requeridas (`cartopy`, `rioxarray`, `geopandas`, etc.).
3. Ejecuta la segunda celda (**Conexión a Drive**). Google Colab abrirá una ventana emergente pidiéndote acceso de lectura. Inicia sesión con tu cuenta y selecciona **Permitir**.
4. Corre el resto de las celdas del taller en orden secuencial.

---

## Requisitos del Entorno (Instalación Automática)
El script se encarga de preparar el entorno virtual de Colab instalando e importando:
* **Análisis Espacial y Climático:** `xarray`, `netcdf4`, `geopandas`, `rioxarray`
* **Manejo de Matrices y Estadísticas:** `numpy`, `pandas`, `scipy`
* **Visualizaciones y Mapas:** `matplotlib`, `plotly`, `cartopy`
