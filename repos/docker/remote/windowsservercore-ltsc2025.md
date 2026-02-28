## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a86a7f53fd5f28509c601a3bee5223705f9e2da2d13c6aa49559db7ecb7fa913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:8adc1ea2a335bacb49fd01b1cac0cf3288b6241ce54744a6f1cb58f27720c443
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2025646567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f960ce56780111af6819315df734df0ac835f351417abb824f38888e95b16e9`
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
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:44:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:44:19 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:44:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:44:30 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:44:38 GMT
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
	-	`sha256:0c8fecd8861c56fefbd35822e522c756a164aa3d37dd262f98ad438a95f8db81`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7b071c2faeaa8569fda83bb88fba9ed73846631970b3b0d14721fc48a8559`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 369.0 KB (369040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349d48567f1c6c7903eb5d37de6df665046e21340c38e0a4a5979d7eb05bca0`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ef673a03e21f60cb7a2f30229fc9fa4f379cb921aef1b72951239cfdac5594`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e190b3d2972d3201fbae0ac07c094428f7a732d8e416908d03315315aaefa`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 19.4 MB (19445004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369575b922e845d939ad940aa1ea82e9cd08f06e346a0001ea7483ae5cb2c9d`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1522ec443e28a83261bf5734712b4c9e11aec045f70d11b79269e263ce14e8a`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c077c7089ab69c4846f6326bfc8b115c5d20413f8c10b6a513721c8c295a3c3`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfd81c02864aa131850545bb63bf55804e738732881a931669f9a619979c074`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 29.4 MB (29419828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b640fd9bf971384c0ef0f4d964b6d311ee0a0d66729df8dd2ca97af1ccaba502`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff016c0dfe5242b2a2a90ceaad29581fdacfef972a2f8709b33f8e7ee17fc0bb`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b503dbc573993dbb1567403db5b6765a54d2def3ede2df5271ed13b54484aee`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37151df22c07f87a0463edda2aac3d9ee8578d7e747212faa48f66fd04767c54`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 11.6 MB (11641004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
