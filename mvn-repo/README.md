# TiCSw Maven Repository
A Maven repository for TiCSw (for libraries not available in Maven Central) 

### What is this?

This is a Maven repository for some libraries that do not include information about their dependencies or include errors in it. 

More information in the [mvn-repo project in Github][github-project]. 

### Usage

In order to use the repository in your projects, you must include the repository information in your ``pom.xml``.

```xml
	<repositories>
		<repository>
			<id>ticsw-mvn-repo</id>
			<url>http://ticsw.github.io/mvn-repo/</url>
		</repository>
	</repositories>
``` 

In order to install and use a local maven repository, you may check the documentation in the [mvn-repo project in Github][github-project].

[github-project]: https://github.com/ticsw/mvn-repo 