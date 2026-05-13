## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a2cd087e4823118b4b9199e5c16012a875230d226f9780d8b87d006515160c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:d3d056bf1fea4615b3c5891eaf3b9a631526e174931941cb1cad7ff31756e0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261926295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531a5b56cd2ee2b16751d69e0ec0b81695d6b225f4224557dd9fd1a4721a470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:37:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:37:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 May 2026 23:37:24 GMT
ENV DOCKER_VERSION=29.4.3
# Tue, 12 May 2026 23:37:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.3.zip
# Tue, 12 May 2026 23:37:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:37:35 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 12 May 2026 23:37:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 12 May 2026 23:37:36 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 12 May 2026 23:37:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:37:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 12 May 2026 23:37:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Tue, 12 May 2026 23:37:44 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Tue, 12 May 2026 23:37:51 GMT
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
	-	`sha256:501f68ee4ec3df8e709de0c6a68dead6e0f2d4a50e602e1f955eb2c615012770`  
		Last Modified: Tue, 12 May 2026 23:38:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62a0234ef41158a27d532ab6232f14f8af532758cc5b9651e6f42455d590907`  
		Last Modified: Tue, 12 May 2026 23:38:00 GMT  
		Size: 378.0 KB (378035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e982fa1b07a52a470d543cbea18e8616f6ef685a3b7619d0955f1b6cf337e6a1`  
		Last Modified: Tue, 12 May 2026 23:37:59 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a2ca7c2c894b4ad8747520d94189a2786f2f47ecacd3bf783f1d2d674d35e`  
		Last Modified: Tue, 12 May 2026 23:37:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf4f4da7d56dd9c9634740725bbb4ddc3b34c9ebe1ac94b0cbd24a4cafbc7fa`  
		Last Modified: Tue, 12 May 2026 23:38:02 GMT  
		Size: 20.2 MB (20210296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7c058a79dc37d6b81f82405d5239ed17b9efb8b98dd89e6e0e497ce2579040`  
		Last Modified: Tue, 12 May 2026 23:37:58 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc84b0240e3328b9ab2afe0ff0aeac93515e3fb1fe66753fe3796e47f4fa47e`  
		Last Modified: Tue, 12 May 2026 23:37:57 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e2a2dc65c3a64853c56a7248f2b8859362a20a90b33c40e4193065e94c8a6e`  
		Last Modified: Tue, 12 May 2026 23:37:57 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d415af4598bc69ae9ae4cc0946f85bc7059aeca6fa3ae77281e4db020fdf552`  
		Last Modified: Tue, 12 May 2026 23:37:59 GMT  
		Size: 23.4 MB (23443507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9365d56a0d5f013c2d7028779812c720c94a9f5f0461c4deead03e6cadd67fb`  
		Last Modified: Tue, 12 May 2026 23:37:55 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b99303623625f7c010ac53762c9d0c31b84d5d7ecd7b9543cfd61ba15ffbf00`  
		Last Modified: Tue, 12 May 2026 23:37:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91709febb456b5a22e9480bbd7ab39bed2f0f9d0f5326576369039c71c3bf5f`  
		Last Modified: Tue, 12 May 2026 23:37:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc2bd004fc96bbf942dc709be69b8bbd29514fb99a36f6b21f79acdb2704106`  
		Last Modified: Tue, 12 May 2026 23:37:57 GMT  
		Size: 11.9 MB (11940687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
