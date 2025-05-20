## `docker:rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:e393cad45f157bf2c3187fffc7e1ffe0aade707cde632220ab449439f4183bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:f9f79b35f18b56395b8b360bf83addbac5b1da496de46fa7f2b765074c42bef8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459346774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2014fd10b36c39ef11c3bbf5020eac8fac30dd7c36688daef0dbf5287493fbab`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 22:03:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:04:04 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:04:05 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Tue, 15 Apr 2025 22:04:06 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Tue, 15 Apr 2025 22:04:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:04:20 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:04:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:04:23 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:04:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:04:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:04:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:04:37 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:04:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Thu, 08 May 2025 17:36:24 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91183b2a88e148dca95fdc63ddf9242f11339ce9038bd05fd528a47f77ebcbb5`  
		Last Modified: Fri, 09 May 2025 06:20:21 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b08db622f6ed809d3398f0012786f8331a4c270647bee3ea71256cd06ec4415`  
		Last Modified: Fri, 09 May 2025 06:20:21 GMT  
		Size: 414.6 KB (414611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf28ff6d5ae985d808794c1797af3a827c47a9e541a73ea5195300032674e57f`  
		Last Modified: Fri, 09 May 2025 06:20:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd680cf57a45b235b43b6e47acfe000305cf88ca6337b8b766182d1fd93473da`  
		Last Modified: Fri, 09 May 2025 06:20:21 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca77b3effd4271362131982258dca41b2b7f7210ad86ff87e091bdd69bfbc31`  
		Last Modified: Fri, 16 May 2025 17:11:47 GMT  
		Size: 19.9 MB (19936516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc439e7b5dcd89838451a4fb16687f89932c9772da7dc822339859ae6c63bad`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee2c50089d08c3e89bd35fb8dc35a8a6b3f02a800ffb840228f03cc8b50e8ec`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23738aa6b5ed990f136e101c0049f0d75505f0877824c4cbb24d45494428eedf`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea7c93aa52117155d66f23e00e3fde9fe191d2f42972ca04f132f95f5206f50`  
		Last Modified: Fri, 16 May 2025 17:10:17 GMT  
		Size: 22.4 MB (22411622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0980586e177a08e20fc55ad3763a03121f648b8838c1763921f2283558243a04`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16bdc99cc42be98ae3e10f4a6b0b00f86f4017a0a4b6c6fe0e7b2137fe06ca9`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81ec503ae82985d6d43e418959a3196432a5439666828b5016b0cb8f1903fba`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3fdef74f545d913c5819a1c9d01e8984a5b6a690b2c6e00c6773ea0e9d6cfc`  
		Last Modified: Fri, 16 May 2025 17:09:20 GMT  
		Size: 21.9 MB (21892647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
