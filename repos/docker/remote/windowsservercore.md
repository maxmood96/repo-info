## `docker:windowsservercore`

```console
$ docker pull docker@sha256:f63b7f4c754176432cb02b6df9b22363d006a10d4847a4e861c843c9d1e85480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull docker@sha256:b787c9789b3e1f229f1a18ecce89f90ed4af18db8d40c34b2e1f26b21df7f329
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170865718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7247690dbdd1dad74cfc715193b158738ff09462dff187094caa02e9599eb9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 05 Jun 2024 19:53:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 05 Jun 2024 19:54:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 05 Jun 2024 19:54:51 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 19:54:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Wed, 05 Jun 2024 19:55:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 05 Jun 2024 19:55:08 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 05 Jun 2024 19:55:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 05 Jun 2024 19:55:10 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 05 Jun 2024 19:55:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 05 Jun 2024 19:55:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 19:55:20 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 05 Jun 2024 19:55:21 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 05 Jun 2024 19:55:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60926ad275a20f87cd180e251fe27c024cfdccfb4c917f519ce09b5479f200a`  
		Last Modified: Wed, 05 Jun 2024 19:55:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0349f472edc1a10481cb19a4cc565387a6dfe2beadcb40854334cbd1d821e`  
		Last Modified: Wed, 05 Jun 2024 19:55:39 GMT  
		Size: 359.8 KB (359830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127ac9c6dfdd03a922655d18329d7f8a8f86de5ea7c9760284338ab44c6ae0b`  
		Last Modified: Wed, 05 Jun 2024 19:55:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d3ad23e8c14c90a2737ec6b8757aa11e1f4050b21a7b5063cdea1065ec4578`  
		Last Modified: Wed, 05 Jun 2024 19:55:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff4d27ae7eb20cfd30e4eae656a52ad032b7b4c1cf1b38254c663567275fa6c`  
		Last Modified: Wed, 05 Jun 2024 19:55:40 GMT  
		Size: 19.3 MB (19253175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f12b2dd07d550959bc3684d0023d09e7bdd5d3eff99775bcfa6445898f9883d`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dc664c296e9f466b7059eec930faec106903f69057da835aa173b69958fc07`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717c76f39c894f08e4b267de3c93e800fa2f4a95e91c7559b192f79e8887707e`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c475eed2f3ae1a218f11298c10e246ba03cfa5b7756973f0fbb37f98aff7a8d`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 18.9 MB (18931360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ab9dfed534aac25935e94cffcad9c27f1083d8f2ee3ec46ed0e48c248e2ec6`  
		Last Modified: Wed, 05 Jun 2024 19:55:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb78d95032f41c0991d3325887cff15fdc96dc77faa53032b743a8f08227b06`  
		Last Modified: Wed, 05 Jun 2024 19:55:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bf2312acea1db4b5c8b958af372082aceec3892d4d560bae3f2ec44f5c3f23`  
		Last Modified: Wed, 05 Jun 2024 19:55:34 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92ea4a144add9f5889379b66d67fe56e1cf88725d22a4f8d67475c9ab656876`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 19.6 MB (19638389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull docker@sha256:69e6e1c677587ff5cfa1425bcfbfccef1011a86d0d77dae2bd13ee62b348477c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2238079428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb655c2895110996c9a6aff928c9dbd27f9ee394deebc645b5abd73d70d7ffd7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 05 Jun 2024 19:53:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 05 Jun 2024 19:55:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 05 Jun 2024 19:55:36 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 19:55:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Wed, 05 Jun 2024 19:56:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 05 Jun 2024 19:56:10 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 05 Jun 2024 19:56:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 05 Jun 2024 19:56:11 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 05 Jun 2024 19:56:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 05 Jun 2024 19:56:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 19:56:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 05 Jun 2024 19:56:48 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 05 Jun 2024 19:57:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e04e6ca3d1265d92c909905156beca6ca4a025101a45ac9ce953e9cb9b243f`  
		Last Modified: Wed, 05 Jun 2024 19:57:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cd39f897979200e694f209aa28e7e5cc43ad06b99a6338f49f1d7dcd056ec8`  
		Last Modified: Wed, 05 Jun 2024 19:57:23 GMT  
		Size: 495.7 KB (495735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932eaf4c9cf289a0e28d7f94e65b7a19187d960684404d8d845d620c2d3c3237`  
		Last Modified: Wed, 05 Jun 2024 19:57:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd691f0c95a59428f610232d3e169456cb2603e332acb815381faa8b0bc5c0a`  
		Last Modified: Wed, 05 Jun 2024 19:57:22 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8891f8c623550ec8c26add4766358c0f9006ec39bf05c093439fb16b7636cedd`  
		Last Modified: Wed, 05 Jun 2024 19:57:24 GMT  
		Size: 19.3 MB (19268715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28d4fbf48084cfd9bac2d82413f2a0b0aad4cacb550089d834e687d5e8770a`  
		Last Modified: Wed, 05 Jun 2024 19:57:21 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391f12cceec60b0874b1f4faf77815ca8f0af7f625a05b875e9a3fa4aed8da46`  
		Last Modified: Wed, 05 Jun 2024 19:57:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2854b4ff7a9ed08244de3f3ad1df467988fb04a14fdaded11559e6c535266197`  
		Last Modified: Wed, 05 Jun 2024 19:57:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0036c3bfef0edc6929b515024771bbb1e9c47b9accdd08df113c7fa1f8f989d9`  
		Last Modified: Wed, 05 Jun 2024 19:57:22 GMT  
		Size: 18.9 MB (18942213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6986a3a6568b28591bcec084c765e1c9bd477d593d26306fd410b0cab8ad4d5a`  
		Last Modified: Wed, 05 Jun 2024 19:57:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b812960ae17a5094d6abec875322b7b34abc7494a7a1c0f1ca5e08b5e1a35154`  
		Last Modified: Wed, 05 Jun 2024 19:57:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14fc5195e3c4bc1beacfbd6fedd92393dfd2f4d062e12e7817e75819c37f232`  
		Last Modified: Wed, 05 Jun 2024 19:57:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd721a78d1e9120465f886472e0b65b9b558616e7c2fa11bcfe95b750944b64`  
		Last Modified: Wed, 05 Jun 2024 19:57:22 GMT  
		Size: 19.6 MB (19649630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
