# Building-a-Java-Project-with-Nexus
java-maven-tomcat-nexus
### This project demonstrates the complete CI/CD lifecycle of a Java Web Calculator Application, built using Maven, versioned and deployed through Sonatype Nexus, and hosted on Apache Tomcat servers across multiple environments using Amazon EC2 (IaaS).


### Architecture Overview

By the end of this guide, you'll have a system where you:

Build Server: Maven + Java + Git (Builds WAR files)

Nexus Server: Sonatype Nexus (Artifact Repository)

Pull those artifacts to deploy across Tomcat servers.

Deploy Server: Apache Tomcat (Runs the Java Web App)

Pull those artifacts to deploy across Tomcat servers.

Track and deploy application versions (v0.0.1, v0.0.2, v0.0.3).

Cloud Infrastructure: AWS EC2 (Ubuntu instances)



Step-by-Step Pipeline Overview

 1. Launch and Prepare Build Server (EC2)

Launch an Ubuntu EC2 instance (Build Server).


<img width="1602" height="386" alt="Image" src="https://github.com/user-attachments/assets/9f8e3a6d-f3bb-4921-ade8-dc4cdc004f4c" />

3. Launch and Setup Nexus Repository (EC2)

Launch another Ubuntu EC2 instance (Nexus Server).

### Install Java and Nexus:

<img width="1214" height="304" alt="Image" src="https://github.com/user-attachments/assets/0bd9dc43-1468-46b6-8574-dd219971ff99" />

<img width="1214" height="304" alt="Image" src="https://github.com/user-attachments/assets/9a3ddddf-b164-4615-a715-b545c482e987" />


### update using sudo apt -y update.

<img width="911" height="95" alt="Image" src="https://github.com/user-attachments/assets/498f4de2-4b05-4616-ab0b-574fc5dd9c55" />

### Install java
<img width="701" height="116" alt="Image" src="https://github.com/user-attachments/assets/750ec10a-bf85-40a2-8f56-2b67fe2793e0" />

### Install maven

<img width="916" height="108" alt="Image" src="https://github.com/user-attachments/assets/f6173475-d448-491e-98b4-fd66139d4e74" />

### git clone

<img width="1067" height="71" alt="Image" src="https://github.com/user-attachments/assets/99def87d-9d07-4a40-880e-17e8eae914ab" />

### mvn validate and mvn package 

<img width="870" height="479" alt="Image" src="https://github.com/user-attachments/assets/f5dd0966-14aa-4e89-9898-d20488591646" />


<img width="776" height="109" alt="Image" src="https://github.com/user-attachments/assets/e972c3ab-6914-428e-8fe5-8b27dd7be593" />

### got a war file

<img width="1894" height="182" alt="Image" src="https://github.com/user-attachments/assets/cda9eab6-bf95-4863-979c-e1f484fe6b27" />

### Setup Apache Tomcat on Deploy Server

A third EC2 instance was launched for deployment.

Tomcat was installed by downloading the tar file from the browser and extracting it.

Configuration files tomcat-users.xml and context.xml were updated to enable deployment manager access.

Update the server

<img width="707" height="88" alt="Image" src="https://github.com/user-attachments/assets/f5f4397e-5856-4087-9491-a09cab2397d8" />

### Install java

<img width="1067" height="134" alt="Image" src="https://github.com/user-attachments/assets/f24a23e1-b95b-4320-980e-c78d4f754836" />

<img width="1012" height="176" alt="Image" src="https://github.com/user-attachments/assets/c1494d21-a8ab-462c-adee-8ed9f8e2636d" />


### Install tomcat using wget and download tar file  from browser

<img width="912" height="612" alt="Image" src="https://github.com/user-attachments/assets/a99ebfdd-bc90-452a-ab05-05714d7ab932" />

<img width="1323" height="77" alt="Image" src="https://github.com/user-attachments/assets/3c298924-c764-45b1-9ef0-df10e9dbc2db" />

### extract the file 

<img width="904" height="87" alt="Image" src="https://github.com/user-attachments/assets/f991c5f5-95df-4f4b-88f2-4211eae2b5d1" />

### edit context.xml and tomcatusers.xml

<img width="1243" height="177" alt="Image" src="https://github.com/user-attachments/assets/ba66967d-79b5-49fd-b684-1d20fe01f453" />

<img width="1331" height="691" alt="Image" src="https://github.com/user-attachments/assets/22920b67-92fb-454e-a6f5-a59d1daf475d" />

<img width="1247" height="140" alt="Image" src="https://github.com/user-attachments/assets/60e4343d-2534-45fd-b4c1-a5a9efb66e61" />

