# TiCSw Maven Repository
A Maven repository for libraries not available in Maven Central used in some TiCSw projects.

### What is this?

This is a Maven repository for some libraries that do not include or have errors in the information about their dependencies. 
[Maven][maven] is a software building system that keep track of dependencies. When a developer defines a dependency for a project, Maven use that information to download the libraries and all the transitive dependencies before building. In addition, developers may use Maven tools to detect errors and conflicts.

However, there are many java libraries that does not include information about dependencies that may used by Maven. In addition, many projects built using Maven, such as some [Eclipse][eclipse] plugins created with [Maven Tycho][tycho], includes information about dependencies that cannot be used outside Eclipse (e.g. web applications).

[maven]: http://maven.apache.org/
[eclipse]: https://eclipse.org/
[tycho]: https://eclipse.org/tycho/

### Usage

In order to use the repository in your projects, you can use a Github-hosted or a local repository. In both cases, must include the repository information in your ``pom.xml``.

To use the Github-hosted repository, you must include the following:

```xml
	<repositories>
		<repository>
			<id>ticsw-mvn-repo</id>
			<url>http://ticsw.github.io/mvn-repo/</url>
		</repository>
	</repositories>
``` 

To use a local repository, you must install this project and include the information of your local installation in your ``pom.xm``

```xml
	<repositories>
		<!-- An example local Maven repository -->			
		<repository>
			<id>local-mvn-repo</id>
			<name>Maven local repository</name>
			<url>file:${project.basedir}/mvn-local-repo</url>
			<releases>
				<updatePolicy>never</updatePolicy>
			</releases>
		</repository>
	</repositories>
``` 

### Install

In order to install this Maven repository in other location, you must customize the ``build.xml`` file.

To use a local directory in the same project:

    	<property 
    	    name="deploy.repository.url" 
			 value="${basedir}/mvn-local-repo" />

To install the libraries in your local Maven repository:

		<property 
		    name="deploy.repository.url" 
			 value="${user.home}/.m2/repository" />

After modifying the script, you can run it using the command line

    $ ant build.xml

Or using Eclipse:

1. Select the ``mvn-repo`` project in Eclipse
2. Select the ``build.xml`` file
3. Run the script using "Run As > Ant Build".

### Local Repository

After running the script, a new folder is created with a local Maven repository. The script creates the repository in the ``mvn-local-repo`` folder. (This folder is not included in the Git repository)  
