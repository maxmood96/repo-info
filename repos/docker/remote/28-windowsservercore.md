## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:36a1648985e1f5297301daf2dbefd4472a9d3094029b460620bff6c2cc8027b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:03fb3a913dc4f1465332f09a30d64bd2d1593c087d8076f192958cc0e78ead73
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565629198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dba4f80b10e0ffc054202c373d41b17ed08299798d42223f423c37a30983daa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 01 Sep 2025 22:39:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Sep 2025 22:39:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 01 Sep 2025 22:39:25 GMT
ENV DOCKER_VERSION=28.3.3
# Mon, 01 Sep 2025 22:39:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Mon, 01 Sep 2025 22:39:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 01 Sep 2025 22:39:36 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Mon, 01 Sep 2025 22:39:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.windows-amd64.exe
# Mon, 01 Sep 2025 22:39:37 GMT
ENV DOCKER_BUILDX_SHA256=1e89de288c9897990220d2ee695b50956d42a3a0792c0b070e9fee7711b9f896
# Mon, 01 Sep 2025 22:39:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 01 Sep 2025 22:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Mon, 01 Sep 2025 22:39:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Mon, 01 Sep 2025 22:39:49 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Mon, 01 Sep 2025 22:39:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce467fb2ca593283d716259d94188ee1c7db07b5d251b522ff0e1919dbc8adaa`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8e7b9b4c09027a9f9e7099ee679070906a44e8c98327b16f182a19fade0c24`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 380.9 KB (380911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6bdb99e4ffa1186246d1ec272e9a12b7338929a91e887b763d282dd9c24f8`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941f54a3ed76421817cc8c0063d31aca441f926224430a6f74520e0995ee143f`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0a0098b0bbdaad6162f85f0a2e9adf14fe89aed4714c18dc36e9beeddad9f`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 20.9 MB (20859849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c35ede22d20d1da237e03fbf6806721d65c33eb0681dbccc1965c7c1917d4e`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9032419640af747a06d5d26fbd513025681aac754eff8dce56025265729020da`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2995d785b536a0e21ee15143622b4d651abc8f74e8f14d78228c004232b022de`  
		Last Modified: Mon, 01 Sep 2025 22:43:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab515808fb28c0db212d7836f2d2ceb248a67c98f56df6ec462a00af9ae1772`  
		Last Modified: Mon, 01 Sep 2025 22:43:45 GMT  
		Size: 23.1 MB (23130307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46559d189a20d0a0caef1c4fbe4282a81a22a684a9b3f020a0c8c495a98711b`  
		Last Modified: Mon, 01 Sep 2025 22:43:37 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff97af7cbfef4ee2f69bf6f5b414fa5f316fb7ee9b9d08eb5676f596a9424ac`  
		Last Modified: Mon, 01 Sep 2025 22:43:37 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9eebf1fc56984a1d0592fd38a8a7edae56836d5e88a23c3eb04f945470762`  
		Last Modified: Mon, 01 Sep 2025 22:43:37 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019f501dd43a6c2ca290b616ef72b9cc599efb4623a276a5752300ae5588d2a2`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 22.4 MB (22415690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:fea23f98bc37fdbc260dd8a07fe8acede44461120acf94bf6eda83989f8a6cb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348246655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b99128cde343e7f88f2b466a99ab25313f6cfc097ff4bd18a6dbf98c1c332bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 01 Sep 2025 22:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Sep 2025 22:35:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 01 Sep 2025 22:35:15 GMT
ENV DOCKER_VERSION=28.3.3
# Mon, 01 Sep 2025 22:35:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Mon, 01 Sep 2025 22:35:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 01 Sep 2025 22:35:35 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Mon, 01 Sep 2025 22:35:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.windows-amd64.exe
# Mon, 01 Sep 2025 22:35:37 GMT
ENV DOCKER_BUILDX_SHA256=1e89de288c9897990220d2ee695b50956d42a3a0792c0b070e9fee7711b9f896
# Mon, 01 Sep 2025 22:35:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 01 Sep 2025 22:35:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Mon, 01 Sep 2025 22:35:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Mon, 01 Sep 2025 22:35:50 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Mon, 01 Sep 2025 22:36:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d889f82830dee53ace7cb143aea2cc46eac27873259d87b424a4338267f61e9f`  
		Last Modified: Mon, 01 Sep 2025 22:36:37 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dac808240f9af82f49a031ac3aff0005dec4393846fb557995e9ead0c6b1e7`  
		Last Modified: Mon, 01 Sep 2025 22:36:37 GMT  
		Size: 347.4 KB (347431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3821ed3fb9a6213b172071d52cb9a7fe7bb6834a9298ec830d32c25ec41491d7`  
		Last Modified: Mon, 01 Sep 2025 22:36:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cb5070c1ca1deb64c3454baa10f84e036037f643795d567eb89b28b1e4131e`  
		Last Modified: Mon, 01 Sep 2025 22:36:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bd7d16f38fbd761e815c63f813ec08cb86a1021e4344614a58bb3c46d61c63`  
		Last Modified: Mon, 01 Sep 2025 22:36:38 GMT  
		Size: 20.8 MB (20793756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a81976cff0193aab560baad775ca4e72fe06d5880978313c74e6144eeb9c29`  
		Last Modified: Mon, 01 Sep 2025 22:36:39 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6a824d6f7297959d8fe1902e4657cf59ed2abe776e68864121dbd4bc20b01c`  
		Last Modified: Mon, 01 Sep 2025 22:36:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415e6d6777b6d6831835ae2dcc03d4e442f0239ece676844de7a14ae42d90758`  
		Last Modified: Mon, 01 Sep 2025 22:36:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b360cbe3efafee08b630f7a08d210a4c917d4c029b1e0362229d47c3dc0ff20a`  
		Last Modified: Mon, 01 Sep 2025 22:36:39 GMT  
		Size: 23.1 MB (23058984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81996d89ec6356f15058f81343ffc30af888dd8940ef3dda54b5e1834c72be0`  
		Last Modified: Mon, 01 Sep 2025 22:36:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8607375d6805249ea112680ad9e018f1626fd0c9460aaafbe8b81dafaf4257c1`  
		Last Modified: Mon, 01 Sep 2025 22:36:38 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b105f78a01edee86cbba4068c8ea5d9982fb6ed74c7340d136b8d5262ddde56`  
		Last Modified: Mon, 01 Sep 2025 22:36:39 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe73e11ce7a6f02c1680d677422e7aee0ccbe9b275d8c75c42ffc847a0dd11ea`  
		Last Modified: Mon, 01 Sep 2025 22:36:40 GMT  
		Size: 22.3 MB (22342992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
