# Java Notes:
## Servlets:
- The name of a servlet is s different from the servlet class. A servlet class can have multiple names and different urls. Imagine having a servlet class that implement the same logic for two different servlets that conntect to two different databases. Basically one servlet class can map to multiple servlet names and urls.
- To configure a project to run on a local container like tomcat, right click tomcat on Servers in the bottom in eclipse (I know this is bad) and click on add/remove.
- **Context params** get defined in the deployment descriptor `web.xml` and one can get them with
```java
ServletContext s = HttpServlet.getServletContext();
```
- Within The deployment descriptor, we use the `<context-param>` as in:
```xml
<context-param>
	<param-name>database</param-name>
	<param-value>msql</param-value>
</context-param>
```
- `<context-param>` should be listed under the `web-app` tag. Context params are app-wide. For specific servlets, **init params** are used.
- `@MultipartConfig` annotation is used to control file upload. In a file descriptor, `<multipart-config>` tag can be put in a `<servlet>` tag to do the same job.

## JSP:
- **JSPs** combine java code, html tags, built-in jsp tags, custom jsp tags and expression language. They are used to create dynamic html pages.
- JSPs are fancy servlets. They are compiled into java code.