<img width="1162" height="762" alt="Image" src="https://github.com/user-attachments/assets/56a1846d-3202-40d5-b856-eacee60fed0b" />

<img width="1622" height="373" alt="Image" src="https://github.com/user-attachments/assets/8c0b712e-0d6e-4456-a493-27d2dd1eea33" />

### start tomcat

<img width="1814" height="192" alt="Image" src="https://github.com/user-attachments/assets/1bfbd384-7239-4cd5-8222-99694996d011" />

### check in the browser

<img width="1600" height="836" alt="Image" src="https://github.com/user-attachments/assets/35b149b6-c6a4-4872-92cc-7a50f9ca8add" />

### give the details and sign in

<img width="1358" height="489" alt="Image" src="https://github.com/user-attachments/assets/4cd5f28e-dcfb-4d33-81c2-6623f7fdbdbe" />

<img width="1635" height="918" alt="Image" src="https://github.com/user-attachments/assets/f495ee18-837a-4dfe-9c2b-e25966edcd8a" />


### log in to nexus server and update

<img width="725" height="126" alt="Image" src="https://github.com/user-attachments/assets/7b29fb48-6a77-4848-a1fd-63380802d8c8" />

### install java

<img width="864" height="160" alt="Image" src="https://github.com/user-attachments/assets/8f8369dd-4048-466a-87bd-1fcb43be2f06" />

### install nexus from browser using wget

<img width="1334" height="92" alt="Image" src="https://github.com/user-attachments/assets/ce3416fe-4d95-4e76-bbeb-21ff1ab89ee2" />


<img width="1698" height="699" alt="Image" src="https://github.com/user-attachments/assets/223bd13e-a471-424d-a6e9-bbe187a9bca5" />


### extract tar file

<img width="824" height="109" alt="Image" src="https://github.com/user-attachments/assets/b79395e9-81fc-41f0-9d41-3fbb0ff55a97" />

### start nexus

<img width="892" height="189" alt="Image" src="https://github.com/user-attachments/assets/4c219945-ced9-463f-9b9a-455087e2a835" />


### install net tools to check nexus status with sudo netstat -ntpl

<img width="870" height="79" alt="Image" src="https://github.com/user-attachments/assets/24c01b2e-759e-4304-905f-6b034c50094b" />

<img width="1551" height="436" alt="Image" src="https://github.com/user-attachments/assets/49dea59d-78d4-4d50-94e9-400057dbeab4" />

<img width="1050" height="196" alt="Image" src="https://github.com/user-attachments/assets/47107882-46db-4ef4-b9f5-3991b3d967a6" />


### go to browser and check with nexus public id u will see sonatype page

<img width="1887" height="908" alt="Image" src="https://github.com/user-attachments/assets/f73e29b0-f2f2-444e-b7a5-62afdfddaa91" />


### log in and change password

<img width="1027" height="642" alt="Image" src="https://github.com/user-attachments/assets/38b7b277-9ced-4151-b40e-235c0c721a9a" />


<img width="1005" height="563" alt="Image" src="https://github.com/user-attachments/assets/07f26c6e-02ba-480a-bf3b-01be29022246" />


<img width="1471" height="658" alt="Image" src="https://github.com/user-attachments/assets/395645c7-8bb8-4a44-bed7-bb5c26b0b426" />


<img width="868" height="584" alt="Image" src="https://github.com/user-attachments/assets/bb2cf4d4-2104-40fd-bd1f-2496d18d2784" />


### create a repo after logging in into sonatype 

<img width="635" height="214" alt="Image" src="https://github.com/user-attachments/assets/36691877-addf-4dfa-a599-e8b371c9f4a3" />

<img width="1516" height="895" alt="Image" src="https://github.com/user-attachments/assets/5ed259aa-eded-458b-b071-a223ccac6327" />

<img width="1880" height="777" alt="Image" src="https://github.com/user-attachments/assets/13d72578-083e-438a-a087-bf5011ad5f71" />


### go to build server and edit pom.xml file

<img width="748" height="213" alt="Image" src="https://github.com/user-attachments/assets/ca81bcaa-3ec0-48ae-ac8b-f1ccd16d21f4" />

<img width="1053" height="646" alt="Image" src="https://github.com/user-attachments/assets/7bfc40ab-7eba-4445-b327-92a3c37587af" />

<img width="812" height="89" alt="Image" src="https://github.com/user-attachments/assets/8dae52a3-323f-4583-a8d1-2bf870d6fc63" />

### run maven clean

