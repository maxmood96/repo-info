## `docker:rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:e9937901c087c14eadb0609de2609fcd54b69ea34c8fce2710b473203a9362c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:403258ef95ff1fdddcc35622dbfcea0ad94797e79ff9fca6f9ca7b50b77d4701
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542397347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d32d0d87b6ee14f3dcedaa891a7d28dbea4a9f0dc1c0dbeb0e77bfe3ffaf8fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 23 Jun 2025 22:23:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Jun 2025 22:23:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 23 Jun 2025 22:23:19 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 22:23:21 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.3.0-rc.2.zip
# Mon, 23 Jun 2025 22:23:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 23 Jun 2025 22:23:32 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 22:23:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Mon, 23 Jun 2025 22:23:34 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Mon, 23 Jun 2025 22:23:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 23 Jun 2025 22:23:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 23 Jun 2025 22:23:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-windows-x86_64.exe
# Mon, 23 Jun 2025 22:23:48 GMT
ENV DOCKER_COMPOSE_SHA256=f52bba6d8031da7e01c5bcf621dadea0afa41a317be09f2946701e15e899f8a4
# Mon, 23 Jun 2025 22:24:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c7008b17526d92bd263f18b826a5a09a9e9f10379377689f67f7c6c97510df`  
		Last Modified: Mon, 23 Jun 2025 22:27:26 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04dfab72015fcb95e77f61025f9eb828edd0656f0259d4b31f674afc383c57`  
		Last Modified: Mon, 23 Jun 2025 22:27:26 GMT  
		Size: 405.6 KB (405577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ea96b99d9265972141d07e48b327da6dfd80ed0df1cd2c64ce99139abf6dae`  
		Last Modified: Mon, 23 Jun 2025 22:27:26 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61de75cdcfa722139a79cacf4c4fddeaece5bd209575d26d88ca0e2df5edc7c5`  
		Last Modified: Mon, 23 Jun 2025 22:27:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a200e72b03556da71408319d4316ed7bf451cb5b4c71eee39d0b3f61c93773ca`  
		Last Modified: Mon, 23 Jun 2025 22:27:28 GMT  
		Size: 20.9 MB (20873225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600d0d12492bad0aaa6ed77e577ee99dea502a4243b06eaf3d50f11f16572cfc`  
		Last Modified: Mon, 23 Jun 2025 22:27:26 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e609c8994ece8274aefde2158e72faea75a1585fa306c34a4c32d0fadb3ac87`  
		Last Modified: Mon, 23 Jun 2025 22:27:26 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ffe4c54f63df2c273b373f007fe33e02296a8f171957792a5eb4e46f0c376c`  
		Last Modified: Mon, 23 Jun 2025 22:27:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c26cee4838c13473a9c3e07c46f39171194ccdbb82f4f12738f0db19b4fc0a4`  
		Last Modified: Mon, 23 Jun 2025 22:27:28 GMT  
		Size: 22.7 MB (22696039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b70086fdc46eb9a146e2c76694c89081183c189b936ecc99ca8c79fc65094b`  
		Last Modified: Mon, 23 Jun 2025 22:27:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7632d1a6ce06db0086d2b439ba2381aaccde8cc43589e0b237dab8ffa9c92048`  
		Last Modified: Mon, 23 Jun 2025 22:27:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db953f2a31727229e35fe61343c6e65fae6a4d354d8a1dc2c5726782a9f72285`  
		Last Modified: Mon, 23 Jun 2025 22:27:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00750ca303b24e0cedcfc1df329ae94f4c5e55750e8193b786655dc982dcba17`  
		Last Modified: Mon, 23 Jun 2025 22:27:35 GMT  
		Size: 22.2 MB (22236690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
