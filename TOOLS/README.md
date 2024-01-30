#  Integrated Development Environment (IDE)<br> Programming Java

<p align="center"> 
<img src="/TOOLS/IMG/IDE-Java.png" width="400" align="center">
</p 

<br>

## Concept
**Software for Java**
 
**Netbeans IDE**<br>
Windows<br>
* [Oracle Java ](https://www.oracle.com/br/java/)
* [Java SE Development Kit 21 ](https://www.oracle.com/br/java/technologies/downloads/)
* [Netbeans org ](https://netbeans.apache.org/)
* [Netbeans IDE](https://netbeans.apache.org/front/main/download/nb20/)


**Java SE Development Kit 21**<br>
Ubuntu<br>

1. Verificar se o Java esta instalado<br>
```
java --version
```

2. Download 
* [Java SE Development Kit 21](https://www.oracle.com/br/java/technologies/downloads/) for Windows, Linux or Mac OS.<br>
Neste caso como já tinha instalado via .deb tive que fazer todas as configurações abaixo, porém recomendo fazer 
o processo 
* [Documentação Instalação ](https://docs.oracle.com/en/java/javase/19/install/overview-jdk-installation.html)

3. Instalar o Java<br>
https://help.ubuntu.com/kubuntu/desktopguide/C/manual-install.html<br>
```
sudo dpkg -i package_file.deb
```

4. Instalar o Java, este momento será apresentado o seguinte erro:<br>
dpkg: error processing package jdk-19 (--install):<br>
 dependency problems - leaving unconfigured<br>
Errors were encountered while processing:<br>
 jdk-19<br>
* [Ask](https://askubuntu.com/questions/1397989/java-jdk-wont-install)

5. Fazer atualização<br>
```
sudo apt update
apt list --upgradable
apt install -f
```

6. Instalar novamente o Java<br>
https://help.ubuntu.com/kubuntu/desktopguide/C/manual-install.html<br>
```
sudo dpkg -i package_file.deb
```

7. Mesmo já tendo feito o processo via .deb é nessário realizar os seguintes passos: <br>
https://www.edivaldobrito.com.br/como-instalar-o-oracle-java-19-no-ubuntu-debian-e-derivados/<br>
Realizei correções nos comandos devido a  erros de digitação <br>
```
sudo -s
echo "JAVA_HOME=/usr/lib/jvm/jdk-19" >> /etc/profile
echo "PATH=$PATH:$HOME/bin:$JAVA_HOME/bin" >> /etc/profile
echo "export JAVA_HOME" >> /etc/profile
echo "export PATH" >> /etc/profile
update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-19/bin/java 1
update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-19/bin/javac 1
update-alternatives --install /usr/bin/jar jar /usr/lib/jvm/jdk-19/bin/jar 1
update-alternatives --set java /usr/lib/jvm/jdk-19/bin/java
update-alternatives --set javac /usr/lib/jvm/jdk-19/bin/javac
update-alternatives --set jar /usr/lib/jvm/jdk-19/bin/jar
. /etc/profile 
```

8. Instalação realizada com sucesso<br>
```
java --version
javac --version
jar --version
```

**Netbeans IDE**<br>
Ubuntu<br>
1. Download Netbeans<br>
* [Netbeans IDE](https://netbeans.apache.org/download/nb16/) for Windows, Linux or Mac OS.

2. Install Netbeans<br>
```
sudo dpkg -i apache-netbeans_16-1_all.deb
```

**Visual Studio Code IDE**<br>
Online<br>
* [Visual Studio Code Online](https://vscode.dev/)<br>
Após fazer Sign in no github.com, no diretório que deseja realizar as alteração pressione "." isso encaminha você ao VScode - Online

**Visual Studio Code IDE**<br>
Windows<br>

* [Documentação e Download ](https://code.visualstudio.com/docs/?dv=win)
* [Documentação ](https://code.visualstudio.com/docs/java/java-tutorial)
* [Estensão Java for Visual Studio Code ](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)
<br>
Abrir o VScode, clicar no ícone "extenções"<br> 
<p align="center"> 
<img src="/TOOLS/IMG/001-Extensions.jpeg" width="400" align="center">
</p 
<br>
Digitar no campo "pesquisa de extenções" "Java" <br>
<p align="center"> 
<img src="/TOOLS/IMG/002-Extensions.jpeg" width="400" align="center">
</p 
<br>
<p align="center"> 
<img src="/TOOLS/IMG/003-ExtensionsJava.jpeg" width="400" align="center">
</p 
<br>
Instalar o Extension Pack for Java<br>
Conforme apresentado abaixo seguir o passo a passo <br>
<p align="center"> 
<img src="/TOOLS/IMG/004-ExtensionsJavaInstall.jpeg" width="400" align="center">
</p 
<br>
<p align="center"> 
<img src="/TOOLS/IMG/005-ExtensionsJavaInstall.jpeg" width="400" align="center">
</p 
<br>


**Visual Studio Code IDE**<br>
Ubuntu <br>
1. Download VScode<br>
* [Visual Studio Code IDE](https://code.visualstudio.com) for Windows, Linux or Mac OS.
2. Instalar VScode<br>
https://help.ubuntu.com/kubuntu/desktopguide/C/manual-install.html<br>
```
sudo dpkg -i package_file.deb
```
3. Instalar a extesão Extension Pack for Java no VScode<br>

4. Instalação realizada com sucesso<br>
```
java --version
javac --version
jar --version
```

## Software
* [Java SE Development Kit 21.0.2 ](https://www.oracle.com/java/technologies/downloads/) for Windows, Linux or Mac OS.
* [Netbeans IDE](https://netbeans.apache.org/front/main/download/nb20/) for Windows, Linux or Mac OS.
* [Visual Studio Code IDE](https://code.visualstudio.com) for Windows, Linux or Mac OS.
## Extension for Visual Studio Code :

EMMET (extensão) - Produtividade 
* [EMMET](https://docs.emmet.io/cheat-sheet/)
    
Remote (extensão) - SSH
* [Remote](https://code.visualstudio.com/docs/remote/ssh-tutorial)

Code Runner (extensão) - .run
* [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