<img width="907" height="663" alt="Image" src="https://github.com/user-attachments/assets/16eb3119-1620-4a83-a583-8f9da3ab3b9a" />

<img width="659" height="60" alt="Image" src="https://github.com/user-attachments/assets/18dcf5e5-65d7-4729-be71-99aeb6d22ee6" />

### copy index.jsp file to temp and edit index.jsp file

<img width="981" height="176" alt="Image" src="https://github.com/user-attachments/assets/99b46c29-1865-479a-8b55-4f1f1ca00e02" />

<img width="1356" height="622" alt="Image" src="https://github.com/user-attachments/assets/ab2e9b3c-5aeb-42a8-8429-70c239eebad2" />

<img width="957" height="179" alt="Image" src="https://github.com/user-attachments/assets/6aa75ee0-19fe-49cf-949b-3a817c290a79" />


### run mvn validate,mvn package,mvn deploy

<img width="748" height="115" alt="Image" src="https://github.com/user-attachments/assets/b53a34e1-a6d8-416e-a2e5-85c755c26f75" />

<img width="814" height="332" alt="Image" src="https://github.com/user-attachments/assets/0f5d0e91-89d8-437e-93b1-8e5bf827ff89" />

<img width="976" height="399" alt="Image" src="https://github.com/user-attachments/assets/068f92a0-d66d-45bb-b2f2-f6308cd2c69a" />

<img width="1128" height="333" alt="Image" src="https://github.com/user-attachments/assets/ea8dfc98-9505-45d6-a89c-66ebf3649197" />


### go to browser sonatype and check for .war and copy the link address of the war file artifact

<img width="524" height="497" alt="Image" src="https://github.com/user-attachments/assets/2b52e755-1f4c-412c-a0e0-6e2db20e223e" />

<img width="1622" height="610" alt="Image" src="https://github.com/user-attachments/assets/529a5b9b-e92b-41a6-b84f-25b085a9a35b" />

<img width="1298" height="763" alt="Image" src="https://github.com/user-attachments/assets/e2ed7392-7773-47c0-81cb-6a3eb01d3b64" />


### go to deploy server and download the url using wget and u will see .war file

<img width="1101" height="116" alt="Image" src="https://github.com/user-attachments/assets/36f76369-8f47-40c2-9c7d-5480f9f90a5c" />

<img width="1919" height="145" alt="Image" src="https://github.com/user-attachments/assets/76979359-02aa-4a76-801d-aad961ca7dbf" />

<img width="1829" height="209" alt="Image" src="https://github.com/user-attachments/assets/4975a7b4-1bb8-4007-83b7-f89eb6ba90b4" />


###Deploy Version 0.0.1

Initial deployment included a basic calculator with addition functionality.

WAR file uploaded from Nexus and deployed to Tomcat.

Web application was successfully accessed in the browser.

###  go to tomcat server and refresh u will get the java cal page

<img width="731" height="293" alt="Image" src="https://github.com/user-attachments/assets/6e4ea353-5350-43dc-a53a-66b9d04d9b69" />

<img width="1885" height="786" alt="Image" src="https://github.com/user-attachments/assets/4fb9684d-d55a-4957-b242-e35cc48ddf16" />



### now version 0.0.2

### go to build server and cp index.jsp file from temp to home

<img width="957" height="125" alt="Image" src="https://github.com/user-attachments/assets/784ae600-0f0f-4776-bbf9-687b75851dce" />

### edit index.jsp file add substraction in script

<img width="785" height="636" alt="Image" src="https://github.com/user-attachments/assets/cbeb7977-fa16-40aa-9bb4-ba9008aebb3f" />


### run maven clean

<img width="1041" height="427" alt="Image" src="https://github.com/user-attachments/assets/efe3e09f-d529-488b-b6f1-3baf44562069" />

### edit pom.xml change version to 0.0.2

<img width="677" height="93" alt="Image" src="https://github.com/user-attachments/assets/5b004456-2ff6-4129-a001-ada3a99ea66d" />

<img width="673" height="340" alt="Image" src="https://github.com/user-attachments/assets/0b973817-c7a8-4cd7-bc0b-bf3b9c906e47" />


### run mavn package and maven deploy

<img width="669" height="74" alt="Image" src="https://github.com/user-attachments/assets/71acc4a5-f0fb-43f1-aaa1-85d88ccd355f" />

<img width="948" height="393" alt="Image" src="https://github.com/user-attachments/assets/46c69992-8b11-498c-924f-3866db966ac1" />

<img width="651" height="47" alt="Image" src="https://github.com/user-attachments/assets/3d9ab682-4147-4d0d-8d04-ddc020b86054" />

