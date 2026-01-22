## `docker:rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5d6f5de54f670fd9749a7f266e9d8b0dca7321cd6e5323bed8f79decca35c6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:ef9a6f86137ac9b5c8dfaa618fa9cd2720f704a09d5695c3c8c0ad1dc4ef78fc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1551002197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79d1a6db077c9649349e4be2f406a17571abec5a58e4b3549b5f910f87c3f3a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 20 Jan 2026 18:49:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 19:08:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 20 Jan 2026 19:08:37 GMT
ENV DOCKER_VERSION=29.2.0-rc.2
# Tue, 20 Jan 2026 19:08:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.2.0-rc.2.zip
# Tue, 20 Jan 2026 19:08:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 20 Jan 2026 19:08:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 20 Jan 2026 19:08:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 20 Jan 2026 19:08:47 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 20 Jan 2026 19:08:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 20 Jan 2026 19:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Tue, 20 Jan 2026 19:08:56 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Tue, 20 Jan 2026 19:08:57 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Tue, 20 Jan 2026 19:09:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea386d3f231cd51d65f90cee89c9ac8d16f1a31939e14e985fa6a726457dbcd`  
		Last Modified: Tue, 20 Jan 2026 19:01:31 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccac9a5a94f24745425e5b719e77c4034890e1e335cde63fbc6d8811ded9a89`  
		Last Modified: Tue, 20 Jan 2026 19:09:12 GMT  
		Size: 390.6 KB (390622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f5c476b39d1eae37fe8ba15e7e8401ae3737ee2ba706ad3a4392ded90081a2`  
		Last Modified: Tue, 20 Jan 2026 19:09:23 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d1b3384ee1603a36aeb6e70de845b2ed50db055f4a77c62474391a86ec6ff1`  
		Last Modified: Tue, 20 Jan 2026 19:09:23 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113cf18d56e8f2b3875ae45a37efe9420240cc2b3b3070864a9998877748c1c5`  
		Last Modified: Tue, 20 Jan 2026 19:09:30 GMT  
		Size: 19.4 MB (19444537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c94843f5304751214cc125c173bfaebdcb07d89ecaf32d02415dfbbf26cbd0f`  
		Last Modified: Tue, 20 Jan 2026 21:11:03 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4461235ebe7afa09a00b3c2cc9c9d9c30b9aa94758d92c7cfe412bd4688b32`  
		Last Modified: Tue, 20 Jan 2026 19:09:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac225a0f9162c87c0d77e39222c6184049a7be62ebf1774e8fd16b176700569`  
		Last Modified: Tue, 20 Jan 2026 21:11:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d1a9fe2db4faec63e3aa3d3c22beda4d4a320a3ff3c379f3989ab9e705323d`  
		Last Modified: Tue, 20 Jan 2026 19:09:27 GMT  
		Size: 23.9 MB (23936009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe6183709cbb23778e6b547e25a6e2157242c066d41b3e4f3f5d0deda8d3606`  
		Last Modified: Tue, 20 Jan 2026 19:09:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7cbdac2c3c966e383aace6c50d7dd8cbed549a748094dcbcc424acf4358c4b`  
		Last Modified: Tue, 20 Jan 2026 19:09:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937cfa7610ff4a5f402397351ba0c2f50000dc61826321664093ffd6bd7ffad1`  
		Last Modified: Tue, 20 Jan 2026 19:09:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26da30edd31daff6584c5f1df2041f2177b23a1cbb0263173405dda011836df6`  
		Last Modified: Tue, 20 Jan 2026 19:09:23 GMT  
		Size: 11.5 MB (11458960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
