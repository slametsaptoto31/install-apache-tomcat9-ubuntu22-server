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

6. #### Setting upload max file size .war
```sh
   nano /usr/share/tomcat9-admin/manager/WEB-INF/web.xml
```

7. #### Ubah setting upload max file size, contoh max 200 mb
```sh
   <multipart-config>
      <!-- 50MB max -->
      <max-file-size>252428800</max-file-size>
      <max-request-size>252428800</max-request-size>
      <file-size-threshold>0</file-size-threshold>
  </multipart-config>
```

8. #### Restart service tomcat9
```sh
   systemctl restart tomcat9
```

9. #### Akses uji coba alamat web tomcat ke http://ipaddress:8080

10. #### Optional, setting besaran ram untuk alokasi java tomcat
```sh
   
```

