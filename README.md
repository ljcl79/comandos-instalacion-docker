#Comandos para instalar la WSL

Verificación de disponibilidad de WSL

`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`

Verificación del sistema de imagenes virtuales
`dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`

Instalar la WSL 2
`wsl --install`

Verificar la instalación de la WSL 2
`wsl --list --verbose`

#Comando para instalar Docker

Actualización de paquetes
```
sudo apt update
sudo apt upgrade -y
```

Instalar dependencias necesarias
`sudo apt install -y apt-transport-https ca-certificates curl software-properties-common`

Agregar la clave GPG de Docker
`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`

Agregar el repositorio oficial de Docker
`echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`

Instalar Docker
```
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io
```

Verificar versión de Docker
`docker --version`

Ejecutar el  hello world
`sudo docker run hello-world`
sudo apt update
sudo apt upgrade -y
