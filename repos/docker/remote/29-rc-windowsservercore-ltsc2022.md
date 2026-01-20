## `docker:29-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d6906a3c6421e2eea78554a71060b59f2706b9a7f251a4a2fad1d5e78bc3ef43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:8afa41bc87cff08a7c12096922216ddfb3742c53f4eb0d8af3e26041f8b211da
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1890886241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04c850e02448b3a4b7770b7edcaa01df4b37fee031b432a098066ac71922b5e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:52:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:52:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Jan 2026 22:52:45 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Tue, 13 Jan 2026 22:52:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.2.0-rc.1.zip
# Tue, 13 Jan 2026 22:53:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 22:53:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 13 Jan 2026 22:53:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 13 Jan 2026 22:53:04 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 13 Jan 2026 22:53:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 22:53:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Tue, 13 Jan 2026 22:53:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Tue, 13 Jan 2026 22:53:22 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Tue, 13 Jan 2026 22:53:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23bc3ca2680b957e34cc3091ac9144824a7199ca3cacec82251cc10fec8f7a7`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e89d99b6c42cb54c9f5848a7f3614ab3e11ec7cce3f0b0fc11e5fa800cd603c`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 480.0 KB (479968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9f23b39cf20b9f7c69de7f891b52cf568214abba62aaed2b5fa75a3ea65e7f`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8cd1584e40cd14dd7ad9c7064c1bbdd7cd38b98668dfd445cf0cec1e10e1c4`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec2d0dc9ec845d6410f241ac749463dbd553fceacac1b96468335ad8c300f1d`  
		Last Modified: Tue, 13 Jan 2026 23:01:22 GMT  
		Size: 19.4 MB (19405277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd7908890733c17a8dcb4c67380fdf5a1a9d9d7bc94c1a1243e646ae708de66`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b37196b52c66a985cf42f52d977a73ff802ff93bd7a90a5be6e4a11efed8b8`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c0bd91450c22f11622a834e611b1601602752f2e1cd322f01018ee5a81d091`  
		Last Modified: Tue, 13 Jan 2026 22:53:41 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb12ad46df6360ddb762d7245cbf110577c16bc3ff086a53d2d9b1ec6763c332`  
		Last Modified: Tue, 13 Jan 2026 22:53:51 GMT  
		Size: 23.9 MB (23904864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2dea3b04a666e1832103ea7a6175a0b791f66c8a94fcf19d1e625048ea65af`  
		Last Modified: Tue, 13 Jan 2026 22:53:39 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476cb382479e5904229f0c02889bf45f34619470217f4278418350ce96d4be36`  
		Last Modified: Tue, 13 Jan 2026 22:53:39 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e994d58eb1ff500890652e7fcf83297a6b29b44d6b81658522eba9c6b9302b2d`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23476da1d9f559021b9515f27a69f9352fc0c6b72ae6f9736153ea78d6f1633`  
		Last Modified: Tue, 13 Jan 2026 22:53:41 GMT  
		Size: 11.4 MB (11425095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
