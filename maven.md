📦 Maven: A Tool for Your Java Project
Maven is a tool for your Java projects. It helps you build your code and manage other programs you need. It is better than doing it all yourself.

What is a pom.xml file?
This is an XML file. It tells Maven about your project. It has:

<groupId>, <artifactId>, and <version>: This is the name of your project.

<dependencies>: This lists other programs your project needs.

<build> and <plugins>: These are special parts that tell Maven how to build your project.

What are Dependencies?
Dependencies are other programs your project needs to work. Maven gets them for you.

scope test: Some programs are only for tests, like JUnit. They are not for your main code.

Maven saves these programs on your computer in a folder here: ~/.m2/repository.

What are Plugins?
Plugins are special parts of Maven that do things.

The compiler plugin builds your Java code.

The surefire plugin runs your tests.

Common Maven Commands
Here are some commands you use a lot:

mvn clean: Clean your project.

mvn compile: Build your code.

mvn test: Run your tests.

mvn install: Build and save your program on your computer.

mvn dependency:tree: See all the programs your project needs.

I hope this simple version is helpful for you. Let me know if you need any other changes!
