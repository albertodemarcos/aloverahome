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

curl -LJO [URL_DIRECTA_AL_ARCHIVO_WAR]


En ambos casos tienes que dar permisos sobre el war para que tomcat puede obtenerlo












