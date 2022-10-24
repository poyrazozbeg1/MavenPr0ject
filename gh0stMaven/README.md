A) Sıfırdan Kurulum:
---------------------------------------------------------------------
01:
C:\Users\poyraz>mvn archetype:generate -DgroupId=com.gh0st.app.App -DartifactId=gh0stMaven -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
C:\Users\poyraz>cd gh0stMaven
C:\Users\poyraz\gh0stMaven>mvn clean package
---------------------------------------------------------------------
02:
a)intelij-file open- open C:\Users\poyraz\gh0stMaven

b)pom.xml'e git

c)
plugin'lerde değişim yap:
        <plugin>
          <artifactId>maven-jar-plugin</artifactId>
          <version>3.0.2</version>
          <configuration>
            <archive>
              <manifest>
                <mainClass>com.gh0st.app.App</mainClass>
              </manifest>
            </archive>
          </configuration>
        </plugin>
d)C:\Users\poyraz\gh0stMaven>mvn clean package
---------------------------------------------------------------------
03:
a)https://mvnrepository.com/artifact/org.apache.commons/commons-lang3/3.0

b)dependencies'lerin arasına:
<dependency>
    <groupId>org.apache.commons</groupId>
    <artifactId>commons-lang3</artifactId>
    <version>3.0</version>
</dependency>

c)C:\Users\poyraz\gh0stMaven>mvn clean package
---------------------------------------------------------------------
04:
mvn package

java -cp target/gh0stMaven-1.0-SNAPSHOT.jar com.gh0st.app.App

"Hello World"
---------------------------------------------------------------------
05:
java -jar target/gh0stMaven-1.0-SNAPSHOT.jar com.gh0st.app.App

"Hello World"
---------------------------------------------------------------------
---------------------------------------------------------------------

B)Github'daki dosyalarla kurulum:
Github'da src klasörünün (içinde yalnızca main var, test yok çünkü gerekli değil anladığım kadarıyla) ve pom.xml dosyasının olması yeterli.
Terminalde "mvn clean package" işleminden sonra otomatik olarak target klasörü oluşuyor.
Ardından "java -jar target/gh0stMaven-1.0-SNAPSHOT.jar com.gh0st.app.App" yazıldığında sonuç sıfırdan kurulumla aynı oluyor. Yani;
"Hello World"