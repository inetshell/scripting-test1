## Ejercicio:
Realizar un script que lea el archivo __input1.dat__ y genere los archivos __query.sql__ y __schema.dat__.

## Requisitos
1. El script debe tener tres parametros de entrada:
   - El archivo de entrada
   - Nombre de la base de datos
   - Nombre de la tabla
2. Debe ser posible agregar nuevas lineas al archivo de entrada y que genere las salidas correspondientes.

## Ejemplo
```bash
user@host:~/$ script.sh input1.dat DB TB

user@host:~/$ cat query.sql
SELECT CAST("ID" AS VARCHAR(4)), CAST("FEC_CORTE" AS VARCHAR(16)), CAST(CAST(TRIM("SALDO") AS NUMBER) AS VARCHAR(8)), CAST("CONCEPTO" AS VARCHAR(25)) FROM DB.TB;

user@host:~/$ cat schema.dat
"ID" VARCHAR(14), "FEC_CORTE" VARCHAR(26), "SALDO" VARCHAR(18), "CONCEPTO" VARCHAR(35)
```

## Notas
* El script debe correr sobre un equipo CentOS 7 que tiene python27, bash, grep, sed y awk.
