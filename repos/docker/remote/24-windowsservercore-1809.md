## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:d1401e27fb9c14e8e40a8433491da3632a4f395fca5c9808521e2432f13460bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:9bc3a7c59feacbde651b62ee7c249c0e73c56a6fd3deac23e47de80b5be2c2dd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2124813163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268bd4740bc0c06eb785e243c685e604c6a9745bd134bb9b471d66f16959477d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Fri, 26 Jan 2024 01:49:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jan 2024 01:49:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 26 Jan 2024 01:49:51 GMT
ENV DOCKER_VERSION=24.0.8
# Fri, 26 Jan 2024 01:49:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.8.zip
# Fri, 26 Jan 2024 01:50:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 26 Jan 2024 01:50:19 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 26 Jan 2024 01:50:19 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 26 Jan 2024 01:50:19 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 26 Jan 2024 01:50:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 26 Jan 2024 01:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Fri, 26 Jan 2024 01:50:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-windows-x86_64.exe
# Fri, 26 Jan 2024 01:50:47 GMT
ENV DOCKER_COMPOSE_SHA256=107586a56c0efb53cdd164f8de2c06d9737f4e142c80b6d7d9f5aa2be956425e
# Fri, 26 Jan 2024 01:51:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9f28841efdb3c387d3563654f5ff589e0b000dfa79914cc191d786bb45d5fb`  
		Last Modified: Fri, 26 Jan 2024 01:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9feb90f6af1f7c50c8ca3233b18a6a511ab3db77ad3ae89a764f09370aba235c`  
		Last Modified: Fri, 26 Jan 2024 01:51:21 GMT  
		Size: 493.5 KB (493478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991b0d7fe787cf53e402f3c6b5a36b012c24b730504ee78c48cd40e9be4e154e`  
		Last Modified: Fri, 26 Jan 2024 01:51:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fe7a5e6e101925ae2cc36189a22f32ae4a06e253c041c02b90707c44d61032`  
		Last Modified: Fri, 26 Jan 2024 01:51:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2244ad432c105b73c9885eabc22fa2b0ad3195e33405a1b0068756770a675d4a`  
		Last Modified: Fri, 26 Jan 2024 01:51:20 GMT  
		Size: 17.5 MB (17536844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6ceeb84b3ecbe91a3d0521d781526764afd110b3ffa23729ae4d310ff94e13`  
		Last Modified: Fri, 26 Jan 2024 01:51:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f298afb96a9eb947be5dfe03fe488843a4e7de7b59b83d87b0ef8295ef330a9`  
		Last Modified: Fri, 26 Jan 2024 01:51:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb285d17087b0dbedc30a54398c6df11dcb6e3418d2e728cb369b260a8deb15`  
		Last Modified: Fri, 26 Jan 2024 01:51:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1e6b483d9fdd2dcdba0664360bde8c2fc2d769bead4ac255d3ba7c1cf2e2d`  
		Last Modified: Fri, 26 Jan 2024 01:51:18 GMT  
		Size: 18.0 MB (18020451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2573ce6169f591c6a794d5548e7b3a0830f24ba591b0e8340b7256d7a2b5a3`  
		Last Modified: Fri, 26 Jan 2024 01:51:15 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c4b5e2f7ff5c5a4b0ee7f67f1b46266f77fcc5f1e351a294c1f0e77d7abc3`  
		Last Modified: Fri, 26 Jan 2024 01:51:15 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaa586ad23595b818c6f646b1281fa40db8e9d16776dc882dc9f371fe2fea3e`  
		Last Modified: Fri, 26 Jan 2024 01:51:15 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce48f58371ebe8ed75c98970fc155e14ec4079a66f3b1fcd3ba0c2783a528fcc`  
		Last Modified: Fri, 26 Jan 2024 01:51:18 GMT  
		Size: 19.0 MB (19028238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
