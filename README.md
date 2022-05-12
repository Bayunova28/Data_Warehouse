# Data Warehouse
* Instructor : <b>Nabilah Ayu Nindita</b> & <b>Yuma Adhli</b>
* Place : <b>Multimedia Nusantara University</b>

## Installation PDI & Launching the PDI Graphical Designer – Spoon
* Firstly, make sure your Windows Environment Variable named [JAVA_HOME](https://www.oracle.com/java/technologies/downloads/) to point to the JRE,
`JAVA_HOME =: C:\Program Files\Java\jre1.8.0_144`
* Donwload [Pentaho Data Integration](https://sourceforge.net/projects/pentaho/files/Data%20Integration/)
* Unzip the downloaded file in a folder of your choice
* Now that you've installed PDI, you're ready to start working with the data. PDI has a desktop designer and before start your spoon please execute 
the `set-pentaho-env.bat` by double-click
* Start Spoon, run `Spoon.bat` from within the PDI installed directory

## Installation Laragon & SQLyog
* Download [Laragon source code](https://sourceforge.net/projects/laragon/)
* Follow the instructions on [Installation | Laragon - portable, isolated, fast & powerful
universal development environment for PHP, Node.js, Python, Java, Go, Ruby](https://laragon.org/docs/install.html)
* Start your MySQL Virtual server
* Download [SQLyog Community Edition](https://github.com/webyog/sqlyog-community/wiki/Downloads)

## Installation Apache Tomcat
* Download [apache-tomcat-7.0.91-windows-x64.zip](https://jakarta.apache.org/site/binindex.cgi)
* Save and extract to your desktop on location of `C:\Program Files\apache-tomcat-7.0.91`
* In the Tomcat folder, open the bin folder then Click the `startup.bat` icon.
* You should see a black and white Java command window and you should not see any obvious java error messages
* Open your browser and point to `http://localhost:8080` and you will have the Tomcat welcome page

## Apache Mondrian Web Application Setup
* Download the [Mondrian package](https://sourceforge.net/projects/mondrian/files/mondrian/mondrian-3.5.0/mondrian-3.5.0.zip/download)
* Copy the `mondrian.war` file from `mondrian-3.5.0.zip\mondrian-3.5.0\lib` to the webapps folder of Tomcat when the Tomcat server is running
* After a while the server will extract / deploy the war package
* Open the queries folder from the Mondrian application `C:\apache-tomcat-6.0.16\webapps\mondrian\WEB-INF\queries`
* Edit the `mondrian.jsp` file which contains the MDX configuration and query tags for Mondrian and search for the line with the following contents:
  ```jsp
  <jp:mondrianQuery
  id="query01"
  jdbcDriver="com.mysql.jdbc.Driver"
  jdbcUrl="jdbc:mysql://localhost/foodmart?user=root&password="
  catalogUri="/WEB-INF/queries/FoodMart.xml">
  ```
