# Bio-Analizador de Variantes Genómicas (Bash Pipeline)

Proyecto final del curso: Principios de Programación en Bioinformática (1ABL0014).
Este repositorio contiene herramientas desarrolladas en Bash para el procesamiento eficiente, filtrado y análisis comparativo de archivos en formato VCF (Variant Call Format) de *Drosophila melanogaster*.

## Estructura del Proyecto

1.  **`script1.sh`**: Análisis profundo mono-muestra. Permite realizar estadísticas detalladas sobre un único archivo genómico.
2.  **`Multi_muestra_menu.sh`**: Pipeline avanzado para procesamiento en lote. Automatiza la comparación de múltiples muestras, filtrado de calidad y cálculo de ratios mutacionales.

## Características Técnicas

* **Procesamiento al vuelo**: Uso intensivo de `zgrep` y `awk` para procesar archivos comprimidos (`.vcf.gz`) sin necesidad de extraerlos, optimizando el uso de disco.
* **Filtrado Biológico**: Identificación y separación automática de SNPs puros (longitud REF/ALT = 1).
* **Análisis Poblacional**: Cálculo del ratio **Ts/Tv** (Transiciones/Transversiones), métrica estándar de calidad genómica para evaluar la fidelidad de la secuenciación.
* **Interfaz Dinámica**: Menú interactivo que permite al usuario seleccionar qué métricas desea extraer, ideal para demos en vivo y optimización de recursos computacionales.

### Requisitos
* Sistema: Cloud Shell.
* Archivos en formato `.vcf.gz`.

### Ejecución
1.  Dar permisos de ejecución:
    ```bash
    chmod +x Multi_muestra_menu.sh
    ```
2.  Ejecutar el pipeline:
    ```bash
    ./Multi_muestra_menu.sh /ruta/a/tu/directorio/con/archivos
    ```**
