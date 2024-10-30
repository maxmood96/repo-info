## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:134ee55063a0ce1e9ae80e14e7d4412d40320285f3e74dd116773ef49492047d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
