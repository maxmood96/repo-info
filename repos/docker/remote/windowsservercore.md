## `docker:windowsservercore`

```console
$ docker pull docker@sha256:888ccff3b9636b55646e6bb5477e92d060a93a2c17c21e6e1bddb8907b3667ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
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
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
