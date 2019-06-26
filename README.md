# Correlation b/w Software Metrics (Team D)

### Software Metrics Used:
1. Statement Coverage 
2. Branch Coverage
3. Mutation Score
4. Cyclomatic Complexity
5. Code Change Proneness
6. Software Defect Density

### Projects Used:
1. **Apache Commons Configurations** - [*source-code*](https://github.com/apache/commons-configuration) 
2. **Apache Commons Collections** - [*source-code*](https://github.com/apache/commons-collections)
3. **Apache Commons Math** - [*source-code*](https://github.com/apache/commons-math)
4. **Apache Commons Lang** - [*source-code*](https://github.com/apache/commons-lang)
5. **JFreeChart** - [*source-code*](https://github.com/jfree/jfreechart)

### Repository Structure
    .
    ├── CLOC Analysis                      		# Description 1
    ├── Class/Code Change Proneness        		# Description 2    
    ├── Data Analysis                      		# Description 3
    ├── Jacoco Coverage and Complexity Reports 	# Description 4
    ├── Mutation Coverage 				# Description 4
    ├── Post-Release-Defect-Density.PNG		# Description 5
    └── README.md
    
### Requirements for Running the Tools

#### 1) EclEmma (JaCoCo)
##### Prerequisites 
Make sure the Code Coverage plugin is enabled. The plugin is activated by default. If the plugin is disabled, enable it on the Plugins page as described in Managing plugins. If the plugin is disabled, the code coverage tabs will not be visible in the run/debug configuration dialogs.
##### Installation Steps:
```
Step 1. Specify how you want to process the coverage results.
Step 2. Create tests for the target code, if you are going to measure code coverage for testing.
Step 3. Configure code coverage measurement in the desired run/debug configuration.
Step 4. Run with coverage, using the dedicated command on the main menu Run | Run with Coverage, or Run with Coverage.
Step 5. Once the run with coverage has been executed, you can perform the following actions:
    - Use the various coverage suites.
    - View code coverage data.
    - Generate code coverage report.
```

#### 2) PIT (Mutation Coverage)
##### Prerequisites 
PIT requires Java 5 or above and either JUnit or TestNG to be on the classpath.  
JUnit 4.6 or above is supported (note JUnit 3 tests can be run using JUnit 4 so JUnit 3 tests are supported). JUnit 5 is not supported out of the box at this time, a plugin can be found here here.   
TestNG support in PIT is quite new. PIT is built and tested against TestNG 6.1.1, it may work with earlier and later versions but this has not yet been tested.  
Additionally PIT requires a JVM that supports XStream’s enhanced mode.  
##### Installation Steps:
Add the plugin to build/plugins in your pom.xml
```
<plugin>
    <groupId>org.pitest</groupId>
    <artifactId>pitest-maven</artifactId>
    <version>1.4.2</version>
    <dependencies>
        <dependency>
            <groupId>org.pitest</groupId>
            <artifactId>pitest-junit5-plugin</artifactId>
            <version>0.7</version>
        </dependency>
    </dependencies>
</plugin>
```
##### Run:
```mvn org.pitest:pitest-maven:mutationCoverage```

#### 3) Change Proneness Estimation (Code Change Proneness)
##### Installation Steps:
```
1. Build the project after downloading.
2. Install Java 2 Runtime Environment, Standard Edition 1.5.0
3. You can download it from http://java.com/en/index.jsp
4. Download the Probabilistic Evaluation Tool (source included)
5. Execute with double click or in console java -jar probability.jar
```
##### Usage:
```
You must first select the root of the project package. Only class files (bytecode files) are necessary for the project analysis.
You can also give as input the XML file containing the description of the static structure of the project.
```
#### 4) CLOC (Software Defect Density)
##### Installation Steps:
Depending your operating system, one of these installation methods may work for you:
```
npm install -g cloc                    # https://www.npmjs.com/package/cloc
sudo apt install cloc                  # Debian, Ubuntu
sudo yum install cloc                  # Red Hat, Fedora
sudo dnf install cloc                  # Fedora 22 or later
sudo pacman -S cloc                    # Arch
sudo emerge -av dev-util/cloc          # Gentoo https://packages.gentoo.org/packages/dev-util/cloc
sudo apk add cloc                      # Alpine Linux
sudo pkg install cloc                  # FreeBSD
sudo port install cloc                 # Mac OS X with MacPorts
brew install cloc                      # Mac OS X with Homebrew
choco install cloc                     # Windows with Chocolatey
scoop install cloc                     # Windows with Scoop
```
##### Execution Steps:
```
Step 1: Download cloc (several methods).
Step 2: Open a terminal (cmd.exe on Windows).
Step 3: Invoke cloc to count your source files, directories, archives, or git commits. The executable name differs depending on whether you use the development source version (cloc), source for a released version (cloc-1.82.pl) or a Windows executable (cloc-1.82.exe). On this page, cloc is the generic term used to refer to any of these.
```

### Team Information
| Name | Student Id | Email-Id |
|--|--|--|
| Ashish Sharma | 40050452 | ashish.sharma5293@gmail.com |
| Kritika Sharma | 40056951 | sh.kritika01@gmail.com |
| Mandeep Kaur | 40059801 | kaur.mandeep2295@gmail.com |
| Pranav Bhatia | 40056384 | bhatiapranav1996@gmail.com |
| Rodolfo Miranda | 40042111 | rodolfomotamiranda@gmail.com |
