## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:0f5015bb466628fdfd18594e4de5b65e09631323ee555e80be32ae5dc8c138d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f310a3854e7bf80794dcd9ff1c8cc30806fd9645b5a5717472b2fed1c2fc5537
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704797453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5d4fa3d80518f588ad3eee4f7f6ee350dd0d2d76f23e98bf9bfa681733e74`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:35:34 GMT
ENV DOCKER_VERSION=24.0.2
# Sat, 24 Jun 2023 03:35:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.2.zip
# Sat, 24 Jun 2023 03:36:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 03:36:08 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Sat, 24 Jun 2023 03:36:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.windows-amd64.exe
# Sat, 24 Jun 2023 03:36:10 GMT
ENV DOCKER_BUILDX_SHA256=e314569943a591a097fa9119bf786556a4eb5c710e8ddefa57e95cd95aa7cc7f
# Sat, 24 Jun 2023 03:36:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 04 Jul 2023 01:15:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Tue, 04 Jul 2023 01:15:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Tue, 04 Jul 2023 01:15:45 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Tue, 04 Jul 2023 01:16:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed839336f22dd57d3537286fd2cb28bb3fc0572198a3b9bd727227ee4cbdf055`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce643c4303a7b93be26b0dd0216711bedc40974b948aa175e501ebfd967e8da`  
		Last Modified: Sat, 24 Jun 2023 03:41:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc026cb3268fba4d3f45b15b22d85c45b0833d7e6f03faf3f1adb1f7750eb889`  
		Last Modified: Sat, 24 Jun 2023 03:41:57 GMT  
		Size: 17.4 MB (17427965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ada76c0fbca30898687db44782375adfd8511d9f5fe79eb1df4524e36cb3b`  
		Last Modified: Sat, 24 Jun 2023 03:41:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a336a464a58681af94fdcfb3fbc461c2ac77b4bd2d6ec0c339fbae654521420`  
		Last Modified: Sat, 24 Jun 2023 03:41:52 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f6fe82d1e4f989c122320481c6c3473632cffcc634f225106e7c73585db1c7`  
		Last Modified: Sat, 24 Jun 2023 03:41:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f83ed64356628e46ae865b628bc2568b3e8679ec35b1c6211d4c49ee99d80`  
		Last Modified: Sat, 24 Jun 2023 03:41:55 GMT  
		Size: 17.9 MB (17857203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575bb31d4e1e844481bc4365c5a09edf18ca961693140e5fd407ab5a31943de7`  
		Last Modified: Tue, 04 Jul 2023 01:18:22 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a439f4a0f428f900ced959aa5f68c22dac2269bff9bdd57b58fbc8f7d369589`  
		Last Modified: Tue, 04 Jul 2023 01:18:22 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dc63a64ccb561d80e3f36ce2e08139e02746ab4884c778ca92c4b867f445f6`  
		Last Modified: Tue, 04 Jul 2023 01:18:22 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5bcee50f9938bfef5140021817f8dac5f7f2a23e6a07a960d54ac08bce33ee`  
		Last Modified: Tue, 04 Jul 2023 01:18:26 GMT  
		Size: 18.5 MB (18457426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
