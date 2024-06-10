## Java Installation on Mac M1 Pro OS

Follow these steps to install Java on your Mac M1 Pro OS:

### Step 1: Download Java
1. Visit the official Java download page: [Oracle Java Downloads](https://www.oracle.com/in/java/technologies/downloads/).

### Step 2: Install Java
1. Open the downloaded Java installer file.
2. Follow the on-screen instructions to complete the installation process.

### Step 3: Verify Java Installation
1. Open Terminal.
2. Enter the following command to check if Java is installed:
   ```sh
   /usr/libexec/java_home -V
   ```
   This command lists all installed Java versions.

### Step 4: Set Up `JAVA_HOME` Environment Variable
1. Open Terminal.
2. Navigate to your home directory:
   ```sh
   cd ~
   ```

### Step 5: Create or Open `.zshrc` File
1. If the `.zshrc` file does not exist, create it:
   ```sh
   touch .zshrc
   ```
2. Open the `.zshrc` file using a text editor:
   ```sh
   nano .zshrc
   ```
   Or:
   ```sh
   open .zshrc
   ```

### Step 6: Add Java Environment Variables
1. In the `.zshrc` file, add the following lines, replacing `<version>` with the desired Java version (e.g., `1.8`, `17`, `22`):
   ```sh
   export JAVA_HOME=$(/usr/libexec/java_home -v <version>)
   export PATH=$JAVA_HOME/bin:$PATH
   ```
2. Save and close the file (if using `nano`, press `CTRL + X`, then `Y` to confirm, and `Enter` to save).

### Step 7: Apply the Changes
1. Load the changes to the current terminal session by running:
   ```sh
   source .zshrc
   ```

### Step 8: Verify Configuration
1. Check if the `JAVA_HOME` environment variable is set correctly:
   ```sh
   echo $JAVA_HOME
   ```
2. Check the Java version:
   ```sh
   java -version
   ```
