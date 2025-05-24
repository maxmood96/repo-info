## `docker:28-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:0eb8599d4c139d3a62faaad8c054931a01691351ae67b79757590f304bee8992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:28-rc-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:f1a89df7c53c7dfac7b29a6612fa88952449c40867eb4b01e0f270d169928410
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248868900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056565e8f6ee860761212d44751317c2e99b8be580caa62f78746d274278ef72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Sat, 24 May 2025 00:22:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 May 2025 00:22:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 May 2025 00:22:44 GMT
ENV DOCKER_VERSION=28.2.0-rc.2
# Sat, 24 May 2025 00:22:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.2.zip
# Sat, 24 May 2025 00:22:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:22:56 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Sat, 24 May 2025 00:22:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Sat, 24 May 2025 00:22:57 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Sat, 24 May 2025 00:23:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:23:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Sat, 24 May 2025 00:23:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Sat, 24 May 2025 00:23:06 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Sat, 24 May 2025 00:23:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ef241f8b857578702f535bb88edd7ce6097a0f2cdafbdaf5707d4fdbb91b8`  
		Last Modified: Sat, 24 May 2025 00:23:20 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e10efa7c358f5f265995a5ca81fe2b9a78d81ecc4ca9d694c947e4eae26b9b3`  
		Last Modified: Sat, 24 May 2025 00:23:20 GMT  
		Size: 376.6 KB (376641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2535217676498abcbd0c07b49661eb3b8723343f213591611e6bf30d0571fef`  
		Last Modified: Sat, 24 May 2025 00:23:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9798f17e81f73297f77e2ed8cfd41ac06691099e1ed339eb84f921a5b652d990`  
		Last Modified: Sat, 24 May 2025 00:23:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d5e58b58549cfbaba9ecc0f92581854eb132815cf282974ac3bc95d8e547da`  
		Last Modified: Sat, 24 May 2025 00:23:21 GMT  
		Size: 20.5 MB (20462420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546ccfd97644ce015beefbcff4592d23d654cc76e17d172d54cc8fa37bddd641`  
		Last Modified: Sat, 24 May 2025 00:23:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c161426b0e02f75b7d46a19197e9a79fdb13556b35b6752bb595120c27668463`  
		Last Modified: Sat, 24 May 2025 00:23:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143158268e9d8cc97f2b7f7d22ac3a3e4d2de4e9757d680a99762648f241736b`  
		Last Modified: Sat, 24 May 2025 00:23:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bf40d8ee540935c7d1cf46a9a739fbd5e4896af5ee60f96a1ac9592410bf94`  
		Last Modified: Sat, 24 May 2025 00:23:20 GMT  
		Size: 22.3 MB (22279213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25cc3aab05ca82eb9814b69b3dbaded9d5abf57a18300db2d97eabf4f15645a`  
		Last Modified: Sat, 24 May 2025 00:23:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd42897d40d8c74a99f11996e69177ea6604d66fb384292013948edaaafcea8`  
		Last Modified: Sat, 24 May 2025 00:23:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ffcbcf45cb2a43d118db419d2e5d0c9de2ef2aa09eb900e5f68ec5e8e49db6`  
		Last Modified: Sat, 24 May 2025 00:23:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff5d903c04ccd00920f42fe293681f173c3027bd53d9a5e4121ac2b9cebbc`  
		Last Modified: Sat, 24 May 2025 00:23:20 GMT  
		Size: 22.0 MB (22021514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
