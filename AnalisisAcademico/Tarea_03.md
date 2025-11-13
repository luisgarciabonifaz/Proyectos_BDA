# Tarea 03: Conversin CSV a Parquet

## Script

``` python

    import pandas as pd

    # Ruta del archivo CSV original
    csv_path = "Indicadores_Finales.csv"

    # Ruta donde se guardará el archivo Parquet
    parquet_path = "Indicadores_Finales.parquet"

    # Leer el CSV intentando detectar el delimitador automáticamente
    df = pd.read_csv(csv_path, sep=None, engine="python", on_bad_lines="skip")

    # Guardar como Parquet (requiere pyarrow o fastparquet)
    df.to_parquet(parquet_path, index=False)

    print(f"Conversión completa. Archivo guardado en: {parquet_path}")

```

## Requisitos

- Entorno Virtual Python
	- Crea un entorno virtual en una carpeta llamada "venv"
		- python3 -m venv ~/venv
	- Actívalo
		- source ~/venv/bin/activate
	- Ahora instala lo que quieras dentro del entorno
		- pip install pandas pyarrow
	- Después puedes ejecutar tu script dentro del entorno:
		- python convertir_csv_a_parquet.py
	- Para salir del entorno:
		- deactivate


## Validación

https://parquetreader.com/