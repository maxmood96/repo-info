## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:95be95978dfc80495bc75a852dbd47fd10da7d9513a28375a9843cab054ff34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull docker@sha256:41dd3178edaf230cd35133e233fb4cc223b09f5bd747cd4fba7c07139b6affde
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2881548163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd1d03eab84d83aeb24d5bfc4ad5b840d7af0ab4949367e30f273d0e4434dbc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 04 Mar 2025 00:33:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 00:33:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Mar 2025 00:33:18 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 04 Mar 2025 00:33:18 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 04 Mar 2025 00:33:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 00:33:29 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Tue, 04 Mar 2025 00:33:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Tue, 04 Mar 2025 00:33:30 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Tue, 04 Mar 2025 00:33:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 00:33:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Tue, 04 Mar 2025 00:33:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Tue, 04 Mar 2025 00:33:40 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Tue, 04 Mar 2025 00:33:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873bde0a024bbb47d9adc1ca69132677619a46dc7ae53c2085247b309817b9c7`  
		Last Modified: Tue, 04 Mar 2025 00:33:54 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c1e902eeff054bdde47732eff8f1aa6de3bcc4c46e8596a0d2f15a3634bad9`  
		Last Modified: Tue, 04 Mar 2025 00:33:53 GMT  
		Size: 385.3 KB (385263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e439c5ce9e0f469c82308bb855e0a2e97b62e24b5494c295448ef98e8c7cf315`  
		Last Modified: Tue, 04 Mar 2025 00:33:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e2bf665f05e8ced4984518f264078fd5eb8a8b3a82f44ad96cf966269c7e5`  
		Last Modified: Tue, 04 Mar 2025 00:33:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6bf571ac7566cc24f2ae42f353e81365f35a13b3c702766b8d2334c737b`  
		Last Modified: Tue, 04 Mar 2025 00:33:54 GMT  
		Size: 19.9 MB (19854105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dc89784d0da0d2b33b177376efce93fea76dceab100093c458ced17523f7ad`  
		Last Modified: Tue, 04 Mar 2025 00:33:51 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c825a18719865c1e957072540a17e3b905d7d0a0fe8be07e9825b22fb844d5`  
		Last Modified: Tue, 04 Mar 2025 00:33:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1941ad73f062eabc4251387f75737cd4fcf24093f41051b81fbc915899601918`  
		Last Modified: Tue, 04 Mar 2025 00:33:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7616a3640f42b2255b3885440afacbab1710060fad80994d424fdcd7b9f551`  
		Last Modified: Tue, 04 Mar 2025 00:33:53 GMT  
		Size: 22.8 MB (22782025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23c983c6a83fcd4d457b73f39a356665b647e5cffb43b3b2aa120012c7995ce`  
		Last Modified: Tue, 04 Mar 2025 00:33:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078504c4afa8d66c6a77721a658a9c596b20fecb21cab428954af9f7b86e19c`  
		Last Modified: Tue, 04 Mar 2025 00:33:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793493f1d5b33ded086e3ec730f6b181065addc19927c6a13a183adbc36a0d63`  
		Last Modified: Tue, 04 Mar 2025 00:33:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14c8acab7d062ec4d157f6384519bb7993561c21b4cad44ff3c14dd0be2b557`  
		Last Modified: Tue, 04 Mar 2025 00:33:56 GMT  
		Size: 21.9 MB (21927492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
