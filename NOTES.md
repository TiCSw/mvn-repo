# Notes for the Maven Repository

- [FeatureIDE libraries](#featureide-libraries)
- [Eclipse dependencies](#eclipse-dependencies)
- [Epsilon libraries](#epsilon-libraries)
- [Eclipse UML2 libraries](#eclipse-uml2-libraries)

---

### FeatureIDE libraries

FeatureIDE libraries included in this repository has dependencies to libraries in both, this same repository and the Maven Central. Libraries included in Maven Central are not included in this repository.

To use the FeatureIDE libraries, you can specify the following dependencies:
```xml
		<!-- FeatureIDE --> 
		<dependency>
			<groupId>de.ovgu.featureide</groupId>
			<artifactId>de.ovgu.featureide.lib.fm</artifactId>
			<version>3.5.3</version>
		</dependency>
		<!-- optional support for feature models with attributes -->	
		<dependency>
			<groupId>de.ovgu.featureide</groupId>
			<artifactId>de.ovgu.featureide.lib.fm.attributes</artifactId>
			<version>3.5.3</version>
		</dependency>
``` 


### Eclipse dependencies

Eclipse plugins included in the repository has dependencies to plugins/libraries in the Maven Central. The Eclipse plugis included in Maven central are not included in this repository.

For instance, the Eclipse EMF (Juno) dependencies in Maven Central may be specified as follows:
```xml
		<dependency>
			<groupId>org.eclipse.emf</groupId>
			<artifactId>org.eclipse.emf.common</artifactId>
			<version>2.9.2-v20131212-0545</version>
		</dependency>	
		<dependency>
			<groupId>org.eclipse.emf</groupId>
			<artifactId>org.eclipse.emf.ecore</artifactId>
			<version>2.9.2-v20131212-0545</version>
		</dependency>
		<dependency>
			<groupId>org.eclipse.emf</groupId>
			<artifactId>org.eclipse.emf.ecore.xmi</artifactId>
			<version>2.9.1-v20131212-0545</version>
		</dependency>
``` 
The following are th eEMF (Luna) dependencies:

```xml 
		<dependency>
			<groupId>org.eclipse.emf</groupId>
			<artifactId>org.eclipse.emf.common</artifactId>
			<version>2.10.0-v20140514-1158</version>
		</dependency> 
		<dependency>
			<groupId>org.eclipse.emf</groupId>
			<artifactId>org.eclipse.emf.ecore</artifactId>
			<version>2.10.0-v20140514-1158</version>
		</dependency>
		<dependency>
			<groupId>org.eclipse.emf</groupId>
			<artifactId>org.eclipse.emf.ecore.xmi</artifactId>
			<version>2.10.0-v20140514-1158</version>
		</dependency>
		<dependency>
			<groupId>org.eclipse.xsd</groupId>
			<artifactId>org.eclipse.xsd</artifactId>
			<version>2.10.0</version>
		</dependency>
		<!-- required for UML -->
		<dependency>
			<groupId>org.eclipse.emf</groupId>
			<artifactId>org.eclipse.emf.mapping.ecore2xml</artifactId>
			<version>2.8.0-v20140519-0339</version>
		</dependency>
```

In addition, a dependency to the Eclipse Core Runtime may be specified as the following:

```xml
		<dependency>
			<groupId>org.eclipse.core</groupId>
			<artifactId>org.eclipse.core.runtime</artifactId>
			<version>3.7.0</version>
		</dependency>
```

### Epsilon libraries

> **NOTE:** Starting from version 1.4.0, released at 2016, there are Epsilon packages in the [Maven central](https://mvnrepository.com/artifact/org.eclipse.epsilon).

[Epsilon plugins/libraries][epsilon] are included in this repository. The following were obtained from the [Epsilon download page][epsilon-downloads]:

* v1.2, the version included in Eclipse Luna(4.4)
* v1.x, the version included in the original [Epsilon EGL Servlet][epsilon-egl-servlet].

There are others that have not been included (yet) in the repository:

* v1.1_SR1, an update to the version included in Eclipse Kepler(4.3)
* v1.1, the version included in Eclipse Kepler(4.3)
* v1.0, the version included in Eclipse Juno(4.2)


[epsilon]: http://eclipse.org/epsilon/download/
[epsilon-downloads]: http://eclipse.org/epsilon/download/
[epsilon-egl-servlet]: https://www.eclipse.org/epsilon/doc/articles/egl-server-side/

The dependencies for these plugins/libraries have been defined using the MANIFEST files and the information provided in the [download page][epsilon-downloads]. 

* Epsilon Core, v1.2
  * **NOTE:** Antlr runtime, v3.1.1, is included in the .jar
* Epsilon EMF, v1.2 
  * Epsilon Core, v1.2
  * Eclipse EMF Common, v2.10.0.v20140514-1158
  * Eclipse EMF Ecore, v2.10.0.v20140514-1158
  * Eclipse EMF Ecore XMI, v2.10.0.v20140514-1158
  * Eclipse EMF XSD, v2.10.0.v20140519-0339
* Epsilon UML, v1.2
  * Epsilon Core, v1.2
  * Eclipse EMF Mapping Ecore2Xml, v2.8.0.v20140519-0339
  * Eclipse UML2 Common, v2.0.0.v20140602-0749 
  * Eclipse UML2 Types, v2.0.0.v20140602-0749
  * Eclipse UML2 UML, v5.0.0v20140602-0749
* Epsilon GraphML, v1.2
  * Epsilon Core, v1.2
  * org.Jdom JDOM, v1.1.2
* Epsilon HUTN, v1.2
  * Epsilon Core, v1.2  

The dependencies for the v1.x plugins were obtained from the Epsilon EGL Servlet project.

* Epsilon Core, v1.x
  * Antlr runtime, v3.1.1
* Epsilon EOL engine, v1.x
  * Antlr runtime, v3.1.1
* Epsilon EMF, v1.x
  * Eclipse EMF Common, 2.9.2-v20131212-0545
  * Eclipse EMF Ecore, 2.9.2-v20131212-0545
  * Eclipse EMF Ecore XMI, 2.9.2-v20131212-0545
 * Epsilon GraphML, v1.x
  * org.Jdom JDOM, v1.1.2

### Eclipse UML2 libraries
  
The Eclipse UML2 libraries (required by Epsilon UML) are not included in the Maven Central. There are only old versions (dated on 2010).  The following are the dependencies for that plugins:
  
* Eclipse UML2 Common, v2.0.0.v20140602-0749
  * Eclipse Core Runtime (v3.5+), v.3.7.0
  * Eclipse EMF Ecore, v2.10.0.v20140514-1158
* Eclipse UML2 Types, v2.0.0.v20140602-0749
  * Eclipse UML2 Common, v2.0.0.v20140602-0749
* Eclipse UML2 UML, v5.0.0v20140602-0749
  * Eclipse UML2 Common, v2.0.0.v20140602-0749
  * Eclipse UML2 Types, v2.0.0.v20140602-0749
  * Eclipse EMF Ecore XMI, v2.10.0.v20140514-1158
  * Eclipse EMF Mapping Ecore2Xml, v2.8.0.v20140519-0339

  