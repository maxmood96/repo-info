## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:bbd27b75d62eb2a01c7411d844d6dbb4b3f0791c7e18f1f32755ec35bfa2d430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:5a69cb05f52d14ef11fdd011f41f30046b153b39e35920f62471216b15a7b60e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541854833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed5775a8322a1df58857e50173fd7b2e54ef42266e46e0bd41a38d2057e3fa6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 16 Jun 2025 17:59:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 17:59:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 16 Jun 2025 17:59:47 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Mon, 16 Jun 2025 17:59:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.3.0-rc.1.zip
# Mon, 16 Jun 2025 18:00:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 16 Jun 2025 18:00:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 16 Jun 2025 18:00:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Mon, 16 Jun 2025 18:00:10 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Mon, 16 Jun 2025 18:00:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 16 Jun 2025 18:00:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Mon, 16 Jun 2025 18:00:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Mon, 16 Jun 2025 18:00:26 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Mon, 16 Jun 2025 18:00:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe196980a94a57510545ad7497d7be6fde3f4b61e6d989b021b118736bce717`  
		Last Modified: Mon, 16 Jun 2025 18:04:35 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5267311e1cd49617a678f82fb14e6e7de627ffa4161504b2cf222657cdc713b7`  
		Last Modified: Mon, 16 Jun 2025 18:04:35 GMT  
		Size: 411.4 KB (411441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6205cf9ec6c1f54fe6063a991312205fcf4605a08889ee3d26e68559166deecb`  
		Last Modified: Mon, 16 Jun 2025 18:04:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486ceec100347b4501f8d7273342719f832d61174bf33dab3c12ae7fea8dd196`  
		Last Modified: Mon, 16 Jun 2025 18:04:35 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1319b07baa51287b8ea42c06f3d3f99a4781e271494d36aaedf8a9310a085e96`  
		Last Modified: Mon, 16 Jun 2025 18:04:40 GMT  
		Size: 20.9 MB (20870725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200ef71d91ebfba452baf1e2907e50771cecd0cca753a22712e581564a99e847`  
		Last Modified: Mon, 16 Jun 2025 18:04:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739afa9e4969aaf5a16d8d33b377774e3f192ac3667fc1d4e22a1bb88290314a`  
		Last Modified: Mon, 16 Jun 2025 18:04:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c79fb4fcdf8d01ae6e66824c03901711b471af13d89b82848489602b58bd5`  
		Last Modified: Mon, 16 Jun 2025 18:04:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029b364720ff32debe500d22ef1ae8b32cd34a324bd021f85ba824b3b3b73ba3`  
		Last Modified: Mon, 16 Jun 2025 18:04:22 GMT  
		Size: 22.3 MB (22307647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ae07dc9b642ba1053ac18d1492384d613b34939a6c59adc2a6b76397723e6`  
		Last Modified: Mon, 16 Jun 2025 18:04:21 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d44f81cacbb915d54840063ab7470c0a034f64bf550a5cb41b9296cc66d496`  
		Last Modified: Mon, 16 Jun 2025 18:04:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f74a8275a019a0fd9a0af38a2126d372ab1afb31aeb240bd75c197499a934b`  
		Last Modified: Mon, 16 Jun 2025 18:04:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a14bb4599cffce349d56a126369a3ed25eb0a5dae8cd32680ad7b2a2e1a71`  
		Last Modified: Mon, 16 Jun 2025 18:04:23 GMT  
		Size: 22.1 MB (22079229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:1c18d1ace8ad03daa25ce539abbf5d77e10bbe68fe3f7c2090d9315943708c54
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345728613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af0d828d7d252811a139b284f7971d1495419ff796f64bd288cf9d5d7ff549d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 16 Jun 2025 18:08:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 18:08:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 16 Jun 2025 18:08:32 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Mon, 16 Jun 2025 18:08:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.3.0-rc.1.zip
# Mon, 16 Jun 2025 18:08:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 16 Jun 2025 18:08:46 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 16 Jun 2025 18:08:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Mon, 16 Jun 2025 18:08:47 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Mon, 16 Jun 2025 18:08:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 16 Jun 2025 18:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Mon, 16 Jun 2025 18:08:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Mon, 16 Jun 2025 18:08:58 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Mon, 16 Jun 2025 18:09:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0046aca4639c724d05f2dfe9e79f315394048286853bdaa63815531dba5330`  
		Last Modified: Mon, 16 Jun 2025 18:10:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a46c34654491cce60a9274acd4ca7d6dc971ce937018dd526358223f6f643cc`  
		Last Modified: Mon, 16 Jun 2025 18:10:25 GMT  
		Size: 355.5 KB (355532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8942102d92dbbd4e7ec6585b949b409eead4cfa4e4b737973cea01b2e58eb0e6`  
		Last Modified: Mon, 16 Jun 2025 18:10:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad591045392d9ab8d49e096a953713861327266c5532b421ea256e955c87b77`  
		Last Modified: Mon, 16 Jun 2025 18:10:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9393df109419e72a0569c82be3f3b6d5b94ddffb2f5da165cd7a8fa956ad7ec`  
		Last Modified: Mon, 16 Jun 2025 18:10:27 GMT  
		Size: 20.8 MB (20821847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbff2522ca5ca1869f18b87673157fe6dc17bbc382b9c6da19d72648acab92e6`  
		Last Modified: Mon, 16 Jun 2025 18:10:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a09fde025b3a36d6de22e0fbfb9d9a5b42b1ecfa3cd6cd217cb3b2748308d01`  
		Last Modified: Mon, 16 Jun 2025 18:10:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dde16cdf633804f0113c042a518ecbe1b1c92df2eed41231a25f965e80fb1c`  
		Last Modified: Mon, 16 Jun 2025 18:10:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336868c0fcd8da12e46ebb9051b9d3d56c461b0d39635cacce3580a453f2c8a6`  
		Last Modified: Mon, 16 Jun 2025 18:10:29 GMT  
		Size: 22.3 MB (22261133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fcd30cae683d7bb643d1cd126b74edc82822c67bde66b9f5a343706ec49dc9`  
		Last Modified: Mon, 16 Jun 2025 18:10:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f345ee83a0aaeb0e8dce4d715d7725f42fcd0e26eb1c8f2cde02c21dc7324d77`  
		Last Modified: Mon, 16 Jun 2025 18:10:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc672a420fa48c976c624918d6141630c3fb998e6f6afe85488468e3aee0a74e`  
		Last Modified: Mon, 16 Jun 2025 18:10:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a90762661a6f6431a85193c64734bfbd88403e65256d26d6aa38fea34457c2f`  
		Last Modified: Mon, 16 Jun 2025 18:10:41 GMT  
		Size: 22.0 MB (22026924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