<img width="1361" height="364" alt="Image" src="https://github.com/user-attachments/assets/ffb99397-84cd-4da9-a8b7-6d23ee9ca5c8" />


### Update to Version 0.0.2 - Subtraction Feature

The calculator app was updated to include subtraction.

index.jsp was modified.

Version bumped in pom.xml.

WAR file deployed to Nexus and pulled by deploy server

### now go to browser and check or refresh the sonatype page u will see version 2 add and sub folder and war file

<img width="918" height="726" alt="Image" src="https://github.com/user-attachments/assets/cb9ea3af-787d-446e-b242-c3412b8398ae" />

### now cpoy that link address and download it in deploy server u will see two war files

<img width="746" height="665" alt="Image" src="https://github.com/user-attachments/assets/1eff0832-e603-4a1e-86c3-6aabaea7f464" />

<img width="1911" height="152" alt="Image" src="https://github.com/user-attachments/assets/9274feda-02ff-4e66-85fd-67c09570d312" />

<img width="1653" height="89" alt="Image" src="https://github.com/user-attachments/assets/6c31675c-048b-4441-ad01-03c58c6fe817" />


### now go check tomcat browser ull find a version 2 webapp

<img width="1895" height="361" alt="Image" src="https://github.com/user-attachments/assets/4430e604-b21c-4138-925c-28967771ba2f" />

### go to webapps 0.0.2 version ull seed addition and substraction calci page

<img width="846" height="426" alt="Image" src="https://github.com/user-attachments/assets/8af7debd-5767-46ce-8a2c-7ffa218b1875" />

### Update to Version 0.0.3 - Multiplication Feature

Calculator app enhanced with multiplication support.

WAR artifact uploaded to Nexus with version 0.0.3.

Three distinct versions now visible in Nexus and deployed in Tomcat.

### now go to build server edit pom.xml file edit to version 0.0.3

<img width="962" height="161" alt="Image" src="https://github.com/user-attachments/assets/6c7b4c1a-d42a-4e92-aaa4-92fed3d76402" />

<img width="752" height="268" alt="Image" src="https://github.com/user-attachments/assets/2fe58711-dec6-4efb-99c0-329b8d6baa83" />

### now run maven clean ,package and deploy

<img width="755" height="400" alt="Image" src="https://github.com/user-attachments/assets/9a19564a-ff54-4322-aeac-e887d0408ffd" />

<img width="857" height="386" alt="Image" src="https://github.com/user-attachments/assets/304c76da-24d0-47b8-8674-c6736fe17d42" />

<img width="1115" height="420" alt="Image" src="https://github.com/user-attachments/assets/c09af8c6-bc6e-4ef1-8214-461c614f8ef2" />

### go to sonatype browser and refresh u will see the third version 0.0.3 version

<img width="736" height="393" alt="Image" src="https://github.com/user-attachments/assets/a7e7cddc-6611-4008-87b1-a0041f19d873" />

<img width="1641" height="721" alt="Image" src="https://github.com/user-attachments/assets/bbc8decd-d52f-45e7-b0f6-209aefbc77c4" />

### copy the link address and download it in deploy server using wget and hard core the username and password in it

<img width="1907" height="104" alt="Image" src="https://github.com/user-attachments/assets/0e05c7c2-c2d4-4cd5-bb8b-1c86449bd471" />

### now list you will see three versions artifacts

<img width="1455" height="137" alt="Image" src="https://github.com/user-attachments/assets/f6d0fac5-47b7-416f-8d10-351552512b5f" />

### go to tomcat browser u can refresh and see three version folders and go to third version webapp u will see the calci page with addition ,subtraction and multiplication features.

<img width="1752" height="335" alt="Image" src="https://github.com/user-attachments/assets/c065b5b5-323d-4f4b-b3af-fd4d123c8dd0" />

<img width="582" height="314" alt="Image" src="https://github.com/user-attachments/assets/178c9a56-68ad-408b-a8b4-ffd4dc42bb31" />

<img width="567" height="628" alt="Image" src="https://github.com/user-attachments/assets/a7ab1c22-0ba5-43e4-bdcc-e4cbfa8bba8b" />


### Final Web Calculator View (v0.0.3)

All three versions are hosted in Tomcat as separate webapps.

Version 0.0.3 supports:

✅ Addition

✅ Subtraction

✅ Multiplication

☁️ Nexus stores and versions artifacts.

🖥️ Tomcat hosts multiple live versions.

🔄 Fully repeatable CI/CD cycle via Maven builds and Nexus deploys.

📁 Web UI evolves incrementally with each release.
 















