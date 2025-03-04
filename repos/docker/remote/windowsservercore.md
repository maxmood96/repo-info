## `docker:windowsservercore`

```console
$ docker pull docker@sha256:06c3c785f49c68bcaf768d3133c35e71b3b87ab06655ef6223fe936bc1e10593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3194; amd64

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

### `docker:windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:87c9cf1a40510750ae9f95604b38cd9936d4fc17bc27863899635c499fd1011e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328592408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38cf5da076f826f3f9ba54f56238210d3108f8c5b3f77d353d100395556c815`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 04 Mar 2025 00:29:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 00:31:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Mar 2025 00:31:04 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 04 Mar 2025 00:31:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 04 Mar 2025 00:31:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 00:31:31 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Tue, 04 Mar 2025 00:31:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Tue, 04 Mar 2025 00:31:33 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Tue, 04 Mar 2025 00:31:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 00:31:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Tue, 04 Mar 2025 00:31:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Tue, 04 Mar 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Tue, 04 Mar 2025 00:32:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38469cbea60448a5af74968ad0beb667c1221cdc4edd6a1061978dc95a7cff0`  
		Last Modified: Tue, 04 Mar 2025 00:32:09 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b57d292c399353783829c29aa53178662943f31e834aecd9812aaf03f4a92e`  
		Last Modified: Tue, 04 Mar 2025 00:32:08 GMT  
		Size: 367.5 KB (367496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7ed3c23849f5122202399daefb829190af7fd5734586906a61d470f159551f`  
		Last Modified: Tue, 04 Mar 2025 00:32:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec46e2d0224bfaf68e10d12e9a3218f1089e907aa02d6e2f8766c01a907e526`  
		Last Modified: Tue, 04 Mar 2025 00:32:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1770d749e047c629298c7ceb401e6a2d06cd90f2013da57c2f15d9f62616aa`  
		Last Modified: Tue, 04 Mar 2025 00:32:10 GMT  
		Size: 19.8 MB (19786124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e6b4717889172a0084e293706992b74518c3b29c1fd08805c6bedd308e3f7b`  
		Last Modified: Tue, 04 Mar 2025 00:32:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cf2d5feae8d7ab4794a14a55a62fbf43c346a7df1f9b142143a297848955ac`  
		Last Modified: Tue, 04 Mar 2025 00:32:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f14794a6401ddb6221e4518d691475959ff2eb4bcd23c3bde04a57a0e185c6`  
		Last Modified: Tue, 04 Mar 2025 00:32:06 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0757d9761a4806161c8730bfb74e040a69717925b2b9d9c30cd47209ee9a392`  
		Last Modified: Tue, 04 Mar 2025 00:32:08 GMT  
		Size: 22.7 MB (22712918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad49221c1cc0b321b3bdd6358f52b005ed38076c44484d3935e9454314164c11`  
		Last Modified: Tue, 04 Mar 2025 00:32:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bd5371f0ff8b7b9ff0ca78fbd9a032f17700f57995244170e15654caf3f217`  
		Last Modified: Tue, 04 Mar 2025 00:32:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e15b6b49e57f7a9d788295ca15fccb1f3cda809041b7e2e06a4442533a01e5d`  
		Last Modified: Tue, 04 Mar 2025 00:32:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23089c7ad7952e635e5c9304216876e6fbf911894f8b8287e03265357e523254`  
		Last Modified: Tue, 04 Mar 2025 00:32:09 GMT  
		Size: 21.9 MB (21856166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:6215fbddfc9bd8b0f2fa8848d10b20343bcd80973df38a04ce86b70ec5a49158
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201704185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ac41bac3a6700283fb1b5c8ba96fb1ee9ab3d2b50e32dcf2d5289419485866`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 04 Mar 2025 00:29:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 00:31:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Mar 2025 00:31:08 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 04 Mar 2025 00:31:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 04 Mar 2025 00:31:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 00:31:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Tue, 04 Mar 2025 00:31:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Tue, 04 Mar 2025 00:31:32 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Tue, 04 Mar 2025 00:31:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 00:31:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Tue, 04 Mar 2025 00:31:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Tue, 04 Mar 2025 00:31:47 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Tue, 04 Mar 2025 00:32:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3af89ed9b680338394cd1f5059e6758d8597c9c6ac6b16d4ad696cb310bad3`  
		Last Modified: Tue, 04 Mar 2025 00:32:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f6e23ff07757fe98060214de4fd60d74443c52859f91b727497a856e26c203`  
		Last Modified: Tue, 04 Mar 2025 00:32:09 GMT  
		Size: 342.9 KB (342858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8978879be738db88294accb56bd0af05dc8505e9be9f7c1e59288b53f50de5`  
		Last Modified: Tue, 04 Mar 2025 00:32:08 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4757fc10b66e5f44d973de3ddd167e0e77f58c723997b363e9509d020fa6d733`  
		Last Modified: Tue, 04 Mar 2025 00:32:08 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68558b44767feea7f33c025430360d12559b0e67ecd7636ab8abbdd1396ac36`  
		Last Modified: Tue, 04 Mar 2025 00:32:10 GMT  
		Size: 19.8 MB (19815502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c03b7c8233cc95c7e616979d3e05bfbcc93a93f6f1a4bed46a87527738357b9`  
		Last Modified: Tue, 04 Mar 2025 00:32:07 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c102eeddd47a4d416dcbbe3c9890ce8b2d39190b0824f51978c630affed65c7`  
		Last Modified: Tue, 04 Mar 2025 00:32:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dce39f71d8c354ef22c784774eede444e904cdbbb1e9eb01cd2a841ea964c3`  
		Last Modified: Tue, 04 Mar 2025 00:32:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc63e58f0e5526c149785b94e1f319376b9ba342abb51c7df51549fd160881c2`  
		Last Modified: Tue, 04 Mar 2025 00:32:09 GMT  
		Size: 22.7 MB (22743192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3a9c82c469b6cc58d34f26fb81d336085ebfe8f455a11cb8c9663e5af5af37`  
		Last Modified: Tue, 04 Mar 2025 00:32:06 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cb29e29d02b86b76a7e415b688aae265f608dd051be0ef227a75b13996044c`  
		Last Modified: Tue, 04 Mar 2025 00:32:06 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f05660b945955f4b3777b6411a44c39a59cb0a63413562c1f1f1485d75526ff`  
		Last Modified: Tue, 04 Mar 2025 00:32:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e55ee660ed4b042ef36ab8dc7503a3ba66da4972da69364a70ec4fc8e5eec09`  
		Last Modified: Tue, 04 Mar 2025 00:32:09 GMT  
		Size: 21.9 MB (21882103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
