CONTRATO de api 

1. csv a otro separador
endpoint: api/v1/csv-a-otro-separador/
metodo: POST
body: {
    "lista_archivos_csv_at": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250201_F20250227.csv",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250301_F20250331.csv", 
    ],
    "antiguo_separador": ";",
    "nuevo_separador": "|"
}
RESPONSE 200:
response: {
    "csv": "archivo.zip"
}

2. sav a csv

endpoint: api/v1/sav-a-csv/
metodo: POST
body: {
    "lista_archivos_sav": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/SAV/ARCHIVO_COLJ_I20250101_F20250131.sav",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/SAV/ARCHIVO_COLJ_I20250201_F20250227.sav",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/SAV/ARCHIVO_COLJ_I20250301_F20250331.sav", 
    ],
}
RESPONSE 200:
response: {
    "csv": "archivo.zip"
}

3. txt a csv
endpoint: api/v1/txt-a-csv/
metodo: POST
body: {
    "lista_archivos_txt": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/TXT/ARCHIVO_COLJ_I20250101_F20250131.txt",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/TXT/ARCHIVO_COLJ_I20250201_F20250227.txt",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/TXT/ARCHIVO_COLJ_I20250301_F20250331.txt", 
    ],
    "separador_entrada": "|",
    "separador_salida": "|"
}
RESPONSE 200:
response: {
    "csv": "archivo.zip"
}

4. xlsx a csv
endpoint: api/v1/xlsx-a-csv/
metodo: POST
body: {
    "lista_archivos_xlsx": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/XLSX/ARCHIVO_COLJ_I20250101_F20250131.xlsx",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/XLSX/ARCHIVO_COLJ_I20250201_F20250227.xlsx",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/XLSX/ARCHIVO_COLJ_I20250301_F20250331.xlsx", 
    ],
    separador_salida:"|"
}
RESPONSE 200:
response: {
    "csv": "archivo.zip"
}

5. xlsx a csv con columna mes de reporte
endpoint: api/v1/xlsx-a-csv-con-columna-mes-de-reporte/
metodo: POST
body: {
    "lista_archivos_xlsx": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/XLSX/ARCHIVO_COLJ_I20250101_F20250131.xlsx",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/XLSX/ARCHIVO_COLJ_I20250201_F20250227.xlsx",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/XLSX/ARCHIVO_COLJ_I20250301_F20250331.xlsx", 
    ],
    "separador_salida":"|"
}
RESPONSE 200:
response: {
    "csv": "archivo.zip"
}

6. unir archivos csv
endpoint: api/v1/unir-archivos-csv/
metodo: POST
body: {
    "lista_archivos_csv": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250201_F20250227.csv",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250301_F20250331.csv", 
    ],
    "separador_salida":"|"
}
RESPONSE 200:
response: {
    "csv": "archivo.zip"
}

7. unir archivos csv en xlsx
endpoint: api/v1/unir-archivos-csv-en-xlsx/
metodo: POST
body: {
    "lista_archivos_csv": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250201_F20250227.csv",
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250301_F20250331.csv", 
    ],
    "separador_salida":"|"
}
RESPONSE 200:
response: {
    "xlsx": "archivo.zip"
}
----------------------------------------------------
8. Normalizar columnas coljuegos disciplinarios
endpoint: api/v1/normalizar-columnas/coljuegos/disciplinarios/
metodo: POST
body: {
    "archivo_limpiar": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
    ],
    "nombre_archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "nombre_archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",

}
RESPONSE 200:
response: {
    "archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",
}

9. Normalizar columnas coljuegos pqr
endpoint: api/v1/normalizar-columnas/coljuegos/pqr/
metodo: POST
body: {
    "archivo_limpiar": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
    ],
    "nombre_archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "nombre_archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",

}
RESPONSE 200:
response: {
    "archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",
}

10. Normalizar columnas Dian defensoria
endpoint: api/v1/normalizar-columnas/Dian/defensoria/
metodo: POST
body: {
    "archivo_limpiar": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
    ],
    "nombre_archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "nombre_archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",

}
RESPONSE 200:
response: {
    "archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",
}
11. Normalizar columnas Dian disciplinarios
endpoint: api/v1/normalizar-columnas/Dian/disciplinarios/
metodo: POST
body: {
    "archivo_limpiar": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
    ],
    "nombre_archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "nombre_archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",

}
RESPONSE 200:
response: {
    "archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",
}
12. Normalizar columnas Dian notificaciones
endpoint: api/v1/normalizar-columnas/Dian/notificaciones/
metodo: POST
body: {
    "archivo_limpiar": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
    ],
    "nombre_archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "nombre_archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",

}
RESPONSE 200:
response: {
    "archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",
}

13. Normalizar columnas Dian pqr
endpoint: api/v1/normalizar-columnas/Dian/pqr/
metodo: POST
body: {
    "archivo_limpiar": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
    ],
    "nombre_archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "nombre_archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",

}
RESPONSE 200:
response: {
    "archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",
}

14. Normalizar columnas ugpp disciplinarios
endpoint: api/v1/normalizar-columnas/ugpp/disciplinarios/
metodo: POST
body: {
    "archivo_limpiar": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
    ],
    "nombre_archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "nombre_archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",

}
RESPONSE 200:
response: {
    "archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",
}

15. Normalizar columnas ugpp pqr
endpoint: api/v1/normalizar-columnas/ugpp/pqr/
metodo: POST
body: {
    "archivo_limpiar": [
        "~/Documentos/ITRC/DOCUMENTOS_LIMPIAR/copia_COLJUEGOS_PQRS/2025/CSV/ARCHIVO_COLJ_I20250101_F20250131.csv",
    ],
    "nombre_archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "nombre_archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",

}
RESPONSE 200:
response: {
    "archivo_salida": "ARCHIVO_COLJ_I20250101_F20250131_procesado.csv",
    "archivo_errores": "ARCHIVO_COLJ_I20250101_F20250131_errores_procesamiento.csv",
}