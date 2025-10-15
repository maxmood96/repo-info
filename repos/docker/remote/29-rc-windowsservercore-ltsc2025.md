## `docker:29-rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:4d14c2517cdd1a8c15f5dc3f9fbe4cf4d25db3ef9a6bf31c6a48ea69754ed825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `docker:29-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull docker@sha256:64ddc004a2fa0bad3e2897238a2d61b014a471f25bd4f779979b38af5b2821c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286541030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eebe88dfff624c5f4f00202486ac869a93cff870827f94fc395dd2277dcbbd4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Oct 2025 20:43:47 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Tue, 14 Oct 2025 20:43:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.0.0-rc.1.zip
# Tue, 14 Oct 2025 20:43:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:43:57 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 20:43:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 14 Oct 2025 20:43:58 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 14 Oct 2025 20:44:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:44:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 20:44:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Tue, 14 Oct 2025 20:44:06 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Tue, 14 Oct 2025 20:44:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b31ef2acd9573fa311450133976eaea07e0ccfd74f3de24d672c7bf465eba24`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda084d1a958ebf4512ae43e2bafe7f4730de69d98d47316b0b6761527f131e7`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 343.9 KB (343918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2840c27852fa0d84cecf8b6482725ffea44bf4d5a6265636880af118e2d364c8`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aa055df8cdf3d599b2dfb9dd8d37a8f74e4272dfef7f3aed78b721c2412cce`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a22d7045e5dd04a91d34ef11f9ff814cf02dbac1ce9771525aea43dfc0a7b02`  
		Last Modified: Tue, 14 Oct 2025 20:51:57 GMT  
		Size: 20.0 MB (20037714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9499f137aa6a14f6b888acc1a5feb978f14989939de341321f173b23f1989c`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8ddde69192b3fcacbf403b401b83710e61302eddc5d0332b7b032e3422e5bf`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54825960fb319f1a6ce0ce19f33b1ee7ad255fa729542af519160fe795e9ef95`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3276b825ae2f4660615b8547237bb2124c52fc558f75bdd0843bb66a00201e11`  
		Last Modified: Tue, 14 Oct 2025 20:51:56 GMT  
		Size: 23.1 MB (23134355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9aa360df8d049ae41febeb07f10574547d45d379783f9aae87e3bbb6c5582b4`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fcbba6adc95ca39b3c7da92b957366caf97226ad99c3e9a062759574f28467`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f049b84548e49195f45e1d1fe6c48bf6ee5fe164c17d32e193b598843e2e86d`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e8797f1b9454d03f533aa1af5c20e84edb9b6395bc1350d8632918dd44730b`  
		Last Modified: Tue, 14 Oct 2025 20:52:00 GMT  
		Size: 22.5 MB (22532779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
