# ⚙️ WSL Hacks

Este guia mostra como preparar seu ambiente WSL (Windows Subsystem for Linux) para desenvolvimento em **Python**, além de instalar ferramentas essenciais como **Java** e **Apache Spark**.

Vamos passar por:

- Escolha e instalação da distro Linux
- Configuração de rede e atualização do sistema
- Instalação do Python, Pip, venv e ferramentas úteis
- Setup de Java + Spark com variáveis de ambiente

---

## 🚀 Configurando o WSL para Projetos com Python, Java e Spark

Tenho um repositório com um script de automatização que consegue fazer a instalação e configuração do ambiente pronto para projetos de dados: [vitorluzz/wsl-for-data](https://github.com/vitorluzz/wsl-for-data)

Abaixo você terá o passo a passo para instalar o WSL para projetos de dados, porém:

### 1 - 🐧 Escolhendo e instalando uma distribuição Linux

**1.1** Para isso, vamos instalar o Debian:

```shell title='shell'
wsl --install -d Debian
```

**1.2** Acessando a distribuição instalada:

```shell title='shell'
wsl -d Debian
```

---

### 2 - 🛠️ Configurações básicas do ambiente

**2.1** Atualizando o sistema:
```shell title='shell'
sudo apt update && sudo apt full-upgrade
```

**2.2** Corrigindo o acesso à internet (DNS Fixo)
```shell title='shell'
sudo rm /etc/resolv.conf
sudo bash -c 'echo "nameserver 8.8.8.8" > /etc/resolv.conf'
sudo bash -c 'echo "[network]" > /etc/wsl.conf'
sudo bash -c 'echo "generateResolvConf = false" >> /etc/wsl.conf'
sudo chattr +i /etc/resolv.conf
```

---

### 3 - 🐍 Instalando Python e suas bibliotecas

**3.1** Instalando o Python:
```shell title='shell'
sudo apt-get install python-is-python3
```

**3.2** Instalando o Pip:
```shell title='shell'
sudo apt install python3-pip
python -m pip install --upgrade pip
```

**3.3** Instalando o venv:
```shell title='shell'
sudo apt install python3.11-venv
```

**3.4** Instalando ferramentas úteis (wget, curl, git e unzip):
```shell title='shell'
sudo apt install wget curl git unzip
```

**INSTALANDO O JAVA ☕**
**3.5** Baixar Java - JDK 21 (necessário para o Spark):
```shell title='shell'
mkdir -p ~/java && cd ~/java
wget https://download.java.net/java/GA/jdk21.0.2/f2283984656d49d69e91c558476027ac/13/GPL/openjdk-21.0.2_linux-x64_bin.tar.gz
```

**3.6** Descompactando o mesmo:
```shell title='shell'
tar -xvf openjdk-21.0.2_linux-x64_bin.tar.gz
rm openjdk-21.0.2_linux-x64_bin.tar.gz
```

**3.7** Adicionar as variáveis de ambiente do Java:
```shell title='shell'
nano ~/.bashrc
```

**3.8** Coloque no final as variáveis de ambiente:
```shell title='shell'
# JAVA
export JAVA_HOME=~/java/jdk-21.0.2
export PATH=$PATH:$JAVA_HOME/bin
```

**3.9** Salve as alterações: `CTRL + O` + `ENTER` + `CTRL + X`
 
---

**Instalando o Spark ⚡**
**3.10** Baixar o Spark:
```shell title='shell'
mkdir -p ~/apache && cd ~/apache
wget https://dlcdn.apache.org/spark/spark-3.5.5/spark-3.5.5-bin-hadoop3.tgz
```


**3.11** Descompactar o mesmo:
```shell title='shell'
tar -xvf spark-3.5.5-bin-hadoop3.tgz
rm spark-3.5.5-bin-hadoop3.tgz
mv spark-3.5.5-bin-hadoop3 spark-3.5.5
```


**3.12** Entre em seu bashrc:
```shell title='shell'
nano ~/.bashrc
```

**3.13** Adicione as variáveis de ambiente necessárias:
```shell title='shell'
# SPARK
export SPARK_HOME=~/apache/spark-3.5.5
export SPARK_LOCAL_IP=127.0.0.1
export HADOOP_HOME=$SPARK_HOME
export PYTHONPATH=$SPARK_HOME/python
export PATH=$PATH:$SPARK_HOME/bin
```

**3.14** Salve as alterações: `CTRL + O` + `ENTER` + `CTRL + X`

**3.15** Atualize o bashcr:
```shell title='shell'
source ~/.bashrc
```

> Pronto, criamos um ambiente preparado para utilizar o 