## `docker:25-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:31f4993d6ec0f2bf8d24282d250c88148d8bc389c2015699da2d5425ed72c64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `docker:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:72a2d18a7e5bc963dc9c5037fa70dfb8096b0388daa682fae8bd247a677e7adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013932491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dbda5f290ba03e320fea6afce03f2499d1062dfa9eebf47ec1222ca2dca7bf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:03:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 00:04:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 00:04:02 GMT
ENV DOCKER_VERSION=25.0.4
# Wed, 13 Mar 2024 00:04:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.4.zip
# Wed, 13 Mar 2024 00:04:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Wed, 13 Mar 2024 00:04:17 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.windows-amd64.exe
# Wed, 13 Mar 2024 00:04:18 GMT
ENV DOCKER_BUILDX_SHA256=001dd8c707862d7c7a7bc17ebb024922ee304bddad1bca11da5b3b3ff18effa6
# Wed, 13 Mar 2024 00:04:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Wed, 13 Mar 2024 00:04:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Wed, 13 Mar 2024 00:04:27 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Wed, 13 Mar 2024 00:04:35 GMT
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
	-	`sha256:3b76541448783ccb077045cc46e35389fc30567b873b9a1ea5cc95e79d0001f7`  
		Last Modified: Wed, 13 Mar 2024 00:04:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f56cdc29c0dd7a7f2d08b29d3c6995b290fc89ac1b5e9e20e36730f1cfc59`  
		Last Modified: Wed, 13 Mar 2024 00:04:41 GMT  
		Size: 489.8 KB (489751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81563a72d86da3fd6dd17b1de4461349ae0a7d9fc877711c4f6eb01883e4af58`  
		Last Modified: Wed, 13 Mar 2024 00:04:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f453debc105e3730989440ea8cdfdace1ebef7d4f6caf3236d9c7b952915651`  
		Last Modified: Wed, 13 Mar 2024 00:04:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8e0696c49420d3e3d91fefa881db25ea90fb63cff85eb0d81587de08484f9d`  
		Last Modified: Wed, 13 Mar 2024 00:04:41 GMT  
		Size: 18.1 MB (18070318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd4e892a7afa06b75d74f071aa5fe64f642c6057e42d9aee84b39c198ecb34`  
		Last Modified: Wed, 13 Mar 2024 00:04:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091a06312216a85f3f29aa7a6673fc343dc3824a0ac0be1a6eac8a9fe276bd1e`  
		Last Modified: Wed, 13 Mar 2024 00:04:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6552d9b284c21420f0ae9fcb1a1366afda07f47f16e675ab3da700ef3fa6dc`  
		Last Modified: Wed, 13 Mar 2024 00:04:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d87cbac3603f5f9cc8f670321503490cdd836ce9f9ef6b67282bb1a345a1c5`  
		Last Modified: Wed, 13 Mar 2024 00:04:40 GMT  
		Size: 18.8 MB (18827638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3d0082bbbbb233d3a5f7a9764ce343e4ee82ce9a63cf4a499c1faca8a1642b`  
		Last Modified: Wed, 13 Mar 2024 00:04:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd9c9514577ca903a822b2ff6c778fa4ed25ef42b45513683006da76259bc3`  
		Last Modified: Wed, 13 Mar 2024 00:04:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7837c571d5ce97d9b73166d5894ad65eda4bec78b4bf9d096a11e0603d02581`  
		Last Modified: Wed, 13 Mar 2024 00:04:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5661e7a1f0f40578e416d9a85b3cfbf2ab251acfc07fed707a5e8aa8ab1abfb1`  
		Last Modified: Wed, 13 Mar 2024 00:04:40 GMT  
		Size: 19.1 MB (19074125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
