# MySql-Scripting

/* problem: you want to run Java-based programs in a web environment.

solution: write programs using JSP notation and execute them using a servlet container such as Tomcat. */

Using the JDBC driver

1. To install Connector/J for use by Tomcat applications, place a copy of it in Tomcat's directory tree. Assuming that the driver

is packaged as a JAR file (as is the case for Connector/J), there are different places under the Tomcat root directory where you

can install it, depending on how visible you want the driver to be: 


2.To make the driver available both to Tomcat and to applications, place it in the lib directory under the Tomcat root.


Installing the JSTL distribution

1. Get JSTL from the Apache Standard Taglibs project page (http://bit.ly/tagslibs), which has a download link from which you can get a binary JSTL distribution.
Get version 1.1.2 or higher.

2. Unpack the JSTL distribution into some convenient location, preferably outside of the Tomcat hierarchy.

3. Unpacking the distribution creates a directory containing several directories and files. Change the file location into the lib directory 
and copy the jstl.jar and standard.jar JAR files to the mcb/WEB-INF/lib directory. Those files contain the classes that implement the JSTL tag actions,
and tag library descriptor files that define the interface for the actions implemented by the classes.

4. the JSTL <sql:setDataSource> tag is used to setup a datasource for connecting to a database. The file looks like this:

<sql:setDataSource
var="conn"
driver="com.mysql.jdbc.Driver"
url="jdbc:mysql://localhost/cookbook"
user="cbuser"
password="cbpass"
/>

Edit the url, user, and password tag attributes if necessary to change the connection parameters to those that you use for 
accessing your database. 

5. restart Tomcat so it notices the changes.


Eclipse Info

1. With respect to Dynamic Web Projects, (connector/J) is required in webapps, web-inf in the lib directory. The driver allows your app to connect MySQL with Tomcat.
2. Now your web server and database are primed to start scripting using JSTL and JSP directives.
3. Now you can generate web content from query results such as: displaying query results as paragraphs, list, unordered list, definition list, nested list, tables, hyperlinks, and work with nav indexs.
4. You are also now setup to begin processing web content using MySQL.
