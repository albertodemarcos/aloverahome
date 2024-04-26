Proyecto de Raspberry pi 4

Tiene instalado:
  Ubuntu 22.04
  Tomcat 9.0.85: /opt/tomcat/apache-tomcat-9.0.85
  Java 11
  PostgreSQL

Comandos importantes

systemctl status tomcat
systemctl start tomcat
systemctl stop tomcat

tail 1000 -f /opt/tomcat/apache-tomcat-9.0.85/logs/catalina.out (logs del tomcat)

chown -R tomcat:tomcat /opt/tomcat/apache-tomcat-9.0.85/webapps/homecarmama-vx.x.x
chmod -R 755 /opt/tomcat/apache-tomcat-9.0.85/webapps/homecarmama-vx.x.x


Otros

En webapps se meten los wars de las aplicaciones java para poder ser desplegados
Puede ser via aplicacion web o con el comando curl

curl -L -o homecamarma-v1.0.0.war "https://github.com/albertodemarcos/aloverahome/releases/download/v1.0.0/homecamarma-v1.0.0.war"

En ambos casos tienes que dar permisos sobre el war para que tomcat puede obtenerlo

Conexion wifi
  ver todas las conexiones: nmcli connection show
  conectar: nmcli dev wifi connect SSID_de_tu_red password contraseña
  desconectar: nmcli connection down nombre_de_conexión
  conectar de nuevo: nmcli connection up nombre_de_conexión

URL:

curl -X GET http://tu-dominio.com/ 
curl -X GET http://tu-dominio.com/inicio
curl -X GET http://tu-dominio.com/home
curl -X POST http://tu-dominio.com/ -H "Content-Type: application/json" -d '{"nombreUsuario": "tuNombreUsuario", "contrasena": "tuContrasena"}'
curl -X PUT http://tu-dominio.com/actualizar -H "Content-Type: application/json" -d '{"nombreUsuario": "nombreActualizado", "contrasena": "contrasenaActualizada"}'
curl -X DELETE http://example.com/usuario/123







