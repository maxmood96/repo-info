## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3a63fe3d9ab8c76984d372685bf69740f4dc4b9f8b136c8144528d2a626e08a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
