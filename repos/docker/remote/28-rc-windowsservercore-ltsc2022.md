## `docker:28-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c4d409719d7d1a11ca06ac1fb9b6f09fc33c046b2108179db87c90cc37bd9ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:445a304feb2e88a9cbdf7d6467a249fc73f9a795f690d09803f7a9c60cddf189
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338685339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b352545fe1da3c73500927364a22132aa12dd898891e3c799fd651c5c7a8a011`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Sat, 24 May 2025 00:25:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 May 2025 00:25:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 May 2025 00:25:40 GMT
ENV DOCKER_VERSION=28.2.0-rc.2
# Sat, 24 May 2025 00:25:41 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.2.zip
# Sat, 24 May 2025 00:25:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:25:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Sat, 24 May 2025 00:25:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Sat, 24 May 2025 00:25:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Sat, 24 May 2025 00:26:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:26:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Sat, 24 May 2025 00:26:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Sat, 24 May 2025 00:26:02 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Sat, 24 May 2025 00:26:09 GMT
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
	-	`sha256:12e3de0e0111f27c4d52da00b9ef260cae0fe83e3d5281fc6c379e496ab555c9`  
		Last Modified: Sat, 24 May 2025 00:26:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7259b63fc079fb24d0965455934211a105573390f6fba346ae28b548eb0c9f8c`  
		Last Modified: Sat, 24 May 2025 00:26:15 GMT  
		Size: 351.0 KB (351045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544468963f723f105125f6135d6b1e6504c84e5b9ce43a74ab917f5404c70acb`  
		Last Modified: Sat, 24 May 2025 00:26:14 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ca2c63da9409264a7229b24de94301dfca28ce1c7abbbc0fb4d9f4c705244b`  
		Last Modified: Sat, 24 May 2025 00:26:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2daf772cbd1bf7e3be7d00e429944fa7f551114f487c9f270643cfd0f2ac29c8`  
		Last Modified: Sat, 24 May 2025 00:26:15 GMT  
		Size: 20.4 MB (20436850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d30e98983ee866bb6a30c5027875c8d34b0d1789192512af472fb53d869fe4`  
		Last Modified: Sat, 24 May 2025 00:26:13 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8685156deecfa30ddff0c2b5bbd9ac2c07878b014a6ac6fdaf545d4ee283fe`  
		Last Modified: Sat, 24 May 2025 00:26:13 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4e5a0f29ee98541294025f3479d95df1490b1a361d77bedc195fc00f49523b`  
		Last Modified: Sat, 24 May 2025 00:26:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd67b57fa5cef74a477f422f445addcebe69e40760fe4907bcebca9157b54ae4`  
		Last Modified: Sat, 24 May 2025 00:26:14 GMT  
		Size: 22.3 MB (22254509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c6311fc7acd0d041ca683ea7eb8ed46935abbb3f4ffbcde57e950482bc1bf`  
		Last Modified: Sat, 24 May 2025 00:26:11 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a28adcfd286d46be02aeeb80c0a500b54bb996c70a12c6d501f881d78860984`  
		Last Modified: Sat, 24 May 2025 00:26:12 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4283558e0ab62442243b8062119f5821615fd15cef3427e6c606e62c1d62801`  
		Last Modified: Sat, 24 May 2025 00:26:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3983537ff7067310e75f45a0d421f3332a19d459a20ab347ac46ccf713a099a`  
		Last Modified: Sat, 24 May 2025 00:26:14 GMT  
		Size: 22.0 MB (22003238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
