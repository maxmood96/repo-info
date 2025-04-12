## `docker:28-rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:8868236e297c5a51f0968aed7c7a586e0f9d4be8b7adff5f701f25be5db308c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:28-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:c9f7620f8decd55000f891e4e530535f211fab505d804ca2c9968d5c4f561b07
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459626548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff798cb5fbda09302015d596f10cf5e7f2e78ce0bc5036d9092dc27a6f459fba`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Sat, 12 Apr 2025 00:54:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 12 Apr 2025 00:54:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 12 Apr 2025 00:54:23 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Sat, 12 Apr 2025 00:54:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Sat, 12 Apr 2025 00:54:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:54:35 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Sat, 12 Apr 2025 00:54:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Sat, 12 Apr 2025 00:54:36 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Sat, 12 Apr 2025 00:54:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:54:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Sat, 12 Apr 2025 00:54:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Sat, 12 Apr 2025 00:54:47 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Sat, 12 Apr 2025 00:54:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e52250079b1072cefccabf33ac9f9163153b024d66477389510eb9639d9dcd6`  
		Last Modified: Sat, 12 Apr 2025 00:55:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49569b0248bfc38217531f89c97d60357d5cd897cdf16ba9a5530e45b10ef042`  
		Last Modified: Sat, 12 Apr 2025 00:55:06 GMT  
		Size: 380.3 KB (380300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8289099d680405c097cd46f9710916bc245714d91e9052610d6efc9b6ef0c911`  
		Last Modified: Sat, 12 Apr 2025 00:55:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140ce2fcaa9abd913edcbab4e5d8ed1f63cabc72c94c23e2f997940af6cbc646`  
		Last Modified: Sat, 12 Apr 2025 00:55:04 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4feb188ba5231ee2f68507591497b0ef1a40a51d603e396ee07d75093578e3c0`  
		Last Modified: Sat, 12 Apr 2025 00:55:06 GMT  
		Size: 19.9 MB (19905126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7c01936c25ba3d98099115fa48a856499ffc9e8aee226b95275f7616be321`  
		Last Modified: Sat, 12 Apr 2025 00:55:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153c6c573782122ace3741fd08ecb37cb37bcd804d788001a3712f7dd9740cdf`  
		Last Modified: Sat, 12 Apr 2025 00:55:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3989683909d8a285a4a67a3820c62f3053a9ebee98a061e1b7b14fb6e8d13b52`  
		Last Modified: Sat, 12 Apr 2025 00:55:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a165aa650a57815627e1dd5229b3d5538763d59200a3bcd47fe06d135e1422e`  
		Last Modified: Sat, 12 Apr 2025 00:55:03 GMT  
		Size: 22.8 MB (22788485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898d1cb8d0886928182966aca90c541cc80ff244020b32be118f32bafe2a0450`  
		Last Modified: Sat, 12 Apr 2025 00:55:00 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52c212a2101e5db2300fc0e5582618675e29d70bafce336e871731828814f8c`  
		Last Modified: Sat, 12 Apr 2025 00:55:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94d700a72581ce491ebf7726df085c5635209c658cf9d8fb5f6a36eaa78acd0`  
		Last Modified: Sat, 12 Apr 2025 00:55:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d88cf1690aaf34daf7f62e68239198d2c83b057b88a353e7e8f478bce8f0f2`  
		Last Modified: Sat, 12 Apr 2025 00:55:03 GMT  
		Size: 21.9 MB (21861432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
