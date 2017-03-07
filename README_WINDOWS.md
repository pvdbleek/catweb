# Build Ship Run

## Demo setup

1. Install Windows Server 2016 (either local as a VM or through AWS/Azure)

2. Install Docker-EE for Windows Server

   `Install-Module -Name DockerMsftProvider -Repository PSGallery -Force`

   `Install-Package -Name docker -ProviderName DockerMsftProvider -Force`

	 `Restart-Computer -Force`

3. Install chocolatey for easy install of additional tools

   `iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex`

4. Install git

	 `choco install git -y`

## Running the demo

1. Clone the repository

	 `git clone https://github.com/pvdbleek/catweb`

2. Rename the Dockerfile for Windows

   `ren Dockerfile.win Dockerfile`

3. Build your image

   `docker build -t catweb .`

4. Run the image

   `docker run -ti -p 5000:5000 catweb`

5. Use docker inspect to find the IP of the container

6. Open Internet Explorer and point it to

  `http://xxx.xxx.xxx.xxx:5000`
