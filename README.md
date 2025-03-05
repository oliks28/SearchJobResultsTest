# Setting Up OpenJDK 17 and Maven
## Windows
### **Download and Install OpenJDK 17**
1. Go to the official OpenJDK download page: [OpenJDK 17 Download](https://jdk.java.net/17/).
2. Select the appropriate Windows version (e.g., `.zip` for the latest build).
3. Extract the downloaded `.zip` file to a directory (e.g., `C:\Program Files\OpenJDK\`).
4. Alternatively, use a package manager:
   - **Scoop**: `scoop install openjdk17`
   - **Chocolatey**: `choco install openjdk17`

### **Set Up Environment Variables**
1. Right-click on **This PC** or **My Computer**, then click **Properties**.
2. Navigate to **Advanced system settings** > **Environment Variables**.
3. Under **System variables**, click **New** and add:
   - **Variable Name:** `JAVA_HOME`
   - **Variable Value:** `C:\Program Files\OpenJDK\jdk-17` (or your extracted location).
4. Edit the `Path` variable and add:
   - `C:\Program Files\OpenJDK\jdk-17\bin`

### **Verify the Installation**
Run the following command in **Command Prompt**:
```sh
java -version
```
Expected output:
```
openjdk version "17"
OpenJDK Runtime Environment (build 17+35)
OpenJDK 64-Bit Server VM (build 17+35, mixed mode, sharing)
```

---
## macOS
### **Install OpenJDK 17**
#### **Via Homebrew (Recommended)**
```sh
brew install openjdk@17
```
#### **Manual Installation**
1. Download the latest OpenJDK 17 `.tar.gz` from [OpenJDK 17 Download](https://jdk.java.net/17/).
2. Extract it to `/Library/Java/JavaVirtualMachines`.
### **Set Up Environment Variables**
Add the following to your `~/.zshrc` or `~/.bash_profile`:
```sh
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home
export PATH=$JAVA_HOME/bin:$PATH
```
### **Verify the Installation**
```sh
java -version
```

---
## Linux
### **Debian/Ubuntu-Based Systems**
```sh
sudo apt update
sudo apt install openjdk-17-jdk
java -version
```
### **CentOS/RHEL-Based Systems**
```sh
sudo dnf install java-17-openjdk
java -version
---
# Installing Maven
## Windows
### **Download and Install Maven**
1. Go to the official [Maven Download](https://maven.apache.org/download.cgi) page.
2. Download the **Binary zip archive** (`apache-maven-x.x.x-bin.zip`).
3. Extract the `.zip` file to a directory (e.g., `C:\Program Files\Apache\Maven`).
4. Alternatively, install via Chocolatey:
   ```sh
   choco install maven
   ```
### **Set Up Environment Variables**
1. Go to **Advanced system settings** > **Environment Variables**.
2. Under **System variables**, click **New** and add:
   - **Variable Name:** `MAVEN_HOME`
   - **Variable Value:** `C:\Program Files\Apache\Maven\apache-maven-x.x.x`
3. Edit the `Path` variable and add:
   - `C:\Program Files\Apache\Maven\apache-maven-x.x.x\bin`
### **Verify the Installation**
```sh
mvn -v
```
Expected output:
```
Apache Maven 3.x.x (c) 2002-2021 The Apache Software Foundation
Maven home: C:\Program Files\Apache\Maven\apache-maven-x.x.x
Java version: 17.x.x, vendor: Oracle Corporation
```
---
## macOS
### **Install via Homebrew (Recommended)**
```sh
brew install maven
```
### **Manual Installation**
1. Download the latest Maven `.tar.gz` from [Maven Download](https://maven.apache.org/download.cgi).
2. Extract it to `/usr/local/apache-maven`.

### **Set Up Environment Variables**
Add the following to `~/.zshrc` or `~/.bash_profile`:
```sh
export MAVEN_HOME=/usr/local/apache-maven/apache-maven-x.x.x
export PATH=$MAVEN_HOME/bin:$PATH
```
### **Verify the Installation**
```sh
mvn -v
```
---
## Linux
### **Debian/Ubuntu-Based Systems**
```sh
sudo apt update
sudo apt install maven
mvn -v
```
### **CentOS/RHEL-Based Systems**
```sh
sudo dnf install maven
mvn -v
```
---
# Verification
To confirm Maven is installed correctly, run:
```sh
mvn -v
```
This command will display the Maven version along with Java installation details.
---
# Setting Up Your Project
### **Clone the Project**
```sh
git clone https://github.com/username/repository-name.git
```
### **Navigate to the Project Directory**
```sh
cd repository-name
```
### **Run Tests**
```sh
mvn clean test
```
This will initiate the automation process.
---
# Generating Reports
After execution, reports will be available at:
```
target/cucumber-reports.html
```
Open this file in a browser to view test results.

