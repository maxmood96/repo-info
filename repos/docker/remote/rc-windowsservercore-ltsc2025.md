## `docker:rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3c5b527ff3bda84d94b34ec503f9d47047b0f56773df6d23ec7843f6c586f8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:af8fe33abc64add24c5a660d2e8a4d6c865d66a1297abd74b6f34848704ca95a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496126139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c231a89c8c540782e47ae99ba7cafa11af86ce0dfd5449c3fdb55fe8dc40d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 21 May 2025 19:21:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 May 2025 19:21:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 21 May 2025 19:21:50 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 19:21:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Wed, 21 May 2025 19:22:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 19:22:02 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 19:22:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Wed, 21 May 2025 19:22:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Wed, 21 May 2025 19:22:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 19:22:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 19:22:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Wed, 21 May 2025 19:22:14 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Wed, 21 May 2025 19:22:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5828b1d5056860a3145b8515ba785b73b260c1cf3762a1350b0c81b4c2360886`  
		Last Modified: Wed, 21 May 2025 19:22:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515c8bc9f80c41e610675c2d4bc3240aab88fcc8fab5b13a750c28c3997de0b3`  
		Last Modified: Wed, 21 May 2025 19:22:29 GMT  
		Size: 397.4 KB (397414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9560460cf41c809f4b1c9a61d2c76b34fda054e103523f078d2d9bcdad349289`  
		Last Modified: Wed, 21 May 2025 19:22:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3baeb53de79a25e2fe403e7cd7fd207b6961bb6d91cf763b76b075a4409a5a`  
		Last Modified: Wed, 21 May 2025 19:22:28 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31518ef9116c05f1ec049019a0a660132a615284421d1c8e16d4d6a6c504c89a`  
		Last Modified: Wed, 21 May 2025 19:22:29 GMT  
		Size: 20.5 MB (20486363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a3c4c1f351e3bf258db48d860e360b42999606d8854a9caf419b6ae1dfb16e`  
		Last Modified: Wed, 21 May 2025 19:22:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7ddc75fb8d9296856367045675b2b6e2f0cb76321ae59f2781c11cbc0d2b70`  
		Last Modified: Wed, 21 May 2025 19:22:27 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5b3e936f34b43ccf863432052c4f40c674abaff996b8fadb05dcfa5359f45b`  
		Last Modified: Wed, 21 May 2025 19:22:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2372d324f0b634ad04df3ea9d288d15817ba70a2bc0e99d14f754567e2fb208c`  
		Last Modified: Wed, 21 May 2025 19:22:28 GMT  
		Size: 22.3 MB (22293001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6105ff81ead97ab635757e03b3b81873fa445e468b9ef872b4d16a2de83f117`  
		Last Modified: Wed, 21 May 2025 19:22:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbd42d2405e6431827eb0be8f5095dc38ce3a456d531c79f0670e6512027cf`  
		Last Modified: Wed, 21 May 2025 19:22:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37d1e1eef0577977318037531b7e88c626cef1cd9b5473f86de4b8c23f8b8ae`  
		Last Modified: Wed, 21 May 2025 19:22:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1522133e64bad38c46a174ce2224768882fde27928d8e3300eb395d7d0f677`  
		Last Modified: Wed, 21 May 2025 19:22:28 GMT  
		Size: 22.2 MB (22171886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
