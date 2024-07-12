## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:652605cceb1690bf179803d27458fe222e9862f3cd3e932e2bf41f0abb2ff47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:4e4debc76e22017cf7304ec8f937133d9f6c29e70690ef7d9a3546d5f238beec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297153261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3bafa245be7244edf9a1b99af64ed40431cde7b4defb730842408377e7190b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 12 Jul 2024 01:06:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 01:07:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Jul 2024 01:07:46 GMT
ENV DOCKER_VERSION=27.0.3
# Fri, 12 Jul 2024 01:07:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Fri, 12 Jul 2024 01:08:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:08:14 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Fri, 12 Jul 2024 01:08:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Fri, 12 Jul 2024 01:08:15 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Fri, 12 Jul 2024 01:08:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:08:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Fri, 12 Jul 2024 01:08:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Fri, 12 Jul 2024 01:08:42 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Fri, 12 Jul 2024 01:09:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434dcc61458355544a47caaa5b8bf847ece6125e09f59156e7fafc0756a3bd1a`  
		Last Modified: Fri, 12 Jul 2024 01:09:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82cab1ca448ff75ecb13363be2022e075aed9142585173a4c753ec9e55fecbf`  
		Last Modified: Fri, 12 Jul 2024 01:09:14 GMT  
		Size: 491.1 KB (491084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79090806c046c70beeca9f9d2e8568d7867fac41798d405a122cd86fdb9f408`  
		Last Modified: Fri, 12 Jul 2024 01:09:12 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d444008e5e58a7453952eab9ec85720c69dd78c9487f3e339c861cba52f4f241`  
		Last Modified: Fri, 12 Jul 2024 01:09:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853930b18086a6b53facc6dbebd0d3abc9ad2fe56050a3113cf1a40916547ead`  
		Last Modified: Fri, 12 Jul 2024 01:09:14 GMT  
		Size: 19.3 MB (19280330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecd5e7ae5eb6b9a160e1746892395c0377fa7e76ca46f5655669690869da2a0`  
		Last Modified: Fri, 12 Jul 2024 01:09:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f603cd95a827520af43f943f8a6307b9c68a8e6baecc9ea29b6222411abd9c`  
		Last Modified: Fri, 12 Jul 2024 01:09:11 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2b2c5bf51ed56893c9f993571d91b02529c95a3cf8572d2dc11a83ffdb1dda`  
		Last Modified: Fri, 12 Jul 2024 01:09:11 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca829aba4f0860779c5f58941e52537c77927b020a4825d3aaf58d1fb155d91b`  
		Last Modified: Fri, 12 Jul 2024 01:09:13 GMT  
		Size: 19.3 MB (19270563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e74043ae6d2d48589dbab20a5f93dd48887933e5d84754cdec692b7bd5275bf`  
		Last Modified: Fri, 12 Jul 2024 01:09:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6578c771f9f25e95907dbbb3fd779815eae3d4c34d05e35a609f18074abb3`  
		Last Modified: Fri, 12 Jul 2024 01:09:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c079a1439fea30469b35eff133cc042a711bc657508389ef22e7f38a905973`  
		Last Modified: Fri, 12 Jul 2024 01:09:10 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a577774727222a8f750b4504e584f985ec41eed091a5f14a801667726afc54e`  
		Last Modified: Fri, 12 Jul 2024 01:09:12 GMT  
		Size: 19.7 MB (19670301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
