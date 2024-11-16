## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b78f4a4a07430c9b97fda04d60b1917c2ff4467b833d1ea7ae65be6c8efe3106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:ed7f0dd01d6293c0a5d9a4729b732b3c1e471970eef0de4c065448593ac58909
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520673493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e77e8e8f1ca989ccd75afdda7dcbb2304d55a29515a044413a4b155d94a682`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 18 Sep 2024 17:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Sep 2024 17:56:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 18 Sep 2024 17:56:15 GMT
ENV DOCKER_VERSION=27.3.0-rc.2
# Wed, 18 Sep 2024 17:56:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.3.0-rc.2.zip
# Wed, 18 Sep 2024 17:56:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 18 Sep 2024 17:56:27 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 18 Sep 2024 17:56:27 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Wed, 18 Sep 2024 17:56:28 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Wed, 18 Sep 2024 17:56:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 18 Sep 2024 17:56:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Wed, 18 Sep 2024 17:56:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-windows-x86_64.exe
# Wed, 18 Sep 2024 17:56:38 GMT
ENV DOCKER_COMPOSE_SHA256=4eda107dc1f83a57116c57595d39e6a0ff63e696a52230ea277bd7fa7977c8d7
# Wed, 18 Sep 2024 17:56:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b356a9373c67bc01437fcc079a69b9c0f1c6cc5e6cc3b52a70319ed9a94681`  
		Last Modified: Wed, 18 Sep 2024 17:56:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffbe15d034c4460b1cd6df8bdb52592886e61ad83240498a231825193090cd0`  
		Last Modified: Wed, 18 Sep 2024 17:56:55 GMT  
		Size: 367.0 KB (367036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef004a0afab4386b84b2315606616992a3b607301bd6e5a700102cc429a5d6c2`  
		Last Modified: Wed, 18 Sep 2024 17:56:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617958e23cc695f2bdb9adf6ebae5b4bcf349e1c1e17f1d41b8e84ec2a3bcd73`  
		Last Modified: Wed, 18 Sep 2024 17:56:53 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9687a20c763a3bdb197adfd261627e6db6835d23165c2b2bbd809141178780`  
		Last Modified: Wed, 18 Sep 2024 17:56:55 GMT  
		Size: 18.9 MB (18893390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adeb800e76e138ad70fc9e923572411681749f51653351f14d8654720f97f96e`  
		Last Modified: Wed, 18 Sep 2024 17:56:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9006a02172f3eeb4615fc8bd4bbd63d3938c95a1fcad6b167367113df3d49d`  
		Last Modified: Wed, 18 Sep 2024 17:56:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d442edccdd08c7cbba330a9f960ebd903a4ac47467d2f37be3f2378f7ff2ab44`  
		Last Modified: Wed, 18 Sep 2024 17:56:52 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5191f35def74322349528de3239f10d10084810efbfe9054bc2783c693d270`  
		Last Modified: Wed, 18 Sep 2024 17:56:53 GMT  
		Size: 19.3 MB (19288629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dea924090002cc8b2f65d1a5f2782501c956f6dd82f767177dec599d17fd89`  
		Last Modified: Wed, 18 Sep 2024 17:56:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3dea645ede50e5df152757613ca83ab5c4d9f5396298fac2f1ee9992ea5e95`  
		Last Modified: Wed, 18 Sep 2024 17:56:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134c5f0ff9fea4a1582299ed35880f3f41fc8063cd955315a292218471cda730`  
		Last Modified: Wed, 18 Sep 2024 17:56:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce28281b94f629d6c7a6762468171a79c404244078d075991d5f413d39ae8a27`  
		Last Modified: Wed, 18 Sep 2024 17:56:53 GMT  
		Size: 19.9 MB (19920363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
