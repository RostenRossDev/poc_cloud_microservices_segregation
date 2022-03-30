# poc_cloud_microservices_segregation
Prueba de concepto de segregacion de configuraciones para diferentes canales, incluye un 
config server generico y posiblemente 1 config server particular por cada canal, un apigateway, un
eureka server y un cliente que va a tener varios canales y cada canal varias instancias. 
El origen de las propiedades de configuracion estaran en una base de datos relacional, el 
config server sera avisado de una actualizacion, luego de eso el config server se actualizaria 
con su endpoint /actuator/refresh, luego de configar que se actualiza deberia de propagar la 
actualizacion a las instancias del canal que corresponda para que se actualizen ellas tambien. 
Se actualizara con mas info mas adelante.
