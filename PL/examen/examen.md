# Control Práctico de Redes de Computadores, dic 2022
## Ejercicio 1 (1 punto)
Interconecta sobre el papel los siguientes dispositivos suponiendo que ninguno de ellos dispone de tecnología Auto-MDIX. Utiliza un trazo continuo para representar un cable direecto y un trazo discontinuo para representar un cable cruzado.

**Enlaces que debes representar (12 en total):**
- Hub0 con Pc0 y Switch0
- Router0 con Switch0, Router1 y Router3
- Switch1 con PC1 y Router1
- PC3 con Router3
- Router2 con Router1, Router3 y Hub1
- PC2 con Hub1

\*esquema en packet tracer con varios dispositivos\*

## Ejercicio 2 (2 puntos)
Crea un fichero de texto y llámalo **ejercicio2.txt**. Escribe en él los comandos necesarios, usando *TCPRewrite* y *TCPReplay*. para modificar y posteriormente enviar a la red el fichero *VoIP.cap* situado en la máquina virtual Redes Máquina A. Los cambios solicitados son los siguientes:
- Direcciones físicas de origen CC:BB:AA:CC:BB:AA y de destino 33:22:11:33:22:11.
- Direcciones IP de origen 192.168.10.2 y de destino 111.111.111.111.
- El paquete debe enviarse a la red 8 veces consecutivas.

## Ejercicio 3 (4 puntos)
En la figura siguiente se muestra el diseño de red de una empresa. La red está dividida en cuatro subredes, cada una de un tamaño distinto. La red A1 necesita alojar a 6 hosts, la A2 a 20 hosts, la B a 4 hosts y la de C a 32 hosts. También necesitaremos dos redes punto a punto (redes con dos direcciones asignables) para los enlaces entre routers.

\*figura en packet tracer con lo anterior\* (cada subred tiene un solo pc y un switch, cada pc tiene el nombre "PC <nombre_subred>".)

Sigue los pasos indicados a continuación para crear un modelo de esta red con Packet Tracer.


### Ejercicio 3.1 (0,5 puntos)
Crea el escenario anterior en Packet Tracer y llámalo **ejercicio3**. Arrastra los dispositivos necesarios al espacio de trabajo teniendo en cuenta lo siguiente:
- Los routers a utilizar deben ser del modelo 2911.
- Los switches deben ser del modelo 2960.
- Utiliza el modelo genérico para los PC.
Conecta los dispositivos utilizando las interfaces que proceda.


### Ejercicio 3.2 (0,5 puntos)
El edificio que albergará toda esta red tiene asignada la dirección de red IP 156.156.156.128/25, que deberá dividirse en subredes de la forma más ajustada posible. Indica a continuación la dirección de red de cada subred (junto con su máscara de subred), así como la primera y la última dirección IP asignable en cada una de ellas.

| Subred     | Dirección de red | Máscara | Primera IP asignable | Última IP asignable |
| ---------- | ---------------- | ------- | -------------------- | ------------------- |
| A1         |                  |         |                      |                     |
| A2         |                  |         |                      |                     |
| B          |                  |         |                      |                     |
| C          |                  |         |                      |                     |
| Router 1-3 |                  |         |                      |                     |
| Router 2-3           |                  |         |                      |                     |


### Ejercicio 3.3 (1,25 puntos)
Configura estáticamente los parámetros de red en los PC y *routers* del escenario anterior, teniendo en cuenta lo siguiente: para cada subred, la primera dirección disponible se deberá asignar a la puerta de enlace y la última al PC. No olvides configurar también las interfaces *GigabitEthernet* utilizadas para conectar los *routers* entre sí, de acuerdo a lo respondido en la tabla de la pregunta anterior.

- Comprueba que cada PC puede hacer ping a su puerta de enlace.
- ¿Funciona un ping entre PCA1 y PCA2?
- ¿Funciona un ping entre PCA1 y PCC?

### Ejercicio 3.4 (0,75 puntos)
Configura en los *routers* Router1 y Router2 un *gateway* de último recurso, en ambos casos con destino a Router3.

### Ejercicio 3.5 (0,75 puntos)
Configura en Router3 tres rutas estáticas individuales, para que este sea capaz de alcanzar las subredes A1, A2 y B.

### Ejercicio 3.6 (0,25 puntos)
Una vez configurado todo el escenario, guarda en cada router su configuración en la memoria no volátil.

## Ejercicio 4
Diseña la siguiente red LAN en Packet Tracer. Para ello, crea un escenario y llámalo **ejercicio4**.

\* diseño en packet tracer \*

### Ejercicio 4.1 (0,5 puntos)
Asigna direcciones IP del rango 120.120.100.0/25 a los dos servidores, el PC de Internet y la interfaz que conecta el Router0 con el Switch0.

La red que conecta el Router0 con el *router* Maestro tiene que utilizar un rango de direcciones con máscara /30. Elige una dirección que consideres correcta y asígnasela a la interfaz del Router0 que lo conecta con el *router* Maestro.

### Ejercicio 4.2 (1 punto)
Activa y configura el servidor FTP un usuario con permisos de listado y descarga. En el servidor DNS crea una tabla llamada *servidorftp.net* que permita acceder al servidor FTP utilizando ese nombre.

### Ejercicio 4.3 (1 punto)
Configura el *router* Maestro para que su red local interna sea la 10.10.10.240/28. Modifica el SSID de su red WiFi para que se llame *EduRoam*. Conecta el PC local al *router* Maestro a través de una conexión cableada, y el Portátil mediante una conexión inalámbrica. El PC local debe obtener su IP de forma estática mientras que el portátil debe obtenerla mediante DHCP.

Configura manualmente los parámetros de red de *router* Maestro en su conexión hacia Internet de manera que sus datos coincidan con los que has puesto en el apartado 4.1.

### Ejercicio 4.4 (0,5 puntos)
Descarga del servidor FTP en el PC local y el Portátil el fichero *asa842-k8.bin*. Asegúrate de que puedes acceder a dicho servidor utilizando la dirección *servidorftp.net*.
