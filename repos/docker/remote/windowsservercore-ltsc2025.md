## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:d385e3828e8366b07bd0af1a4b025c4feb365a506fedb8e307acaae417e63f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:e4420a2945552c16d362b8472d0182a0ec134ce320f2233ec15e93015e599e8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262478653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d0a0d1bad4f84f1fbcaf6c1e419ce3a0952a03ed6d4582f9767303292ca6c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 22:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:21 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:22 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:16:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:16:52 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b535a51fd23dbc5005aa72b61e95ad333b54b6b5276fd600c8f26dc1ec6379`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1111f6cb7254129e7ea39ba28883376409a104ffda0b87a45a420ceee27fcb`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db17ecf93e3efdbccd835fd5d408afb7a3351f7597a48a1ad636c01794ebe04`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83f256bcd38582b57bb91e485a2d85240d5f2ae45b27c9afa7a9a5f44ebed73`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdc10f672c38740ac0512c480a10fe4b0dc1658659e00513da102771c2e3e40`  
		Last Modified: Fri, 15 May 2026 22:17:11 GMT  
		Size: 20.3 MB (20260443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a9dc340d0bdbccbce6b57c4d89cad2a1db92d89f7c2649002da080b5334bd`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309766ee1a21f57c947e3ef48cf4592eb1c12fb99926f92dc710c73dff7b930`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8a3c0bbacac0c1695cff5c5e5eeefe513850e0a04322d018dfc23f9317a07`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562224ef98ba779eb91088241d392cb2a71abbc685b008022439f669f7686d6`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 23.9 MB (23920245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af350faa47b96f1766ca0debecbe39139716c8b55ae988b2528535eed60cca`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780002467e4bb1a15f8748b2ea889bc85483b2d7ddb96b528e3b32c982692e19`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e3ee62773736f785dc51e4bc1a7e48595fe0afed17ab1d89154d1e06595d11`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d076a230450a0b438ed3c7d1ee23904031d66dddd7e9ee8ac765637eb942ff8`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 12.0 MB (11951730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
