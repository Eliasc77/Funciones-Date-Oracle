# Funciones-Date-Oracle
#### Las funciones de Fecha y Hora son funciones que nos permite manejar fechas en nuestra bd y en ese sentido las bd de oracle almacenan las fechas en un formato numerico interno que represeta desde el siglo, el año, el mes , el dia, el minuto y hasta los segundos manejando todo esto con un tipo de formato **date**

> Fundion add_months :agrega a una fecha un numero de meses, si el segundo argumento es positivo se le suma a la fecha envia la cantidad de meses y si es negativo pues se resta a la fecha enviada tanto como se le indique en el segundo argumento
```sql
select add_months(to_date('10/10/2020', 'dd/mm/yyyy'),5) from dual;
```
|ADD_MONTHS(TO_DATE(to_date('10/10/2020', 'dd/mm/yyyy'),5)|
|:-------------------------------------------:|
|10-MAR-21|
