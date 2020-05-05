# apache-olingo-odata2
An example of how to implement OData Version 2 with Apache

# Run with Tomcat
Necessary steps to get your project run with [Tomcat](https://tomcat.apache.org/)

1. Download and install Maven (http://maven.apache.org/) and put its `bin` folder in path!
2. Download [Tomcat](https://tomcat.apache.org/download-90.cgi) and install it.
3. Download and import the project as a Maven project in Eclipse, incase you have problem for opening it in Eclipse,
   type the following command in a terminal in the project folder: `mvn eclipse:clean eclipse:eclipse`.
   As result each Maven module will get a consistent `.project`, `.classpath` and `.settings` file with which each module can be imported as existing project to Eclipse.
4. Open a terminal windows in the Eclipse and type `mvn clean install`.
5. A `.war` file will be generated in the `\apache-olingo-odata2\odata-web\target` folder that you can deploy in Tomact.
6. In the Tomcat you need to activate the slash in the URL. In Windows run the `Tomcat9w.exe` file.  
   Click the Java tab. In the Java Options field, enter: 

   `-Dorg.apache.tomcat.util.buf.UDecoder.ALLOW_ENCODED_SLASH=true` 
   
   and then restart the Tomcat service.
7. Enjoy running the OData in browser. 
