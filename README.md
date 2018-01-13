# One_model para Codeigniter
Este fichero es una clase php que maximiza el dominio en el controlador.

**Indice**
* [Instalación](#instalacion)
* [Inicialización](#inicializacion)
* [Utilización](#utilizacion)
	- [Add](#add)
	- [Update](#update)
	- [Delete](#delete)
	- [Add_batch](#add_batch)
	- [Get](#get)
	- [Get_array](#get_array)
	- [Get_count](#get_count)
	- [Get_where](#get_where)
	- [Get_where_array](#get_where_array)
	- [Get_where_count](#get_where_count)
	- [Get_select](#get_select)
	- [Get_select_array](#get_select_array)
	- [Get_select_where](#get_select_where)
	- [Get_select_where_array](#get_select_where_array)
	- [Get_join](#get_join)
	- [Get_join_array](#get_join_array)
	- [Get_likes](#get_likes)
	- [Get_likes_array](#get_likes_array)
	- [Get_likes_count](#get_likes_count)
	- [Get_order](#get_order)

## Instalación
El fichero Global_model.php se coloca dentro de la carpeta application/models/

## Inicialización
Para inicializar la clase en el controlador, dentro del constructor o metodo tu cargas el modelo

`$this->load->model('Global_model');`

## Utilización
### Add
Metodo para insertar datos en la table

`$data = $this->Global_model->Add($table, $array)`
* @param $table: String //Nombre de la table
* @param $array: Array //Contiene el array a añadir
* @return: Int

### Update
Metodo para actualizar datos en la tabla

`$data = $this->Global_model->Update($table, $array)`
* @param $table: String //Nombre de la tabla
* @param $where: Array //Condicion en array u objeto
* @param $array: Array //Nombre del objeto a modificar
* @return: string

### Delete
Metodo para eliminar datos en la tabla

`$data = $this->Global_model->Delete($table, $array)`
* @param $table: String //Nombre de la tabla
* @param $where: Array //Condicion en array u objeto
* @param $array: Array //Nombre del objeto a modificar
* @return: string

### Add_batch
Metodo para insertar datos en la table

`$data = $this->Global_model->Add_batch($table, $array)`
* @param: $table: String //Nombre de la table
* @param: $array: Array //Contiene el arrays a importar
***
### Get
Metodo para obtener datos de una tabla

`$data = $this->Global_model->Get($table, $allrows, $params)`
* @param $table: String //Nombre de la tabla
* @param $allrows: Boolean //Si es TRUE? Recupera todas las filas: En otro caso recupera una fila
* @param $params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de objetos

### Get_array
Metodo para obtener datos de una tabla

`$data = $this->Global_model->Get_array($table, $allrows, $params)`
* @param $table: String //Nombre de la tabla
* @param $allrows: Boolean //Si es TRUE? Recupera todas las filas: En otro caso recupera una fila
* @param $params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de arrays

### Get_count
Metodo para obtener la cantidad de filas de una tabla

`$data = $this->Global_model->Get_count($table)`
* @param $table: String //Nombre de la tabla
* @return: int

### Get_where
Metodo para obtener datos de una tabla con una condición

`$data = $this->Global_model->Get_where($table, $where, $allrows, $params)`
* @param $table: String //Nombre de la tabla
* @param $where: Array //Contiene la condición a cumplir
* @param $allrows: Boolean //Si es TRUE? Recupera todas las filas: En otro caso recupera una fila
* @param $params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de objetos

### Get_where_array
Metodo para obtener datos de una tabla con una condición

`$data = $this->Global_model->Get_where_array($table, $where, $allrows, $params)`
* @param $table: String //Nombre de la tabla
* @param $where: Array //Contiene la condición a cumplir
* @param $allrows: Boolean //Si es TRUE? Recupera todas las filas: En otro caso recupera una fila
* @param $params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de arrays

### Get_where_count
Metodo para obtener la cantidad de datos de una tabla con una condición

`$data = $this->Global_model->Get_where_count($table, $where)`
* @param $table: String //Nombre de la tabla
* @param $where: Array //Contiene la condición a cumplir
* @return: Int

### Get_select
Metodo para obtener datos de una tabla con determinados campos

`$data = $this->Global_model->Get_select($field, $table, $allrows, $params)`
* @param $field: String //Nombre del campo o de los campos
* @param $table: String //Nombre de la tabla
* @param $allrows: Boolean //Si es TRUE? Recupera todas las filas: En otro caso recupera una fila
* @param $params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de objetos

### Get_select_array
Metodo para obtener datos de una tabla con determinados campos

`$data = $this->Global_model->Get_select_array($field, $table, $allrows, $params)`
* @param $field: String //Nombre del campo o de los campos
* @param $table: String //Nombre de la tabla
* @param $allrows: Boolean //Si es TRUE? Recupera todas las filas: En otro caso recupera una fila
* @param $params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de arrays

### Get_select_where
Metodo para obtener datos de una tabla con determinados campos

`$data = $this->Global_model->Get_select_where($field, $table, $where, $allrows, $params)`
* @param $field: String //Nombre del campo o de los campos
* @param $table: String //Nombre de la tabla
* @param $where: Array //Contiene la condición a cumplir
* @param $allrows: Boolean //Si es TRUE? Recupera todas las filas: En otro caso recupera una fila
* @param $params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de objetos

### Get_select_where_array
Metodo para obtener datos de una tabla con determinados campos

`$data = $this->Global_model->Get_select_where_array($field, $table, $where, $allrows, $params)`
* @param $field: String //Nombre del campo o de los campos
* @param $table: String //Nombre de la tabla
* @param $where: Array //Contiene la condición a cumplir
* @param $allrows: Boolean //Si es TRUE? Recupera todas las filas: En otro caso recupera una fila
* @param $params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de objetos

### Get_join 
(Experimental) Metodo para obtener datos de una tabla unida a otra tabla

`$data = $this->Global_model->Get_join($field, $table1, $table2, $condition, $join, $allrows, $params)`
* @param $field: String //Nombre del campo o de los campos
* @param $table1: String //Nombre de la tabla
* @param $table2: String //Nombre de la tabla
* @param $condition: String	//Condición de unión
* @param $join: String //Lugar de unión
* @param $allrows: Boolean //Si es true? Recupera todas las filas: Recupera una fila
* @param params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de objetos

### Get_join_array
(Experimental) Metodo para obtener datos de una tabla unida a otra tabla

`$data = $this->Global_model->Get_join_array($field, $table1, $table2, $condition, $join, $allrows, $params)`
* @param $field: String //Nombre del campo o de los campos
* @param $table1: String //Nombre de la tabla
* @param $table2: String //Nombre de la tabla
* @param $condition: String	//Condición de unión
* @param $join: String //Lugar de unión
* @param $allrows: Boolean //Si es true? Recupera todas las filas: Recupera una fila
* @param params: Array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de arrays

### Get_likes
Metodo para obtener datos de una tabla con condición de busqueda

`$data = $this->Global_model->Get_likes($titles, $table, $allrows, $params)`
* @param $titles: Array //Contiene la condición de busqueda
* @param $table: String //Nombre de la tabla
* @param $allrows: Boolean //Si es true? Recupera todas las filas: Recupera una fila
* @param $params: array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de objetos

### Get_likes_array
Metodo para obtener datos de una tabla con condición de busqueda

`$data = $this->Global_model->Get_likes_array($titles, $table, $allrows, $params)`
* @param $titles: Array //Contiene la condición de busqueda
* @param $table: String //Nombre de la tabla
* @param $allrows: Boolean //Si es true? Recupera todas las filas: Recupera una fila
* @param $params: array //Contiene los valores el $params['limit'] y $params['offset']"
* @return: array de arrays

### Get_likes_count
Metodo para obtener la cantidad de datos de una tabla con una condición de busqueda

`$data = $this->Global_model->Get_likes_array($titles, $table)`
* @param $titles: Array //Contiene la condición de busqueda
* @param $table: String //Nombre de la tabla
* @return: Int

### Get_order
Metodo para obtener datos de una tabla con condición de orden

`$data = $this->Global_model->Get_order($field, $direction, $table, $result, $params, $count))`
* @param $field: String //Nombre del campo
* @param $direction: String //Parametro de direccion
* @param $result: Boolean //Si es true? retorna array de objetos: retorna array de arrays
* @param $params: Array	//Contiene los valores el $params['limit'] y $params['offset']"
* @return: array


