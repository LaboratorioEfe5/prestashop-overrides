# Optative DNI

La idea es hacer el campo dni optativo cuando se solicita.
Para ello se ha tomado de base lo comentado en:
http://www.loading.es/clientes/knowledgebase/202/Como-hacer-el-DNI-opcional-en-Prestashop-15x.html

Dado que lo que se indica en el texto es hacer un overwrite (sustituir archivos del core) 
se ha tomado como alternativa hacer override (utilizar el método ofrecido por prestashop para este tipo de
modificaciones)

En la versión 1.6.0.9 Parece no funcionar 
Así que se han realizado pequeñas modificaciones

Para usar el override:

* Verificar si ya se han creado override de los archivos AuthController.php y AddressController.php
* Si existen será necesario integrar el código en el que ya hay
* Si no existen: Copiar la carpeta override dentro del prestashop
* En el theme utilizado es recomendable quitar la marca de obligatorio para el campo dni en authentication.tpl y en address.tpl

Para localizar el cambio buscar: 
//--> mod
//--> fin mod