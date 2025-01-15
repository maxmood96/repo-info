## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:a23e84498a9a98c2b1a9dfa3b48a38c116831491c2fcc91c024c3bec41047eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 22:08:08 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 22:08:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 22:08:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 22:42:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 22:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 21:20:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
