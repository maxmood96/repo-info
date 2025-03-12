## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fa4d958eb2453fec999de01713c508b53a971fbbed9f3bcda63fbe7a275ec92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
