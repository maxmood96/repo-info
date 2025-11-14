## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3d255dbdfb3cd84597679d5d3ca0b4a9eba95cd13ee76c69e3ed677b0d2c8406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
