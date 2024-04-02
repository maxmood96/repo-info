## `docker:25-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:dd3fbbea52547a9ca17881d8ebf6504cadb2e8d1e0c17a4d8326e01dd108ac0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `docker:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:f8562c9187c25453843c0f7bb2155b3a6a56b0004618ebbb069d3ad49368ac64
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2014411699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39de8413791bc0d3e15a936a6830b9945ae5c3d0387ff39811653802c5f25e6f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 01 Apr 2024 23:49:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Apr 2024 23:50:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 01 Apr 2024 23:50:38 GMT
ENV DOCKER_VERSION=25.0.5
# Mon, 01 Apr 2024 23:50:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Mon, 01 Apr 2024 23:50:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 01 Apr 2024 23:50:54 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 01 Apr 2024 23:50:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 01 Apr 2024 23:50:55 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 01 Apr 2024 23:51:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 01 Apr 2024 23:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 01 Apr 2024 23:51:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Mon, 01 Apr 2024 23:51:05 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Mon, 01 Apr 2024 23:51:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a991b168b9e3699fd9d7abe27fe54b030e19d0649329c3de60d5976082b3d73`  
		Last Modified: Mon, 01 Apr 2024 23:51:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47321057c96b34d11e1050971e2110b903e6a12fa8c46f8a38e8bf11d9b035ff`  
		Last Modified: Mon, 01 Apr 2024 23:51:22 GMT  
		Size: 499.0 KB (498960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb354736c3a07a76a7e3f2ac359d68a3fdec71020fc5c4a21278cce846d73bf7`  
		Last Modified: Mon, 01 Apr 2024 23:51:21 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca42fc766517c50c9a25bc8745ffdf6ca0a29fa81fdc59a23b4e9c34d61885b`  
		Last Modified: Mon, 01 Apr 2024 23:51:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e34414952f2f6722044068fa58293e070ae3bb09d2c8acdf111ff1e9947ac6e`  
		Last Modified: Mon, 01 Apr 2024 23:51:22 GMT  
		Size: 18.1 MB (18075421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c230a8c5e955cf949a6c9a3e898d8bd7dee1ee42e07986b5c2cd1661219a148`  
		Last Modified: Mon, 01 Apr 2024 23:51:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594064d58df1b92582b9765d6fe247a9cc30a5d5efb0057e18661b97cd69aec8`  
		Last Modified: Mon, 01 Apr 2024 23:51:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76055e8e5a43223aabe65950f3c2bae00d2231bc39b8023f0d89458a6b18ac7c`  
		Last Modified: Mon, 01 Apr 2024 23:51:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fe9b099db2ebf039cf0cd38659b09e3105f2a0be85f08def25484e045e3d0c`  
		Last Modified: Mon, 01 Apr 2024 23:51:19 GMT  
		Size: 18.8 MB (18831426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e89c056d644177a8104c6eb7cf234e7a675f6f45934a17d96247164da4d517`  
		Last Modified: Mon, 01 Apr 2024 23:51:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc434c283491503e74ada3e12525cf97c7018129c2cfad1761cbe8e9767cfd6f`  
		Last Modified: Mon, 01 Apr 2024 23:51:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cad8cfcc4d8055ee22104d3de6fc3311166481ae8ff52ce8a60ddccaa931548`  
		Last Modified: Mon, 01 Apr 2024 23:51:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07daf5ca193fb7fb3c12f81702b9298c4d813849051524a9758ba51ee66132da`  
		Last Modified: Mon, 01 Apr 2024 23:51:19 GMT  
		Size: 19.5 MB (19535262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
