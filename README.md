# bigdata_assignment

Set up development environment for JDK and Maven

Step1 : Generate Maven example project
```
mvn archetype:generate `
  -D archetypeGroupId=org.apache.beam `
  -D archetypeArtifactId=beam-sdks-java-maven-archetypes-examples `
  -D archetypeVersion=2.42.0 `
  -D groupId=org.example `
  -D artifactId=word-count-beam `
  -D version="0.1" `
  -D package=org.apache.beam.examples `
  -D interactiveMode=false
  ```
  Step 2: Change into word-count-beam
 ```
  cd .\word-count-beam
```
Step 3: directory contains a pom.xml and a src directory with example pipelines.
 ```
   dir .\src\main\java\org\apache\beam\examples
```
 Step 4: Run wordcount using Maven
    ```
    mvn compile exec:java -D exec.mainClass=org.apache.beam.examples.WordCount `
 -D exec.args="--inputFile=sample.txt --output=counts" -P direct-runner
  ```
     
     
     
