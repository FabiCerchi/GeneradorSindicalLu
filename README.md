# Generador Categorias Sindicales :smile:

Se debe generar un csv delimitado por comas donde la primera fila son para los campos.

### Campos:

1. Category name: nombre de la categoria a crear. Ej: Supervisor Administrativo
2. Category period: pago que pertecene a esta categoria puede ser month o hour
3. Codigo Cat: Codigo custom que le asignaremos a la categoria para diferenciarla del resto. Ej: S1
4. From Date: Desde que empieza a regir el BASICO. Ej 01/01/2022 (Estrictamente debe ser en este formato)
5. Value: Sueldo base que se le asigna al From Date: Ej: 100000
    
Si hay muchas versiones de la misma categoria debe completarlas todas en la fila que corresponde indicando siempre **FROM DATE ** **VALUE**

Al finalizar la ejercucion se generará un archivo en pdf en la carpeta SRC para incrustrarlo en el xml que estemos trabajando (catergory_price)


### Configuracion main.py

1. Al descargar el proyecto nos vamos a encontrar con la carpeta **Data** en esta carpeta ubicaremos el archivo.csv delimitado por comas
2. Ingresando al main debemos configurar el la ruta del csv y el nombre del sindicato:


`path = Path("../data/fatsa_csv2.csv").resolve()`
 `sindicato = "fatsa"`

3. Abrir la consola en la ubicacion del proyecto y ejecutar el comando python main.py