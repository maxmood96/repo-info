## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:cf52fc75c50a0b3ee0fd34f484cb9e7aa12c6b6f6187e520f1fc9cb2a96807fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:d3430dae25034c55c56dd585271ca3ff7633e012a1ba11f1498b04f25693ef2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286034630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734e887c89ba0c951f704dfa1208365d6a2457d51ed341c05d8223c37bd652a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Tue, 11 Nov 2025 01:09:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 01:09:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 01:09:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 01:09:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 01:09:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:09:59 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 01:10:00 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 01:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 01:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 01:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 01:10:20 GMT
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
	-	`sha256:84cbb13e31831b4a401483474d0b3761d526123e4940ffefb9e59ca0b95bd928`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11778e4fa17626dc91d9d9cb467403166f0cc6134bcadc2c6c394c23f4f77350`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 385.3 KB (385346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea88d46cd119b0ed069843b33c117aa143e9f6c36695cf17ee648d8dcf3655b`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5fa37b5931fe92505e086ba67d6dfb0da4ae0172b58b04d5bb013277f60b9`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ada5899e6769690fd204f9f137706c9612fa97a65835249036bb92593e5eb`  
		Last Modified: Tue, 11 Nov 2025 01:19:20 GMT  
		Size: 19.4 MB (19430246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0272441663d6fec957c0b4d34b58b8a19b8808f1771c45d4c591dff46cb951`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918e1ab8b826581917ab7b2d53b2c6a5f2b06ce5c03f208c14dea008b3cfe60`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d1376a231ae8f91e59637fe876b6fa19bccb1bfd0a4e96c4d2b5d24a5ae5`  
		Last Modified: Tue, 11 Nov 2025 01:19:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f749f808cf8c30f6a915e56d9393b185ef4a06c9ab0ce38fab25952828f43c6d`  
		Last Modified: Tue, 11 Nov 2025 01:19:18 GMT  
		Size: 23.2 MB (23173614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4c6efb8d391dc41567c8e29c5f2c1aaa0d6372c5dab092454b25133fbaf22`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f789efcc4cd75dab1e0486cceffa4fbb47564e174bfb011d328003e81c690ad`  
		Last Modified: Tue, 11 Nov 2025 01:19:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73f4b7bd98ba3e36992613125ce4ea0186486089e65bd5b3be8e14604b916f0`  
		Last Modified: Tue, 11 Nov 2025 01:19:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ae4ce13bc5f392ee40f76f48ccf05ef5a576bd04b4b7affecfadde7443a36`  
		Last Modified: Tue, 11 Nov 2025 01:19:22 GMT  
		Size: 22.7 MB (22686606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
