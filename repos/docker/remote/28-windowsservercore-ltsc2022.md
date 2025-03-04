## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:4ee5263d2d81ebbf176a71a917ba6cbbbbe0681759bf711f965dc2913df0fda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

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
