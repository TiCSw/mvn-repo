# Notes for the Maven Repository

Eclipse plugins included in the repository has dependencies to plugins/libraries in the Maven Central.

For instance, the Eclipse EMF (Luna) dependencies in Maven Central may be specified as follows:
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