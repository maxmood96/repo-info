## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3e78e4b3bbd7a8b9663fa3b09411da2139569cccfb6c179bb80cfa3c8b27a535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
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
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
