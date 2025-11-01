## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:dc41eb31437b5f5b96c3770f1fb85c9f1cf5f7b9d6fc806e2947f8d85f44a669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:871e69554bf56df735f248121de1e93ebd817d84b0aac1a8be0b35cc0f4ed889
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3287397357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0debdf3c164797188654d94b3b856fe4f5ffccf4697d46b66b8165325b45b5dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 31 Oct 2025 23:59:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Oct 2025 23:59:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 31 Oct 2025 23:59:43 GMT
ENV DOCKER_VERSION=28.5.1
# Fri, 31 Oct 2025 23:59:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Fri, 31 Oct 2025 23:59:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 31 Oct 2025 23:59:58 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Fri, 31 Oct 2025 23:59:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Fri, 31 Oct 2025 23:59:59 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Sat, 01 Nov 2025 00:00:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 01 Nov 2025 00:00:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Sat, 01 Nov 2025 00:00:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Sat, 01 Nov 2025 00:00:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Sat, 01 Nov 2025 00:00:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc526edf0002209c81ff3c5d6fb622cc6e858c2254f238c4972d2b726b00754b`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe04abbe3ef736ccb6492d759b61d4bcb045526d66ecc60c6bb655bff2c247c8`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 385.8 KB (385836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676d5ebdb28b29ee20caa6ce4769980bea6e67f4c707371a4a9cd2e88daf4f4`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e860b3de84cb81ca7ec484c9e36ff7cfaf3530ed5a8ab762fec932cfaeed30`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d511b2cd6a7b4283ce10b94aa5e7411a6c14ea531e6df2f23bf24cba302d9f04`  
		Last Modified: Sat, 01 Nov 2025 00:18:05 GMT  
		Size: 20.8 MB (20792620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423cfb084830ceda4d96169fefcfb945fb9f135a19646f53ea4bafacd2534ae`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6dd50c2a2a14e253157e4b93785f9b08504f2668e272f6d67211d424141c3d`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec07de3a2084c08d6dad88c7ae76475ee8c79d4f0452c594cc54b9b63e5a692`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d2367a664de75a0a0e8661070ec6df6d1fb9904d6c0cca4a5482907a4648c2`  
		Last Modified: Sat, 01 Nov 2025 00:18:07 GMT  
		Size: 23.2 MB (23173729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a748831fa362f544d5abbdd503de87258aba945cd6ddcc65cea9cba5af3abf3a`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce27bde16d8f4317b3f45906510eaa53273b6efd4cac1c2c00d5ab292817177`  
		Last Modified: Sat, 01 Nov 2025 00:18:05 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40efd1f5e8a6b41239066da4d8dd2e89ba6ca367d9dd39a11500091df5af0d4a`  
		Last Modified: Sat, 01 Nov 2025 00:18:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d54da9134adf84111849d3e96556e0f6462fdf1aa1d7211382280d93ff5909`  
		Last Modified: Sat, 01 Nov 2025 00:18:08 GMT  
		Size: 22.7 MB (22686372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
