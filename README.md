
# **Laboratorio N°7**
## **CVDS-1**
### **Ciclos de Vida del Desarrollo de Software**

![](https://github.com/DonSantiagoS/LAB2CVDS/blob/master/Imagenes/Logo.PNG)

imagen1

imagen2

````
try {
            String url="jdbc:mysql://desarrollo.is.escuelaing.edu.co:3306/bdprueba";
            String driver="com.mysql.jdbc.Driver";
            String user="bdprueba";
            String pwd="prueba2019";
                        
            Class.forName(driver);
            Connection con=DriverManager.getConnection(url,user,pwd);
            con.setAutoCommit(false);
                 
            
            System.out.println("Valor total pedido 1:"+valorTotalPedido(con, 1));
            
            List<String> prodsPedido=nombresProductosPedido(con, 1);
            
            
            System.out.println("Productos del pedido 1:");
            System.out.println("-----------------------");
            for (String nomprod:prodsPedido){
                System.out.println(nomprod);
            }

````


Verificar la configuracion del archivo para la correcta produccion de MyBATIS, observando el archivo mybatis-config.xml, ubicado en la ruta src/main/resourses verificando que tenga la siguiente configuracion despues de settings

````
<typeAliases>
    <typeAlias type='edu.eci.cvds.samples.entities.Cliente' alias='Cliente'/>
    <typeAlias type='edu.eci.cvds.samples.entities.Item' alias='Item'/>
    <typeAlias type='edu.eci.cvds.samples.entities.ItemRentado' alias='ItemRentado'/>
    <typeAlias type='edu.eci.cvds.samples.entities.TipoItem' alias='TipoItem'/>
</typeAliases>	
````



##### Autores:
 * Santiago Buitrago
 * Andres Cubillos

[1]:https://es.wikipedia.org/wiki/Telnet
[2]:https://tools.ietf.org/html/rfc2616
[3]:https://docs.oracle.com/javaee/7/api/javax/faces/webapp/FacesServlet.html
[4]:https://users.dcc.uchile.cl/~jbarrios/servlets/general.html
