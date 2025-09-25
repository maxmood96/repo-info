## `docker:28-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f83e6610b9060dfc4dc5339d951671637d9f3051a88ef344b638605588bc96db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:28-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:a937bbed072d521be6a982c216a819bba6335ed11f213e4843892552c02c24fe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348336904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c91ad57bf664bb401468d97ca8bc4e4f734de476d57791547d5ad2185e2e20`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 02 Sep 2025 18:02:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Sep 2025 18:03:16 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Sep 2025 18:03:17 GMT
ENV DOCKER_VERSION=28.4.0-rc.2
# Tue, 02 Sep 2025 18:03:18 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.4.0-rc.2.zip
# Tue, 02 Sep 2025 18:03:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Sep 2025 18:03:36 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Tue, 02 Sep 2025 18:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.windows-amd64.exe
# Tue, 02 Sep 2025 18:03:38 GMT
ENV DOCKER_BUILDX_SHA256=1e89de288c9897990220d2ee695b50956d42a3a0792c0b070e9fee7711b9f896
# Tue, 02 Sep 2025 18:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Sep 2025 18:03:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Tue, 02 Sep 2025 18:03:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Tue, 02 Sep 2025 18:03:55 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Tue, 02 Sep 2025 18:04:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8687826872210445ed9fb3dffa5934a5221d8146b07b19f820f9d25c054879e`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc1d1d0f77e1b1e002281108d6969f49c9370bb0926d533ef040bdb9783b89d`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 357.7 KB (357681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f047d82a6729e7ab112b8c091ace1605ae595f5752615b55251e6ce9bbc05`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3542a0e15238c26719c6623c8ba79233c1b0b99788106a8298dfa8c140eb6e4`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e7e9b72d1ab1e0b04a5b3491513b291d42a1f45a949d0209fbef15d2f2c962`  
		Last Modified: Tue, 02 Sep 2025 18:04:45 GMT  
		Size: 20.8 MB (20781508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ba49eec070de62c60b421b5409ed589beefdde9e101527c46b727a2e041b9`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ef258a913cdf6e4443767c05bab0463eaa17f3fc7a8ee6191dd10941739a4b`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b2a123b70288ec9dffbd4cb120874e4a70985d932b08fddb9f83319af30c82`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b712d514e93a8e6c91ea0f936b63a5a844aa09aade4a46de7b6180ff85876b8`  
		Last Modified: Tue, 02 Sep 2025 18:04:57 GMT  
		Size: 23.1 MB (23104919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9fef658903d23785dafcd499b3756d01cb8401c0325d32b795a033f14396f0`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bbdbc8dd63dab152d88d182a5c0f700081c9228d26910935a6327229cac312`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3087fa9bec1c057ff92b30b8c72d00d1f2a98bdc0bb9a6e8b726bdf8e7f02b`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065d834d32d703b390759c11a3f92c9754f0a5528ea89c840add6db996837a7e`  
		Last Modified: Tue, 02 Sep 2025 18:04:46 GMT  
		Size: 22.4 MB (22389245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
