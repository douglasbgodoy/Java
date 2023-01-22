#  Integrated Development Environment (IDE)<br> Programming Java

<p align="center"> 
<img src="/TOOLS/IMG/IDE-C.png" width="400" align="center">
</p 

<br>

## Concept
**Software for Java**
 
**Netbeans IDE**<br>
Windows<br>
* [Oracle Java ](https://www.oracle.com/br/java/)
* [Java SE Development Kit 19.0.2 ](https://www.oracle.com/br/java/technologies/downloads/)
* [Netbeans org ](https://netbeans.apache.org/)
* [Netbeans IDE](https://netbeans.apache.org/download/nb16/)


**Netbeans IDE**<br>
Ubuntu<br>

1. Verificar se o Java esta instalado<br>
java --version

2. Download 
* [Java SE Development Kit 19.0.2](https://www.oracle.com/br/java/technologies/downloads/) for Windows, Linux or Mac OS.<br>
Neste caso como já tinha instalado via .deb tive que fazer todas as configurações abaixo, porém recomendo fazer 
o processo 
* [Documentação Instalação ](https://docs.oracle.com/en/java/javase/19/install/overview-jdk-installation.html)

3. Instalar o Java<br>
https://help.ubuntu.com/kubuntu/desktopguide/C/manual-install.html<br>
sudo dpkg -i package_file.deb

4. Instalar o Java, este momento será apresentado o seguinte erro:<br>
dpkg: error processing package jdk-19 (--install):<br>
 dependency problems - leaving unconfigured<br>
Errors were encountered while processing:<br>
 jdk-19<br>
* [Ask](https://askubuntu.com/questions/1397989/java-jdk-wont-install)

5. Fazer atualização<br>
sudo apt update<br>
apt list --upgradable<br>
apt install -f<br>

6. Instalar novamente o Java<br>
https://help.ubuntu.com/kubuntu/desktopguide/C/manual-install.html<br>
sudo dpkg -i package_file.deb

7. Mesmo já tendo feito o processo via .deb é nessário realizar os seguintes passos: <br>
https://www.edivaldobrito.com.br/como-instalar-o-oracle-java-19-no-ubuntu-debian-e-derivados/<br>
Realizei correções nos comandos devido a  erros de digitação <br>
sudo -s<br>
echo "JAVA_HOME=/usr/lib/jvm/jdk-19" >> /etc/profile<br>
echo "PATH=$PATH:$HOME/bin:$JAVA_HOME/bin" >> /etc/profile<br>
echo "export JAVA_HOME" >> /etc/profile<br>
echo "export PATH" >> /etc/profile<br>
update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-19/bin/java 1<br>
update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-19/bin/javac 1<br>
update-alternatives --install /usr/bin/jar jar /usr/lib/jvm/jdk-19/bin/jar 1<br>
update-alternatives --set java /usr/lib/jvm/jdk-19/bin/java<br>
update-alternatives --set javac /usr/lib/jvm/jdk-19/bin/javac<br>
update-alternatives --set jar /usr/lib/jvm/jdk-19/bin/jar<br>
. /etc/profile<br>

8. Instalação realizada com sucesso<br>
java --version<br>
javac --version<br>
jar --version<br>

9. Download Netbeans<br>
* [Netbeans IDE](https://netbeans.apache.org/download/nb16/) for Windows, Linux or Mac OS.

10. Install Netbeans<br>
sudo dpkg -i apache-netbeans_16-1_all.deb

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
Crie um arquivo "primeiro.cpp"<br> 
Neste momento temos a imagem pedindo para instalar a extensão<br>
<p align="center"> 
<img src="/TOOLS/IMG/001-AutoInstallCpp.png" width="400" align="center">
</p 
<br>
Uma outra forma de instalar a extensão é pesquisar a C/C++ Extension Pack <br>
<p align="center"> 
<img src="/TOOLS/IMG/002-ExtensionPackCpp.png" width="400" align="center">
</p 
<br>
Também é possível instalar somente esta extensão, porém recomendo instalar as duas <br>
<p align="center"> 
<img src="/TOOLS/IMG/003-ExtensionCpp.png" width="400" align="center">
</p 
<br>
Agora com as extensões instaladas é necessário uma configuração para que seja possivel compilar projetos em C++<br>
Para quem tem o CodeBlocks instalado realizar o passo a passo  abaixo ou <a href="https://code.visualstudio.com/docs/cpp/config-mingw"> Documentação Using GCC with MinGW</a>.
<br>
<br>


Add the path to your Mingw-w64 bin folder to the Windows PATH environment variable by using the following steps:

1. In the Windows search bar, type 'settings' to open your Windows Settings.<br>
2. Search for Edit environment variables for your account.<br>
3. Choose the Path variable in your User variables and then select Edit.<br>
4. Select New and add the Mingw-w64 destination folder path to the system path. The exact path depends on which version of Mingw-w64 you have installed and where you installed it. If you used the settings above to install Mingw-w64, then add this to the path: C:\Program Files\CodeBlocks\MinGW\bin. <br>
5. Select OK to save the updated PATH. You will need to reopen any console windows for the new PATH location to be available.
6. Reboot or Sign out  <br>
**Check your MinGW installation**<br>
To check that your Mingw-w64 tools are correctly installed and available, open a new Command Prompt and type: <br>
gcc --version <br>
g++ --version <br>
gdb --version 

**Visual Studio Code IDE**<br>
Ubuntu <br>
1. Download VScode<br>
* [Visual Studio Code IDE](https://code.visualstudio.com) for Windows, Linux or Mac OS.
2. Instalar VScode<br>
https://help.ubuntu.com/kubuntu/desktopguide/C/manual-install.html<br>
sudo dpkg -i package_file.deb<br>

3. Instalar a extesão C/C++ Extension Pack no VScode<br>
4. Verificar se o gcc e g++ esta instalado <br>
gcc --version<br>
g++ --version<br>

5. Instalar gcc e g++ <br>
sudo apt install gcc<br>
Erro<br>
sudo apt install g++
Erro<br>

6. Fazer atualização <br>
sudo apt update<br>
apt list --upgradable<br>

7. Tentar instalar novamente gcc e g++<br>
sudo apt install gcc<br>
sudo apt install g++<br>

8. Instalação com sucesso <br>
gcc --version<br>
g++ --version<br>

## Software
* [Java SE Development Kit 19.0.2](https://www.oracle.com/br/java/technologies/downloads/) for Windows, Linux or Mac OS.
* [Netbeans IDE](https://netbeans.apache.org/download/nb16/) for Windows, Linux or Mac OS.
* [Visual Studio Code IDE](https://code.visualstudio.com) for Windows, Linux or Mac OS.
## Extension for Visual Studio Code :

EMMET (extensão) - Produtividade 
* [EMMET](https://docs.emmet.io/cheat-sheet/)
    
Remote (extensão) - SSH
* [Remote](https://code.visualstudio.com/docs/remote/ssh-tutorial)
