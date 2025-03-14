## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:6283c3fe89ee15688a386677b241d6c87667b3cc28991a59898e00fb2ff030d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:35a99ef123c2d7d7c1ea1af9528e66f511dd018820f0b3cea86a987981376d0b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974039150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b092167b743cc6021d6d129b02a71a082de6f5c93aadf17a5dfb52a1d209c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Fri, 14 Mar 2025 20:20:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Mar 2025 20:20:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Mar 2025 20:20:18 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 20:20:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Fri, 14 Mar 2025 20:20:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:20:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 20:20:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Fri, 14 Mar 2025 20:20:32 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Fri, 14 Mar 2025 20:20:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:20:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 20:20:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Fri, 14 Mar 2025 20:20:43 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Fri, 14 Mar 2025 20:20:52 GMT
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
	-	`sha256:f2a5babb7eba4f089393a9640725650e10994b5ed0b9c609982506e957d47370`  
		Last Modified: Fri, 14 Mar 2025 20:20:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218c27cd0a95eed5a1c4341e7fdc6ae4255c521e08864640c1351258b949c0b2`  
		Last Modified: Fri, 14 Mar 2025 20:20:58 GMT  
		Size: 395.2 KB (395244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e104247e9828963bd2674047321016e63ed7315297860a86485ac4ffc7ae18c9`  
		Last Modified: Fri, 14 Mar 2025 20:20:57 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbf999a57169ebb61d294b9be8ab198343425c6cf19831ec551c391592f22dc`  
		Last Modified: Fri, 14 Mar 2025 20:20:56 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfed6473f68822fc7a9b64f81bf6bca94ddca398395940935700996a9b7fc84e`  
		Last Modified: Fri, 14 Mar 2025 20:20:58 GMT  
		Size: 19.9 MB (19861849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1b796b3730c540738691178687e527833979e90a3cd49af25f545e2ad35536`  
		Last Modified: Fri, 14 Mar 2025 20:20:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbdacd081372db06de4b3b4e0459289992bc9856cdeee2fc178fe604d565ecb`  
		Last Modified: Fri, 14 Mar 2025 20:20:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dfc7b648e8f38d94efd90a7fac02e634ca21581fceb31345144969dc885493`  
		Last Modified: Fri, 14 Mar 2025 20:20:55 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caf08f7c95a51604b46ce6e9bbe22f1968869fad1ed71f33247d35c7f374b8f`  
		Last Modified: Fri, 14 Mar 2025 20:20:58 GMT  
		Size: 22.8 MB (22787743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa5dd995d867671e4df5dadb8f295e1d24b0800b6eb1e80b0a3c7a99f8c9062`  
		Last Modified: Fri, 14 Mar 2025 20:20:54 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5968436f05105bed74785696d55d21c1b130b08a73ef083cb4d53251f2cfba`  
		Last Modified: Fri, 14 Mar 2025 20:20:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb30c755dd22eeb309f90a9eb682a61edd11a01506e372f7a3fc7e0681cd14b5`  
		Last Modified: Fri, 14 Mar 2025 20:20:54 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323f27a4b436ab8b8acf790d34d3c666c8b5acf56661e45290079c39e959ef7a`  
		Last Modified: Fri, 14 Mar 2025 20:20:58 GMT  
		Size: 22.3 MB (22334786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:538f4999202c7e81b53d6b08e3c57970e153f2b39ac17a41fc1cfb146d960797
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335146546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eda11887160daecb3912a773a2f13fb72352ff56a0562ad2b2f014edb7fbef9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Fri, 14 Mar 2025 20:27:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Mar 2025 20:27:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Mar 2025 20:27:33 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 20:27:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Fri, 14 Mar 2025 20:27:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:27:46 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 20:27:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Fri, 14 Mar 2025 20:27:48 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Fri, 14 Mar 2025 20:27:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:27:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 20:27:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Fri, 14 Mar 2025 20:27:59 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Fri, 14 Mar 2025 20:28:09 GMT
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
	-	`sha256:e83bfd3cec0ebe5c646d5735b43ab392607ab6725811e4dd9c8101085c3ab3ef`  
		Last Modified: Fri, 14 Mar 2025 20:28:16 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d483288d5dd71b58e5d2e39986f24e3add8983efe6a4344f8d3da14fc305a`  
		Last Modified: Fri, 14 Mar 2025 20:28:15 GMT  
		Size: 353.8 KB (353804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4e6d225bb6e736cda1f7293493d8b94ae2f4dc09c518455eeccb70382e48e7`  
		Last Modified: Fri, 14 Mar 2025 20:28:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdc60933044b936dcdddb73f9182097bdaaa7972196c25e38b6bfd0f24e549b`  
		Last Modified: Fri, 14 Mar 2025 20:28:14 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c8f449256923700c12fda37d9616e2add2bbff61401ab259cbadaaeeb071e5`  
		Last Modified: Fri, 14 Mar 2025 20:28:15 GMT  
		Size: 19.8 MB (19812922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afc67b968ae48dc367b6f06cad02e565d1eabf6cc403c13b14282176ea39bd2`  
		Last Modified: Fri, 14 Mar 2025 20:28:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17820c7b2f6c9966d8cd748221a321b899635ea378b88301a074474b9fe2a999`  
		Last Modified: Fri, 14 Mar 2025 20:28:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71895d0e38c1b29c95f81698e598e9bfb8feff1aa772410ae1c01b13c308d79`  
		Last Modified: Fri, 14 Mar 2025 20:28:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101409f72d4da5d00ba9032cd3741626d13207f92fa60522af3ccd6041d5275a`  
		Last Modified: Fri, 14 Mar 2025 20:28:16 GMT  
		Size: 22.7 MB (22739166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e89052fe33793fbde299dcbc3130cb0545e9e71d748c173b94d70d04e1dc6`  
		Last Modified: Fri, 14 Mar 2025 20:28:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55431de88dc75aefa8f8aec17bc87c48ebd27a4e417c7ed2c978c16ccf50131f`  
		Last Modified: Fri, 14 Mar 2025 20:28:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b940fd21726a05c3c591d44f8610b4090fe6b744898edd72e85984bbf3d528b2`  
		Last Modified: Fri, 14 Mar 2025 20:28:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bea29af16c9bd9f321318cfbe88d357222fcda3630d99622848479e38ef89f`  
		Last Modified: Fri, 14 Mar 2025 20:28:16 GMT  
		Size: 22.3 MB (22287865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:0a694638bc3152b57c933b27342a3675817c76fe00b6e473ddf7569acb752858
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216825684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28e7bd7c2a77861878ea9d6acc2c71f7f5f06e846a61d3447f6d5333c367a69`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Fri, 14 Mar 2025 20:22:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Mar 2025 20:22:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Mar 2025 20:22:54 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 20:22:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Fri, 14 Mar 2025 20:23:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:23:08 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 20:23:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Fri, 14 Mar 2025 20:23:09 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Fri, 14 Mar 2025 20:23:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:23:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 20:23:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Fri, 14 Mar 2025 20:23:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Fri, 14 Mar 2025 20:23:30 GMT
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
	-	`sha256:ed918122fc29d1ad29df866b313bce7001d47ac1eb47062e4235994521aef586`  
		Last Modified: Fri, 14 Mar 2025 20:23:39 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd329e02e93a958cd27d04d45a380670c9d25f0fd7d06e62522c8b70baf8e7a`  
		Last Modified: Fri, 14 Mar 2025 20:23:39 GMT  
		Size: 339.4 KB (339420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60059bb6810810d7fd065fdc61f8f620ad5a195503e861cb7cd6b2d638fecb74`  
		Last Modified: Fri, 14 Mar 2025 20:23:38 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d1c9f5395896c289e6089101131c105321a3869ba6dd90e3950be2adc74c3b`  
		Last Modified: Fri, 14 Mar 2025 20:23:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3ac701ca298923890a22b35dbdf2811d83ac7ad47cd329cbfe93c5deb49dc4`  
		Last Modified: Fri, 14 Mar 2025 20:23:39 GMT  
		Size: 19.8 MB (19815150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ebd6e37566eae8442f166b1107e57e98f66ff6e80718cfc1f7cf8061f7bee1`  
		Last Modified: Fri, 14 Mar 2025 20:23:36 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f82c328b654329fdfeedec58a10c0622ac05de5ef2fbcf213575b18d0ddb6d`  
		Last Modified: Fri, 14 Mar 2025 20:23:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b5f4d03be59c4be11f3157cc59a36dea48da05b4a8ebdaed5e13e0a2c1dcdd`  
		Last Modified: Fri, 14 Mar 2025 20:23:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0bea2b6f7984f4b6aca23c9e0bf53b4586c96e09eb75d9914c06d1e63a4e8c`  
		Last Modified: Fri, 14 Mar 2025 20:23:37 GMT  
		Size: 22.7 MB (22740895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035b7581971c5d79ebc58ffdb94bb5df3fd9514696e4515ddb6ef80845b5a997`  
		Last Modified: Fri, 14 Mar 2025 20:23:34 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a11663aaf86370562ddb2f14941d1012988a41b2a8723e1cdfd217a951144a5`  
		Last Modified: Fri, 14 Mar 2025 20:23:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77d2ca98e41f2583ed3da2d477d7217f482cb971d7decc53c9a20eb798b4dd`  
		Last Modified: Fri, 14 Mar 2025 20:23:34 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22db86579608f100db6522d1ed570194e7e942c453a471207da13d66670a9c38`  
		Last Modified: Fri, 14 Mar 2025 20:23:37 GMT  
		Size: 22.3 MB (22283834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
