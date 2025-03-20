## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:edc51f855a48c810ed5c88c52f4d6fcf3aafd6eea01dd2107f860bbd070c03fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c7c548a07bcad5b0e9dbea8a658c263479421feaad27e8718220a49af3e23e5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974107962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a883aeb305eb2a99cd9e8dc7c53eac36a5f523e83fdf40b7a8e11bbc65dcb55d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Thu, 20 Mar 2025 17:47:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Mar 2025 17:47:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Mar 2025 17:47:58 GMT
ENV DOCKER_VERSION=28.0.2
# Thu, 20 Mar 2025 17:47:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.2.zip
# Thu, 20 Mar 2025 17:48:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Mar 2025 17:48:11 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 20 Mar 2025 17:48:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Thu, 20 Mar 2025 17:48:12 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Thu, 20 Mar 2025 17:48:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Mar 2025 17:48:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Thu, 20 Mar 2025 17:48:23 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Thu, 20 Mar 2025 17:48:24 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Thu, 20 Mar 2025 17:48:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f394b2d1b832f99af5b849371be079ac2ebbe2884f655a668ab64f6adf6667ac`  
		Last Modified: Thu, 20 Mar 2025 17:48:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488ab2077826cbdd1da89c5349051553d7416435c7b97bf3b8d102fb0f89f6e`  
		Last Modified: Thu, 20 Mar 2025 17:48:43 GMT  
		Size: 401.8 KB (401831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2be92d5e7c8e3d569c5afde4611f4e26e45d6563bf4450efce1cf347a8f8268`  
		Last Modified: Thu, 20 Mar 2025 17:48:41 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ba4440a9fa4b2a773ecc0e89bca22d52b6f172eb91771122ea53dbb3add7d`  
		Last Modified: Thu, 20 Mar 2025 17:48:41 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a6f97779946ec4d2c9839811be26754052fdfe1847ed95cdd53eb5aebed806`  
		Last Modified: Thu, 20 Mar 2025 17:48:43 GMT  
		Size: 19.9 MB (19898768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a217396953c724a918736bc3d75c70d1a604f1fb886ca897e09dcd7ff9ef40f`  
		Last Modified: Thu, 20 Mar 2025 17:48:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04b2847682eae94e56de56d9467f60c837bf636e0d7daf4da062042ea4dc284`  
		Last Modified: Thu, 20 Mar 2025 17:48:39 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a963c18b65324d6d53bf023f1c8a5366b94f405de787bf124da364708a4d56`  
		Last Modified: Thu, 20 Mar 2025 17:48:39 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623e5e02768cadfe2a63cec49b0b06bd0d9b346a63c149006c71ffea5dadbf80`  
		Last Modified: Thu, 20 Mar 2025 17:48:41 GMT  
		Size: 22.8 MB (22811196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc14b775451e8d6643fda82f6057da2d5e5905f180aad594b44b7810ba978d0`  
		Last Modified: Thu, 20 Mar 2025 17:48:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c17aa7782ac7496a824a480efec4642e8e127009a72f83467977a8ce007197`  
		Last Modified: Thu, 20 Mar 2025 17:48:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03281bd176bb405eb9872fe6ba7fd2cc13f053a9e3639b6f1f06d864a5c3cb45`  
		Last Modified: Thu, 20 Mar 2025 17:48:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600211295d58a8d37daaa231afcd076697c890ea538dc2bbd251de5aafad75b3`  
		Last Modified: Thu, 20 Mar 2025 17:48:42 GMT  
		Size: 22.3 MB (22336658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
