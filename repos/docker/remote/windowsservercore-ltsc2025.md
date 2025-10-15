## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:10b5e6906e4e5c97573e12c8dcdfc4c88ff1e988235c0f43e447b04af30851b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull docker@sha256:52e9ebaf8de61d6664b4e6201e1db13472b9695af9d8cc986ddfa1e1d9248842
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3287312349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea10513392ba247c658066bf10212ad354b15409f3b756abe2846428781eebc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Oct 2025 20:43:46 GMT
ENV DOCKER_VERSION=28.5.1
# Tue, 14 Oct 2025 20:43:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Tue, 14 Oct 2025 20:43:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:43:56 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 20:43:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 14 Oct 2025 20:43:57 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 14 Oct 2025 20:44:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:44:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 20:44:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Tue, 14 Oct 2025 20:44:06 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Tue, 14 Oct 2025 20:44:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b2b727d784eaba45ce0b483c5428794b03e121ea025e796ec39aaeaf274a77`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6a2cf39d46f6a96d1baa7a84941b4f76385c2262ba4a8211c67b59f0ab87da`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 355.5 KB (355491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0812d8bdde9efa1d9ee2aa94cb4ff47d65010b9d846f25b70886a27fd293fd19`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a996a1d2d4f6d8b9b54126bd672e1e7bcacd2bc1234a493992602882fac55840`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb89bbd456f6936c53638ec429da09b926c1e7747aba795306e5d700a352d0a`  
		Last Modified: Tue, 14 Oct 2025 20:52:48 GMT  
		Size: 20.8 MB (20768006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d210b4d06c550b8b7c45135cd8ecd606551fbabe2ef311be0ab42aa00808a6f5`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69f62fae2c3ee426e65ea7104999507985780815b3e44358313f2280134400a`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c97feba363065cbc88b05568a3f8c80042b5adf31def71bf8171c4e5404f3`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac9c837d861f92d8ba6675c391da5f0e58eaa075f3595ce507a56ea772cd3d2`  
		Last Modified: Tue, 14 Oct 2025 20:52:48 GMT  
		Size: 23.1 MB (23149490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e79d630081eba32a28d634a229c88c81675a510ceefc0cc865d9602d7cfe7d8`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9bd3dae6ed251e687c19db623b2debb044aa58da489c6cbe14865c08295a87`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30909a435732d7fdcb18db0811e71305bbb299136b08c5c6666794d57391839`  
		Last Modified: Tue, 14 Oct 2025 20:52:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ab6bbe5a559cb9d79103a7478e406abf8a4fbb314a5944b037b5a967aad840`  
		Last Modified: Tue, 14 Oct 2025 20:52:49 GMT  
		Size: 22.5 MB (22547131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
