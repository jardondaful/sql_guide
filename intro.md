# MySQL Configuration for Windows

This README provides step-by-step instructions for configuring the MySQL server on a Windows machine.

## Prerequisites

- MySQL is installed on your Windows system.

## Set the MySQL Hostname

1. **Edit the MySQL Configuration File (my.ini)**:

   - Open the MySQL configuration file `my.ini` in a text editor with administrative privileges. You can usually find this file in the MySQL installation directory, which is often located at `C:\Program Files\MySQL\MySQL Server X.X`.

2. **Locate the `bind-address` Parameter**:

   - Inside the `my.ini` file, look for the `[mysqld]` section, which contains server-related settings.

   - Add or modify the `bind-address` parameter to specify the hostname or IP address to which MySQL should bind:

     ```ini
     [mysqld]
     bind-address = your_desired_hostname_or_ip
     ```

     Replace `your_desired_hostname_or_ip` with the hostname or IP address you want to use for your MySQL server.

3. **Save the Configuration File**:

   - Save the `my.ini` file after making the changes.

4. **Restart MySQL**:

   - To apply the changes, restart the MySQL service. You can do this using either the Windows Services Manager or the Command Prompt:

     - **Using the Services Manager**:
       - Press `Win + R` to open the Run dialog.
       - Type `services.msc` and press Enter to open the Services Manager.
       - Locate the "MySQL" service, right-click on it, and select "Restart."

     - **Using the Command Prompt** (as administrator):
       - Open the Command Prompt with administrative privileges.
       - Run the following commands to stop and start the MySQL service:

         ```batch
         net stop MySQL
         net start MySQL
         ```

         Replace "MySQL" with the exact service name if it's different on your system.
