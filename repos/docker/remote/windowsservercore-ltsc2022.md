## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1edee620df03f6581534e31d7e00ac9e635d810d120ea99065745f34da34a734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:689c42c8850d942c90ae9c75fcbc5cea66b7090a5dd91ce4ef75a90d3c7af251
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2126291699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6847652324316be842b0474015c6fd08139ba36c87dd83cf74bfd740059427a3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Fri, 08 May 2026 16:48:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 May 2026 16:49:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 08 May 2026 16:49:28 GMT
ENV DOCKER_VERSION=29.4.3
# Fri, 08 May 2026 16:49:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.3.zip
# Fri, 08 May 2026 16:49:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 08 May 2026 16:49:40 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 08 May 2026 16:49:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 08 May 2026 16:49:41 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 08 May 2026 16:49:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 08 May 2026 16:49:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 08 May 2026 16:49:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 08 May 2026 16:49:52 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 08 May 2026 16:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b337cde50c0759a6d813d6135b7d5c969ef86ba45eaf2474e985e80329b862fc`  
		Last Modified: Fri, 08 May 2026 16:50:10 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f8869e5132aa478bb632cf6685295339d6ec19a34d8df77a956ad43616023e`  
		Last Modified: Fri, 08 May 2026 16:50:09 GMT  
		Size: 505.6 KB (505582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075b46b136b262a1312240ec65b1b10d83929fbc979aa13a6a6fde8b48d57fa`  
		Last Modified: Fri, 08 May 2026 16:50:08 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c92c8fd347d549c7caeae2d1eeab27f99a5f7919d57e06a42a9b53da6428ff0`  
		Last Modified: Fri, 08 May 2026 16:50:08 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a652f7d4182d65548498def6b1586f6ebd1a4ec02b85780b01cf16e92caf902`  
		Last Modified: Fri, 08 May 2026 16:50:10 GMT  
		Size: 20.2 MB (20197339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2070953893ce38f8bdcc804da9b12958bc2796d0341ceb7db355d4f4a927dc`  
		Last Modified: Fri, 08 May 2026 16:50:06 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f25403fb3a9e736c6b7a647d388cec3d82df57a665c1ed92390e2d414482a2`  
		Last Modified: Fri, 08 May 2026 16:50:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f4ec58719547e67a79e66dfdad5aa28f0daff57a792a107943a55b308d3857`  
		Last Modified: Fri, 08 May 2026 16:50:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71998f76bb652fdef12cec58511de727931da051448503a67028fb9f72cb5eb`  
		Last Modified: Fri, 08 May 2026 16:50:08 GMT  
		Size: 23.4 MB (23437369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b783b5fd3c292b21e6610ae654eb241c27329b097d853fb6f02833a0e641510c`  
		Last Modified: Fri, 08 May 2026 16:50:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0820ce52901c8c1046b72e50ab3c6a5e53c5562d1c7302b4b48f0ace1fcc3af4`  
		Last Modified: Fri, 08 May 2026 16:50:05 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3865132c4c248b33f9fd29405dba032bea9de906a2c99ba3cea2455586454d`  
		Last Modified: Fri, 08 May 2026 16:50:05 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd97b04e3c00c87ba7792f144286060d17c7c384325b4ee3b8ffe836ed9fa1ec`  
		Last Modified: Fri, 08 May 2026 16:50:06 GMT  
		Size: 11.9 MB (11928321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
