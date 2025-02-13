## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:ba99c1ecdb555da3c877be84a95f838a5f3406e78af8970711aff866986f8fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:27-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:149dd640f3089d0e7f8ff3ccc2b60dd0f4bf5791b394d09a6fd5e17275fca8a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2562911644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a082621c966dad3f864a94e22e8f6fb89385039e13e3750730f8bb6c588e7f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 12 Feb 2025 23:30:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Feb 2025 23:31:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Feb 2025 23:31:01 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 12 Feb 2025 23:31:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Wed, 12 Feb 2025 23:31:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 23:31:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 12 Feb 2025 23:31:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Wed, 12 Feb 2025 23:31:13 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Wed, 12 Feb 2025 23:31:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 23:31:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 12 Feb 2025 23:31:23 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Wed, 12 Feb 2025 23:31:23 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Wed, 12 Feb 2025 23:31:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8bc940741c9c000546ed9582af6e711480501d6019de310dade561210b0b3d`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499c1302a799387db657f1ac455600db74f75a8f576d2a04286ff818a2dd7b17`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 382.7 KB (382706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198e7ab21608ce1156039bbcacd713c6b4a2ae02751fe8750e4c6e5fdd989c1`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2212cbe636322f7066ea13750e5fe827e0e79f7aa2af47058a687fd22cf59176`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f494ca76ae9a381da0cca82a092a0eed639efdfd55778c3ef20b2a543b384d`  
		Last Modified: Thu, 13 Feb 2025 03:08:33 GMT  
		Size: 19.2 MB (19200319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f021a357953651beb64ee44c8c257040dc06d5cf904b02fe5b119a66e67d50`  
		Last Modified: Thu, 13 Feb 2025 03:08:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a09fde216168e8fd5d13a27ebb643203c287103ba5f73a5134f6825349400`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d38789705c4c430eef8ebcae23013354c2883442be2b029c89f945cbeca7c`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3912df5f76256fb27ed4327333be19d1a10dceb604ab330396ba80aebccda8d`  
		Last Modified: Thu, 13 Feb 2025 03:08:34 GMT  
		Size: 21.2 MB (21177018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003b0d96bed2919bfa7f464e619968a9e9f7c389904a83054b55668295fa071f`  
		Last Modified: Thu, 13 Feb 2025 03:08:31 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc6f0078ab732aae5f171aa58352317d929acfb91af839892781c09cf58791`  
		Last Modified: Thu, 13 Feb 2025 03:08:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7d87354fe1203a288b123b468d2e4f0086fc24206611d36deb75aabbaf69db`  
		Last Modified: Thu, 13 Feb 2025 03:08:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6301011ea44a308e7dc78e5e4b749be4eae2aada5da22695be7d2eee34d7d3e6`  
		Last Modified: Thu, 13 Feb 2025 03:08:34 GMT  
		Size: 21.9 MB (21862260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:69c9c24a7d3a41d0d4f04b2b1e4dbebeecc3fb038862ae34c3061cdfd2b21f0a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2326425187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797d4c480f72befbeebd3f1f87f8e655aba3dd1e194488e978b1c9adaab979d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:37:14 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 13 Feb 2025 00:37:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 13 Feb 2025 00:37:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:37:24 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 13 Feb 2025 00:37:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 13 Feb 2025 00:37:26 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 13 Feb 2025 00:37:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:37:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 13 Feb 2025 00:37:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 13 Feb 2025 00:37:36 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 13 Feb 2025 00:37:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992eb919bfa3347623a028ed6de3b4fce1dd8a0c2e2fa2744cad19a4ec0a59c`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6e0f5c222d03817e5d295f65e80bdef9a101af7ea64c84b1f22d794928e604`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 379.4 KB (379431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94bfa520c1c0155fbbaa7b673abaef27b67360589405c30b553f788be0bf661`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64493e8af281d85e0ad07c06bc6f447f91594021c00c5edac80311f36e114e3f`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4936d0712c9c06f97a4ecd322941b144de4e8df36ff90601f2ed79b6772d5860`  
		Last Modified: Thu, 13 Feb 2025 03:08:38 GMT  
		Size: 19.2 MB (19180289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d91da65ae6a544995fef5dc2dc81d4899f96f5884966b1a5faea6ee4b2e089f`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c543db2761641064486d54ab2fcec1d289b1500ae626aeb18fe55acd42e75e6`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056f548d500d55c8ea038d74125a03a742fde71107831656584d99b1dfdfa21a`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95754f6197562b6029971291dba5876bd0c5c5087b2a7c55804825205fbcc7d9`  
		Last Modified: Thu, 13 Feb 2025 03:08:31 GMT  
		Size: 21.2 MB (21156399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e046cdfbfdab2425a973be14b185777514cd38ce81fb560b048f597958d6f081`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466974ceb7189221b636928a98e8953a7d84c77749eb7a2a6c8b20265f261bf1`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1cc51cf695b8c69da4ae14c0dc555e2026e7fbd54521e07835d08ea3df07c6`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcededb76ab914824aec331d4470d61555a983eb5848d248c11418809687d62e`  
		Last Modified: Thu, 13 Feb 2025 03:08:34 GMT  
		Size: 21.8 MB (21839476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:dcf28587862b66f11c9152f0f07aba6549e6fc69ae5692187d8b81fd9632e2ae
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199331794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abaa563d895b666255230f87f1e8fe38b9731565871f357c861f66dbf2417f81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:30:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:30:33 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 13 Feb 2025 00:30:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 13 Feb 2025 00:30:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:30:43 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 13 Feb 2025 00:30:44 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 13 Feb 2025 00:30:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:30:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 13 Feb 2025 00:30:55 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 13 Feb 2025 00:30:55 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 13 Feb 2025 00:31:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ddec09ce130898b858d868d863c38d0a59ad02d30317040c713bbcad470d7b`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b18610111d087a831e8f8ee56836d6b68057470111cd634df6fbd5f7eefe8`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 333.7 KB (333660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3085b676e07491e9c1eea56a888e0405ddf3aff207f0f8eee75b2201937c22`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e439965d4bb61c02ec64eb94d7cfe644ef8c059133cbcf266573b59d5ddfe7`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6714307851c701c6dbe14d976b4ed71dfa150ca4c45c6e0c9a64854f7d76ba86`  
		Last Modified: Thu, 13 Feb 2025 03:08:36 GMT  
		Size: 19.1 MB (19148895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e81914763a0ae26bccf9728612de0fc76384393d1a179879e256af8cce9b09`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c219e06bfe9ca604cbde640314b8068a4d0feeaccbafd5f1857f31f72fa57`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcc26bb2920298fb60914141b02f623bd84c3d2e8e5f800678259f8f46ada5e`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622ffa3a23b3c72d93e7700d2d2a621f73d09b371913c49a4b6bb7a03836df1b`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 21.1 MB (21125839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda2cb85d7567448d09f5063d50876774b50476e783a6228538b975f31a4c2d9`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2a862ff7c9cef485f0c7554c1dea61fe84ec9cd43825c10ee846c057f7e319`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a00d05b58e6f9ed3e53e37132919f43c22ee3a79989ef8ca2be0428296cf49`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50ddba2f9c71876169789e635349f235b35dfaf2447e05d22566cc343498165`  
		Last Modified: Thu, 13 Feb 2025 03:08:32 GMT  
		Size: 21.8 MB (21802955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
