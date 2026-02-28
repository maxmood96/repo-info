## `docker:rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:940867ea949ae85fe99a4349e71f115ab66bca9c467a3faf8a43f4333af2ff8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `docker:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:7c7f339540d7e29e06a458d812201e9333cc2316c16b2088d5440149ef3fe4fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2025793169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26fbb1fb3d873cbcf61952f292fbc38424074fe28c8000934d17019a9b0bcda`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Sat, 28 Feb 2026 00:42:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:44:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_VERSION=29.3.0-rc.1
# Sat, 28 Feb 2026 00:44:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.3.0-rc.1.zip
# Sat, 28 Feb 2026 00:44:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:23 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:44:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:44:24 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:44:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:44:34 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:44:35 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:44:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec252a864940fb49290875abbffaaf7d9f3559d54222c34e75a6ed8b36b88854`  
		Last Modified: Sat, 28 Feb 2026 00:44:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edfda47b67392bfa7e4b15a5d299940cdb2eb958222ac589f180265fa1dfb44`  
		Last Modified: Sat, 28 Feb 2026 00:44:50 GMT  
		Size: 369.3 KB (369251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2074bb3dd4ed2d8bd7c5273b6c7cc45bd4176b23c71d5f26ee6841a3d524efb9`  
		Last Modified: Sat, 28 Feb 2026 00:44:49 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8205f5135e38d345f1a5c8ce0c813bca0ce906c93c2b907c231bfb572c811e8`  
		Last Modified: Sat, 28 Feb 2026 00:44:49 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b86ad957e9fb1572f98c74127154f97b7be19141fba906d4220a193b9d31c98`  
		Last Modified: Sat, 28 Feb 2026 00:44:51 GMT  
		Size: 19.6 MB (19591395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb9bff6f4d98053dd730983b39be8c71079e59b0335aa6921383fded10a1d8`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2654d3ddc8fd35a983aec9af382a61f3893c5c8986870d5d9c14106193e66eed`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05f49829bb347064a23a6a317206492ceea2d2bf41bd80bf68eed94259f5dac`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd79727c08ab69b299365c43d0fd701dd9948a2fd297d7200304e4f000ad8416`  
		Last Modified: Sat, 28 Feb 2026 00:44:50 GMT  
		Size: 29.4 MB (29419738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e37306479a92abeda8b061d94bacefc4a0b869057f768287d8180b558f683a`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34bd1976dc6fe239696ac433af4d2644e1a6e90e8110f0869084b5064c0cb3`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a8e79ba688cf0fc1c2b4e6a8531a4ba6d47f584deb6c37b584fcb22d6f3436`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a362f8dcdf342a9b842328b0ced017b5d7fb15c99243df065baa4566ec807884`  
		Last Modified: Sat, 28 Feb 2026 00:44:48 GMT  
		Size: 11.6 MB (11641115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
