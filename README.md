# Funciones-Date-Oracle
#### Las funciones de Fecha y Hora son funciones que nos permite manejar fechas en nuestra bd y en ese sentido las bd de oracle almacenan las fechas en un formato numerico interno que represeta desde el siglo, el año, el mes , el dia, el minuto y hasta los segundos manejando todo esto con un tipo de formato **date**

> Fundion add_months :agrega a una fecha un numero de meses, si el segundo argumento es positivo se le suma a la fecha envia la cantidad de meses y si es negativo pues se resta a la fecha enviada tanto como se le indique en el segundo argumento
```sql
select add_months(to_date('10/10/2020', 'dd/mm/yyyy'),5) from dual;
```
|ADD_MONTHS(TO_DATE(to_date('10/10/2020', 'dd/mm/yyyy'),5)|
|:-------------------------------------------:|
|10-MAR-21|

___

> Funcion last_day : trae el ultimo dia de la fecha del mes indicado

```sql
select last_day(to_date('09/02/2022', 'dd/mm/yyyy')) from dual;
```
|LAST_DAY(TO_DATE(to_date('09/02/2022', 'dd/mm/yyyy'))|
|:-------------------------------------------:|
|29-FEB-22|

> Funcion moths_between : retorna el numero de meses entre las fechas enviadas como argumento en una ejecucion

```sql
select months_between(to_date('19/05/2020', 'dd/mm/yyyy'), to_date ('19/08/2020', 'dd/mm/yyyy'))as meses from dual;
```
|meses|
|:-------------------------------------------:|
|-3|
##### indica que hay 3 meses de diferencia
___

> Funcion next_day: retorna una fecha correspondiente al primer dia especifica en dia y luego de la fecha que se le pase a la ejecucion // dentro de la fecha indicada dinos q dia es lunes y se salta la fecha indicada

```sql
select next_day(to_date('28/02/2022', 'dd/mm/yyyy'),'lunes') from dual;
```
|NEXT_DAY(to_date('28/02/2022', 'dd/mm/yyyy'),'lunes')|
|:-------------------------------------------:|
|17-aug-20|

___

> Funcion current_date nos trae la fecha y hora del calendario acutal
```sql
select current_date from dual;
```
|current_date|
|:-------------------------------------------:|
|04/04/2022|
___

> Funcion sysdate : fecha del sistema que tiene nuestra bd q puede ser diferente a la fecha del calendario y sie sta diferente quiere decir que esta mal omologado
```sql
select sysdate from dual;
```

___
> Funcion current_timestamp : nos trae la fecha y hora correspondiente a nuestra configuracion regional es decir a la configuracion que tengamos en nuestro equipo
```sql
select current_timestamp from dual;
```
|CURRENT_TIMESTAMP|
|:-------------------------------------------:|
|04/04/2022 09.12.43.34324343 AM AMERICA / LIMA|

___
> funcion systimestamp : retorna la fecha y hora actual configurada del sistema
```sql
select systimestamp from dual;
```
|SYSTIMESTAMP|
|:-------------------------------------------:|
|04/04/2022 09.12.43.34324343 AM -04:00|


___
>Funcion to_char :combierte una fecha a cadena de caracteres
```sql
select to_char ('10/10/2020') from dual;
```
|TO_CHAR('10/10/2020')|
|:-------------------------------------------:|
|10/10/2022|

