## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:5c6b1e5297326c477cb969604e14acda8c785b41cd0942919a06a570ad2ff2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:836613ee1e4bd307cc75483e23873e078560e758b35abe3bfeea438857214312
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495540845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa2372696568d2a222b492d9f0b0a18aa52e9a117a6dae29dc4783a69a6b174`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 21 May 2025 18:56:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 May 2025 18:56:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 21 May 2025 18:56:19 GMT
ENV DOCKER_VERSION=28.1.1
# Wed, 21 May 2025 18:56:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Wed, 21 May 2025 18:56:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:56:30 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 18:56:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Wed, 21 May 2025 18:56:32 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Wed, 21 May 2025 18:56:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:56:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 18:56:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Wed, 21 May 2025 18:56:44 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Wed, 21 May 2025 18:56:54 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e951a40e97c39bc9d9a3cddd780cbf926e23804e0bfd59e4e7ce8e3364ead9f`  
		Last Modified: Wed, 21 May 2025 18:57:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66b4089ac6d5e81bbd29f09f93f2495810ce8090f75888d0e0b1474d9fb10a8`  
		Last Modified: Wed, 21 May 2025 18:57:06 GMT  
		Size: 389.0 KB (389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b7dcdbd4722d18849effb2589f3ffe7e2ed45744ea4d47faedbea19f04eff0`  
		Last Modified: Wed, 21 May 2025 18:57:05 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ce1b419877963cb223ad397f2049df1898c06144e71ee780465d0f14d02900`  
		Last Modified: Wed, 21 May 2025 18:57:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5418fe79cb98d70dd16ea96a1626a8739f622eaa7f4c99d28d301b76469c19`  
		Last Modified: Wed, 21 May 2025 18:57:06 GMT  
		Size: 19.9 MB (19920585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6a43be893f0d4bb98570912b16bd8b062f6d0fea963ca9cdd2b4ce1df46d8f`  
		Last Modified: Wed, 21 May 2025 18:57:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09bc7dd13a8b2b29b9da435b8ad6299ea43c6e51a4062ac8dd61bdb4f85392d`  
		Last Modified: Wed, 21 May 2025 18:57:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ca3c32c67f85c7f6e5796913b1776cd560a8ceac8e67db292d873b9ddcff29`  
		Last Modified: Wed, 21 May 2025 18:57:02 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6325e5593ea1f6f3a790920e6b257ec71bc407640035071d46e24a39513c569`  
		Last Modified: Wed, 21 May 2025 18:57:03 GMT  
		Size: 22.3 MB (22285521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2776d8e35ca2f02382f1642e157ed33f4f74e78fd8928539a56c5ae24f44d5f`  
		Last Modified: Wed, 21 May 2025 18:57:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6030148901c7351600c9f02b562b4a53e29529ceb074cee8d6eb28afb2473905`  
		Last Modified: Wed, 21 May 2025 18:57:00 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1578bf41a7f3adfda3d1eb7b6461dee92cc2a4b2978d318b0f4236200731c4c3`  
		Last Modified: Wed, 21 May 2025 18:57:00 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53510a068996fc9aabe79b77ec4ad4c64bb1059e1ab235cd4b202615ee35448`  
		Last Modified: Wed, 21 May 2025 18:57:03 GMT  
		Size: 22.2 MB (22168137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:edecae1c2d095917730d282a7f3ea024ce8170290abea8ab49cc7df5394aa8a6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338290860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb43efb9d2cfe15d17f990e55fcc61d7fe49dbf81bd05403cbaee485de6e5d11`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 21 May 2025 18:59:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 May 2025 18:59:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 21 May 2025 18:59:36 GMT
ENV DOCKER_VERSION=28.1.1
# Wed, 21 May 2025 18:59:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Wed, 21 May 2025 18:59:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:59:48 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 18:59:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Wed, 21 May 2025 18:59:49 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Wed, 21 May 2025 18:59:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:59:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 18:59:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Wed, 21 May 2025 18:59:59 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Wed, 21 May 2025 19:00:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d439d9fe925a99b6d486720ccfaeef809346da1ee35c15024cb7a111dc1dc543`  
		Last Modified: Wed, 21 May 2025 19:00:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5ae6911bf6edd73f5cc4febd2f55809213db3ab6fc0494ad7dd897dc58d096`  
		Last Modified: Wed, 21 May 2025 19:00:16 GMT  
		Size: 356.5 KB (356454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02cd251f73d5038f03efb18ec8e28c5d3f5f29cb7d5c1657897cc4f680355e5`  
		Last Modified: Wed, 21 May 2025 19:00:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f92b1fb092ee120c82ebb173e36e04b2465e9f2131eb2844a40f662ad0682e`  
		Last Modified: Wed, 21 May 2025 19:00:15 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e11e17adbece367833fcc3f44af077986d504c8f3af39bd32ceec6640f1ca4`  
		Last Modified: Wed, 21 May 2025 19:00:17 GMT  
		Size: 19.9 MB (19893779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae75b319556bd7cd89c5e72422b779ecdc9e7b394f0dbdcbc7692fa2a5694d36`  
		Last Modified: Wed, 21 May 2025 19:00:13 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cb1ab109461ecf07619d3cfa1ec80222741076ad388babf2a5bf2dcd7fa241`  
		Last Modified: Wed, 21 May 2025 19:00:13 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfb3221f05f029aeb6aa5e5edc498ad9ad33fff7124dbaa0f6635f25a643fd0`  
		Last Modified: Wed, 21 May 2025 19:00:13 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d90c7984a4757ff6911343a88e223d3e572c7ba05922f961e55d47ab8d865`  
		Last Modified: Wed, 21 May 2025 19:00:14 GMT  
		Size: 22.3 MB (22262354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535600fc4df6ccfef5f1acd698b7c42aea07c958b590b0107d94b6e96866959a`  
		Last Modified: Wed, 21 May 2025 19:00:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ef241213c8638321511e0afbbd0c26282fc1fa658b93924ed729a8898c56d9`  
		Last Modified: Wed, 21 May 2025 19:00:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85177ec6e2723ea1d4e965b85a70e58b0531eaf6cd8d7cbf417a270d0366e03e`  
		Last Modified: Wed, 21 May 2025 19:00:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d84faefda6c802a18cf520bc678885355b1d3d4951b6b5b1046d240365c62d`  
		Last Modified: Wed, 21 May 2025 19:00:14 GMT  
		Size: 22.1 MB (22138592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:d1f566a16f16c2200634bd7a63a359b24b8ebd47172b9dfe48b1d9356006c201
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248385541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda2e9a5987756bfb19e127059fdb2b1860cfa05e9a0a5e5a1c10158e79da414`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 21 May 2025 18:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 May 2025 18:53:15 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 21 May 2025 18:53:15 GMT
ENV DOCKER_VERSION=28.1.1
# Wed, 21 May 2025 18:53:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Wed, 21 May 2025 18:53:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:53:28 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 18:53:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Wed, 21 May 2025 18:53:29 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Wed, 21 May 2025 18:53:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:53:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 18:53:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Wed, 21 May 2025 18:53:40 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Wed, 21 May 2025 18:53:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499427d1ce981d67a01cc876c5e76d173129c64d72e2ac487647436c2799eec`  
		Last Modified: Wed, 21 May 2025 18:54:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8313ca7397104a704d56cc50e7a45b675a975d86d85e3bb2704dcade59c25f24`  
		Last Modified: Wed, 21 May 2025 18:54:00 GMT  
		Size: 361.1 KB (361108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab00e7d99a6a7f48e974efeeb5f19e09acfa901a568f72f39ea5da18189481c0`  
		Last Modified: Wed, 21 May 2025 18:53:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb178d15ba158f2ba1ccab2d911bf798570a62e5e8127aa243f7e1a4253a6c94`  
		Last Modified: Wed, 21 May 2025 18:53:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfdfd8e74c6a851dd97b7d10f48b77cfa23d3207a6078640eca5b9f76e30d99`  
		Last Modified: Wed, 21 May 2025 18:54:00 GMT  
		Size: 19.9 MB (19898560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6153bddc7319ae88042ae3163f3b9a73a723397a055690628f58763a1200efb5`  
		Last Modified: Wed, 21 May 2025 18:53:56 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7b52d657a12c957bf43094687db02c895d55d9eb651a2dca3128c3c5d2a42c`  
		Last Modified: Wed, 21 May 2025 18:53:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec147c75c86d456f89990d417ba60a1e7c392fe2d4f8e1653e9b137eaca1fa9`  
		Last Modified: Wed, 21 May 2025 18:53:56 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258083eed3486ac8a927f9fc7e6d30b707f52e2dec9e829fc9d5a0839a83fe47`  
		Last Modified: Wed, 21 May 2025 18:53:57 GMT  
		Size: 22.3 MB (22263789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbb2597924d10232a9d3a8866d2b0538e8c7b16e60d05ee52ab0555b819a3c7`  
		Last Modified: Wed, 21 May 2025 18:53:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361133f9d49e93e7e016ed868e5cbc7d246411d1ade760972be8c34465854ff3`  
		Last Modified: Wed, 21 May 2025 18:53:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88da0b3c5c863751a4c375334afa30e6e6f031bdabfecdf53e97587f21de0e48`  
		Last Modified: Wed, 21 May 2025 18:53:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33e888916251f5c05e42a3d5032cf78093a49332d60eb39652eb72c991be252`  
		Last Modified: Wed, 21 May 2025 18:53:58 GMT  
		Size: 22.1 MB (22133024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
