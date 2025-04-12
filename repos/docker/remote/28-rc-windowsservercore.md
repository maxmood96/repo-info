## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:c6f9dc1b053964ee7df9335b088e0a01017f7b36da55861512249d614f7c0f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:c9f7620f8decd55000f891e4e530535f211fab505d804ca2c9968d5c4f561b07
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459626548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff798cb5fbda09302015d596f10cf5e7f2e78ce0bc5036d9092dc27a6f459fba`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Sat, 12 Apr 2025 00:54:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 12 Apr 2025 00:54:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 12 Apr 2025 00:54:23 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Sat, 12 Apr 2025 00:54:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Sat, 12 Apr 2025 00:54:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:54:35 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Sat, 12 Apr 2025 00:54:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Sat, 12 Apr 2025 00:54:36 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Sat, 12 Apr 2025 00:54:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:54:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Sat, 12 Apr 2025 00:54:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Sat, 12 Apr 2025 00:54:47 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Sat, 12 Apr 2025 00:54:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e52250079b1072cefccabf33ac9f9163153b024d66477389510eb9639d9dcd6`  
		Last Modified: Sat, 12 Apr 2025 00:55:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49569b0248bfc38217531f89c97d60357d5cd897cdf16ba9a5530e45b10ef042`  
		Last Modified: Sat, 12 Apr 2025 00:55:06 GMT  
		Size: 380.3 KB (380300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8289099d680405c097cd46f9710916bc245714d91e9052610d6efc9b6ef0c911`  
		Last Modified: Sat, 12 Apr 2025 00:55:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140ce2fcaa9abd913edcbab4e5d8ed1f63cabc72c94c23e2f997940af6cbc646`  
		Last Modified: Sat, 12 Apr 2025 00:55:04 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4feb188ba5231ee2f68507591497b0ef1a40a51d603e396ee07d75093578e3c0`  
		Last Modified: Sat, 12 Apr 2025 00:55:06 GMT  
		Size: 19.9 MB (19905126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7c01936c25ba3d98099115fa48a856499ffc9e8aee226b95275f7616be321`  
		Last Modified: Sat, 12 Apr 2025 00:55:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153c6c573782122ace3741fd08ecb37cb37bcd804d788001a3712f7dd9740cdf`  
		Last Modified: Sat, 12 Apr 2025 00:55:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3989683909d8a285a4a67a3820c62f3053a9ebee98a061e1b7b14fb6e8d13b52`  
		Last Modified: Sat, 12 Apr 2025 00:55:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a165aa650a57815627e1dd5229b3d5538763d59200a3bcd47fe06d135e1422e`  
		Last Modified: Sat, 12 Apr 2025 00:55:03 GMT  
		Size: 22.8 MB (22788485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898d1cb8d0886928182966aca90c541cc80ff244020b32be118f32bafe2a0450`  
		Last Modified: Sat, 12 Apr 2025 00:55:00 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52c212a2101e5db2300fc0e5582618675e29d70bafce336e871731828814f8c`  
		Last Modified: Sat, 12 Apr 2025 00:55:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94d700a72581ce491ebf7726df085c5635209c658cf9d8fb5f6a36eaa78acd0`  
		Last Modified: Sat, 12 Apr 2025 00:55:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d88cf1690aaf34daf7f62e68239198d2c83b057b88a353e7e8f478bce8f0f2`  
		Last Modified: Sat, 12 Apr 2025 00:55:03 GMT  
		Size: 21.9 MB (21861432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:305d453e9a9cc5fa7acbbbb054bc6afc4848810f5076574876e730274354557a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335896441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2beae110fd2f615f9707ebc9fb4f4c66d96dc1cc57d48bb82b557e919a30032d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Sat, 12 Apr 2025 00:58:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 12 Apr 2025 00:58:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 12 Apr 2025 00:58:51 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Sat, 12 Apr 2025 00:58:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Sat, 12 Apr 2025 00:59:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:59:04 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Sat, 12 Apr 2025 00:59:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Sat, 12 Apr 2025 00:59:06 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Sat, 12 Apr 2025 00:59:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:59:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Sat, 12 Apr 2025 00:59:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Sat, 12 Apr 2025 00:59:17 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Sat, 12 Apr 2025 00:59:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a8afa9b9eb85cfe6658f299154f9292627995660284ada8b3e74900ffae461`  
		Last Modified: Sat, 12 Apr 2025 00:59:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4da60f4cf6ce999567593e7ee53299430fc9a085aead0e93f775a62ce4d68e0`  
		Last Modified: Sat, 12 Apr 2025 00:59:30 GMT  
		Size: 367.7 KB (367668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16f2a0448f207d33dc3e38ef32a3660b251537fd16fa832c10b3307d14d63e8`  
		Last Modified: Sat, 12 Apr 2025 00:59:29 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71744e072086b943507a00133c27c6474b1ca73ee863efd20d83e3dae089cd3`  
		Last Modified: Sat, 12 Apr 2025 00:59:29 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b3718a498e81e5638cb021774fffcda82ab8a37fa4a4c1b30bdbaea2821fb6`  
		Last Modified: Sat, 12 Apr 2025 00:59:30 GMT  
		Size: 19.9 MB (19893083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d20315fb2ce13cd5baeb22f38f713e6bd14986278c570e402c512ddf32a9f73`  
		Last Modified: Sat, 12 Apr 2025 00:59:28 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b429eccf29adfdb2be8fc36466956b15b32e4da79f76f0664076eb41fb6f6b5`  
		Last Modified: Sat, 12 Apr 2025 00:59:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb0d19f43d5e5a91be1b8d46f1bc660d80fb8954546226a9cfcaeae4e309381`  
		Last Modified: Sat, 12 Apr 2025 00:59:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c5fd971e7bc607f44d63d08cfe1ae36c5db194d30319d0fd30aa2d9c5396b8`  
		Last Modified: Sat, 12 Apr 2025 00:59:30 GMT  
		Size: 22.8 MB (22777459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99afbe11bc4ced1a83405e0bbfae61e8ece43524338d9c12b7a3631d3754569`  
		Last Modified: Sat, 12 Apr 2025 00:59:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1639e41d16ef57344f129699c5658dcad2ba26f9a99f44daa6c0c7a3bb4e4fc9`  
		Last Modified: Sat, 12 Apr 2025 00:59:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b547add0afd06dbf0d78a22d6087e5548085e599e758982703b0b9575401cd`  
		Last Modified: Sat, 12 Apr 2025 00:59:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4246045890cde263daa1b7bdfb7ee4503e7838fac90a59a7621702a50720ee`  
		Last Modified: Sat, 12 Apr 2025 00:59:30 GMT  
		Size: 21.9 MB (21850911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:d795fc8194cd50c7b7262a40166c89261c1164cb9c46132d2585c3c7cda3530c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227543848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5c044a74f87fa926d78667ef770793d5970fd9744fedffcec866cad451d7d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Sat, 12 Apr 2025 00:52:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 12 Apr 2025 00:52:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 12 Apr 2025 00:52:40 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Sat, 12 Apr 2025 00:52:41 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Sat, 12 Apr 2025 00:52:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:52:52 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Sat, 12 Apr 2025 00:52:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Sat, 12 Apr 2025 00:52:53 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Sat, 12 Apr 2025 00:53:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:53:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Sat, 12 Apr 2025 00:53:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Sat, 12 Apr 2025 00:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Sat, 12 Apr 2025 00:53:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abdb6f82b099e8ff452eaeca9fc5249b213a8309e280c8a338dbbb921e0890f`  
		Last Modified: Sat, 12 Apr 2025 00:53:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05679a57590b05908261d4a952156d93de5f78c263841bf401c0fec5369a28df`  
		Last Modified: Sat, 12 Apr 2025 00:53:21 GMT  
		Size: 343.0 KB (342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7203f70c27dcc86d5754accefa55500005a70208301c4745960a7a1c2e788a5`  
		Last Modified: Sat, 12 Apr 2025 00:53:20 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61032f1f6d05f123f680206cea1db3ed81188dc3712b86aff454501c7c431776`  
		Last Modified: Sat, 12 Apr 2025 00:53:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c880aecd7a1808bdbb1eb42f51c42b0094f81ab166d52716b6c9aff694e47d`  
		Last Modified: Sat, 12 Apr 2025 00:53:21 GMT  
		Size: 19.9 MB (19874753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4113a3249a1f710c46ebf5f545bd95fba42456a10cd8c3a467e08499603eabb`  
		Last Modified: Sat, 12 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0403fb18519c614b2094b3bd6fbd9d08a17a40dd65c4950a60f3c50f752570`  
		Last Modified: Sat, 12 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5699130cc7e0a5cb6a750577c87b6f85be557a54431f4adec3355b7024423dc`  
		Last Modified: Sat, 12 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958221aa46dc9274c3b0ed01689c49cf1f7e34015d7e7c273503d7f4c4b11bf`  
		Last Modified: Sat, 12 Apr 2025 00:53:19 GMT  
		Size: 22.8 MB (22759967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d305a1ffced5869ab11321142265499b844c366c020ebacbf4a8598970fb393`  
		Last Modified: Sat, 12 Apr 2025 00:53:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b619282481058ce6f9807e615ac17a24c3600c7f2cdd96e0bdf620f0fa1eae99`  
		Last Modified: Sat, 12 Apr 2025 00:53:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a3b7f242b9d0ff6de6adca6aa9955aa14e21b80a78017211ff318cad70df96`  
		Last Modified: Sat, 12 Apr 2025 00:53:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e6a4883bb0926852a400f48818d6569f8bd70a63b8e687c7c08d636817b579`  
		Last Modified: Sat, 12 Apr 2025 00:53:19 GMT  
		Size: 21.8 MB (21828588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
