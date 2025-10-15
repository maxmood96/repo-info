## `docker:29-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c62922c227c1d2159096defdcd268888cf7325e51692d07cc4dda16cc676245e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `docker:29-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull docker@sha256:c050c526521b8195849895cf6586f598bded352aa7bd3ae51ba4d682fe326605
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1555123541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72dfa16ddb0e81acb517855e4061bb5609883a42f71a2fddabc952d1a3c8592`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:41:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Oct 2025 20:41:24 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Tue, 14 Oct 2025 20:41:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.0.0-rc.1.zip
# Tue, 14 Oct 2025 20:41:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:41:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 20:41:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 14 Oct 2025 20:41:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 14 Oct 2025 20:41:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:41:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 20:41:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Tue, 14 Oct 2025 20:41:46 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Tue, 14 Oct 2025 20:41:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d69910297fad50ffc461b607623e7deea128c2f2ed652341ab8682223c1249b`  
		Last Modified: Tue, 14 Oct 2025 20:45:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150260de3b739792ce3018e4cca074fb52906942b90eca3f89509f562194c7b0`  
		Last Modified: Tue, 14 Oct 2025 20:45:20 GMT  
		Size: 354.8 KB (354812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40a14bb8a1b4eb1423f9318e00110c8d1a4ad55ac0df313b998042e07e87902`  
		Last Modified: Tue, 14 Oct 2025 20:45:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33472e9717eb17705a9d97f97697e31ec93971411ef956edf39b9583ddb08f3f`  
		Last Modified: Tue, 14 Oct 2025 20:45:19 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d95f3b6556394e43f85c9cf05ed5a73b6831d9b1df1443ef81518921250a95`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 20.0 MB (20048222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793e182cb02c36bd84da1b00dc881b7e037c73b807026149ffc83f5fd5dd7ff2`  
		Last Modified: Tue, 14 Oct 2025 20:45:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f025f8580adaf2905d811e02283fa421e936a4a8f1796990e8709f6a9b57001`  
		Last Modified: Tue, 14 Oct 2025 20:45:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba83a1e8b7394f6a8d1bbedafcbe73d7cc7e278c643d69c5187660fc3e3fbcf`  
		Last Modified: Tue, 14 Oct 2025 20:45:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d58d234dfd2386ed0b7e55f88d2cfa37449d0a1f0ca6d88fbd74c3f0f70986`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 23.1 MB (23146401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5703e3165d06c880fe572ccd167c1f9d607573ab6bc3c214be1c10c4d3697bc1`  
		Last Modified: Tue, 14 Oct 2025 20:45:20 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6af1ae30e3685ed308628ca4bb40587e68274a2cca35053c6dbfdf0697afc33`  
		Last Modified: Tue, 14 Oct 2025 20:45:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb44727b079091ac31704faa671b41008b3ff160acac13be5d87b7aeb72350a`  
		Last Modified: Tue, 14 Oct 2025 20:45:20 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb83eeccd639e2086b728e9ea2f36a0093ce32833ab5b89d3693650fa787742`  
		Last Modified: Tue, 14 Oct 2025 20:45:22 GMT  
		Size: 22.5 MB (22543253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
