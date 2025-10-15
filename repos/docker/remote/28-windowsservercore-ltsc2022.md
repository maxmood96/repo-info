## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c1f0d7b63abbea89280e685f7f4fa5a1c4bcfee4a22640786a569c63374c09ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull docker@sha256:913445261809414daf954f1029c70a8f303a077840348b3f614fac2fae39602a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1555842479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16176a4969edf59085083f2f7367f72c179a8cc3935a8bb631cece76fe64cef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:40:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:41:15 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Oct 2025 20:41:16 GMT
ENV DOCKER_VERSION=28.5.1
# Tue, 14 Oct 2025 20:41:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Tue, 14 Oct 2025 20:41:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:41:28 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 20:41:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 14 Oct 2025 20:41:29 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 14 Oct 2025 20:41:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:41:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 20:41:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Tue, 14 Oct 2025 20:41:39 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Tue, 14 Oct 2025 20:41:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fbaa2338b5f21199cd9a50079b2aa9af297c6a713f9ac529a66776518157d9`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eff323dd65eb32198858dde0b16e28b7aefe9698993fa594e49eba318f58d96`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 349.6 KB (349627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075c2fd8a2345a97904c61c867a7b6d4faa35dddeddcce8eea49242bbc4dd0d4`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1bd05bb447e940a4303f9917f681461b654eb6cb47d7496f362960dbb89b80`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3867486207a7fa7a63af0a0ca07da8ed19470b4deeda50041c8111d4dfcaa`  
		Last Modified: Tue, 14 Oct 2025 20:45:25 GMT  
		Size: 20.8 MB (20765170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e436d9a7b89ff746815aa986a8634acc277263f0a703746790fa97b0198aa6`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933c2b5695d674e811f2855438ee3db8421d4101a390551c8eb21725f7b9e5b`  
		Last Modified: Tue, 14 Oct 2025 20:45:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6187d4a7b498720b8a2c9d22a8719092f670c36a7ca3dd37618c7f30e2f194ce`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32830bfe7b040130b8adb8d070e68b6f61364d9f49cf754b69b1353a388f6fa9`  
		Last Modified: Tue, 14 Oct 2025 20:45:25 GMT  
		Size: 23.2 MB (23150370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfe06637960c88ae10b5df172b5a98def2e5e84f7e6b475465d36621a55e581`  
		Last Modified: Tue, 14 Oct 2025 20:45:22 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641517ced187c25b6df36c62af40ddc72ad9cb85655ac087ddca7202e11186e7`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fe8610bbf4cc53687468c96922c04064ac5cab43c1bce19a1f49ddfe12432f`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cd7310394894b5833c4730a0c036c86e7620be3480a400b80e4891678de811`  
		Last Modified: Tue, 14 Oct 2025 20:45:25 GMT  
		Size: 22.5 MB (22546364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
