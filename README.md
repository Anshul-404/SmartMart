SmartMart Application
=====================

The SmartMart Application is a Java desktop solution designed for efficient inventory control and streamlined data management. It provides an easy-to-use interface for managing stocks, employees, and generating bills for a seamless shopping experience.

Features
--------
Manager Panel:

  * Add and manage stocks
  * Manage employees
  * View orders

Receptionist Panel:
    Billing section for handling customer purchases
    View orders processed by receptionist

Barcode Generation:
    SmartMart offers an automatic barcode generation feature for scanned products, simplifying inventory management.

Password Encryption:
    The application ensures enhanced data security by incorporating password encryption using the MD5 algorithm.

Getting Started
---------------

Prerequisites:
    Java Development Kit (JDK)
    MySQL Database

Installation:
    Clone the repository from GitHub:
    ```
    git clone https://github.com/yourusername/smartmart.git
    ```

Configuring Database
--------------------

Copy "smartmart.dmp" file to bin folder of your system's Oracle directory.
    
Use the following commands on Oracle SQL

    ```
    create user grocery identified by grocery
    grant resource,connect,dba to grocery
    ```

Use the following commands on Command Prompt (Administrator) -


    ```
    cd path/to/oracle/bin/
    imp grocery/grocery
    
    Import data only (yes/no): no > no
    
    Import file: EXPDAT.DMP > smartmart.dmp
    
    Enter insert buffer size (minimum is 8192) 30720> 30720
    
    Export file created by EXPORT:V11.02.00 via conventional path
    
    Warning: the objects were exported by GROCERY, not by you
    
    import done in WE8MSWIN1252 character set and AL16UTF16 NCHAR character set
    import server uses AL32UTF8 character set (possible charset conversion)
    List contents of import file only (yes/no): no > no
    
    Ignore create error due to object existence (yes/no): no > no
    
    Import grants (yes/no): yes > yes
    
    Import table data (yes/no): yes > yes
    
    Import entire export file (yes/no): no > yes
    ```

Manager Details:


    <details>
      <summary>Default Credentials For Manager Login</summary>
      <p>User ID : anshul@2002</p>
      <p>Password : password</p>
    </details>

To create a new manager user, first generate a MD5 hash of your password [here](https://codebeautify.org/md5-hash-generator).

Run these commands on Oracle SQL -

    ```
    connect grocery/grocery
    insert into users values ('your@userid', 'E_EMPLOYEEID' ,'YOUR_HASH', 'Manager', 'Username');
    commit;
    ```

    To Remove Default Credentials, run these commands on Oracle SQL -

    ```
    connect grocery/grocery
    delete from users where USERID = 'anshul@2002';
    commit;
    ```

Usage:
------

Run the application using the following command:

        java -jar SmartMart.jar

Generated Barcodes:
    All the generated barcodes are stored in the "Barcodes" folder within the application directory.

