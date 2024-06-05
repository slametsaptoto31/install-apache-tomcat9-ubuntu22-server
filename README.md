# Install Apache Tomcat 9 di Ubuntu 22 Server

1. #### Lakukan update
```sh
  sudo apt update
```

2. #### Install openjdk
```sh
  sudo apt install openjdk-11-jdk
```

3. #### Install tomcat 9
```sh
  sudo apt-cache search tomcat
  sudo apt install tomcat9 tomcat9-admin
```

4. #### Setting tomcat user
```sh
   nano /etc/tomcat9/tomcat-users.xml
```

5. #### Tambahkan baris perintah di akhir
```sh
   <role rolename="admin-gui"/>
   <role rolename="manager-gui"/>
   <user username="admin" password="rsgmpamc2023" roles="admin-gui,manager-gui"/>
```
