## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:6cbf0cc9068592d39d2a597fefad8dfec3a8fb8d1749dec0f05abeebf7ed354c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:008491dd4704ab1b8a11df2c2facbaae62cbf13f1f3eb084bf59c309b55bf805
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496039642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df88a74a802c68bb96f4a42a9403c9e15c8a1dc8559ba8ec6beb8ba7cc8b0d63`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Sat, 24 May 2025 00:25:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 May 2025 00:25:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 May 2025 00:25:38 GMT
ENV DOCKER_VERSION=28.2.0-rc.2
# Sat, 24 May 2025 00:25:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.2.zip
# Sat, 24 May 2025 00:25:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:25:49 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Sat, 24 May 2025 00:25:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Sat, 24 May 2025 00:25:51 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Sat, 24 May 2025 00:25:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:26:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Sat, 24 May 2025 00:26:00 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Sat, 24 May 2025 00:26:01 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Sat, 24 May 2025 00:26:10 GMT
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
	-	`sha256:591ba866027e847bba934488c6162e7f9d007b94b3b6d849fcce274949614c3a`  
		Last Modified: Sat, 24 May 2025 00:26:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8c1fc070f7bb573566de5c32cac8a2a6465d1697557b6ac1219222aa6dc242`  
		Last Modified: Sat, 24 May 2025 00:26:20 GMT  
		Size: 405.5 KB (405542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b85ea38920df696011cd0d57850acede8d48effdee3c10c75c2bb91de923b5e`  
		Last Modified: Sat, 24 May 2025 00:26:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26217a3bfd56af5065ff92996301c310a1096a4199b876eb6afcba46613f405`  
		Last Modified: Sat, 24 May 2025 00:26:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6557f003920af4df18087d6072faccead9b88ba01434eb9ad218344f8edfca6e`  
		Last Modified: Sat, 24 May 2025 00:26:20 GMT  
		Size: 20.5 MB (20489398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47333bd02d7ea1e47e8d0a2a36b5eb4efecc86049965ae4fff31ed276140cf00`  
		Last Modified: Sat, 24 May 2025 00:26:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96671e2a307f6b7d41b0cf48acc54016c7bd4e28abf00a331c4ede591d82cce2`  
		Last Modified: Sat, 24 May 2025 00:26:17 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3fc6280d51c1f957a0cdea9702249e7af68e485b407594cdaeba1bfdd22ba`  
		Last Modified: Sat, 24 May 2025 00:26:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93922b4be4088d515b79ea36629984a45aaaa39cb1c540609622e346a5feca3`  
		Last Modified: Sat, 24 May 2025 00:26:17 GMT  
		Size: 22.3 MB (22306332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89696783c489b4ddcc75986af4711459af9206ccf5d1f5d64277beb4cc2040d4`  
		Last Modified: Sat, 24 May 2025 00:26:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3123ea3daae986d99a1a59cede98e9186600bb4d21dd67262a898ae4787b1763`  
		Last Modified: Sat, 24 May 2025 00:26:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75679fd384131448db62fc009bae9aa84d06bf1c4d1110f01546af3405da9155`  
		Last Modified: Sat, 24 May 2025 00:26:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bafdc1f5c25287448a070f7cfe47a9d43268f2c00891a0eb223c8f976641db`  
		Last Modified: Sat, 24 May 2025 00:26:18 GMT  
		Size: 22.1 MB (22060849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.3692; amd64

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

### `docker:28-rc-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:f1a89df7c53c7dfac7b29a6612fa88952449c40867eb4b01e0f270d169928410
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248868900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056565e8f6ee860761212d44751317c2e99b8be580caa62f78746d274278ef72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Sat, 24 May 2025 00:22:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 May 2025 00:22:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 May 2025 00:22:44 GMT
ENV DOCKER_VERSION=28.2.0-rc.2
# Sat, 24 May 2025 00:22:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.2.zip
# Sat, 24 May 2025 00:22:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:22:56 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Sat, 24 May 2025 00:22:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Sat, 24 May 2025 00:22:57 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Sat, 24 May 2025 00:23:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:23:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Sat, 24 May 2025 00:23:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Sat, 24 May 2025 00:23:06 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Sat, 24 May 2025 00:23:15 GMT
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
	-	`sha256:2b7ef241f8b857578702f535bb88edd7ce6097a0f2cdafbdaf5707d4fdbb91b8`  
		Last Modified: Sat, 24 May 2025 00:23:20 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e10efa7c358f5f265995a5ca81fe2b9a78d81ecc4ca9d694c947e4eae26b9b3`  
		Last Modified: Sat, 24 May 2025 00:23:20 GMT  
		Size: 376.6 KB (376641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2535217676498abcbd0c07b49661eb3b8723343f213591611e6bf30d0571fef`  
		Last Modified: Sat, 24 May 2025 00:23:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9798f17e81f73297f77e2ed8cfd41ac06691099e1ed339eb84f921a5b652d990`  
		Last Modified: Sat, 24 May 2025 00:23:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d5e58b58549cfbaba9ecc0f92581854eb132815cf282974ac3bc95d8e547da`  
		Last Modified: Sat, 24 May 2025 00:23:21 GMT  
		Size: 20.5 MB (20462420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546ccfd97644ce015beefbcff4592d23d654cc76e17d172d54cc8fa37bddd641`  
		Last Modified: Sat, 24 May 2025 00:23:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c161426b0e02f75b7d46a19197e9a79fdb13556b35b6752bb595120c27668463`  
		Last Modified: Sat, 24 May 2025 00:23:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143158268e9d8cc97f2b7f7d22ac3a3e4d2de4e9757d680a99762648f241736b`  
		Last Modified: Sat, 24 May 2025 00:23:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bf40d8ee540935c7d1cf46a9a739fbd5e4896af5ee60f96a1ac9592410bf94`  
		Last Modified: Sat, 24 May 2025 00:23:20 GMT  
		Size: 22.3 MB (22279213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25cc3aab05ca82eb9814b69b3dbaded9d5abf57a18300db2d97eabf4f15645a`  
		Last Modified: Sat, 24 May 2025 00:23:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd42897d40d8c74a99f11996e69177ea6604d66fb384292013948edaaafcea8`  
		Last Modified: Sat, 24 May 2025 00:23:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ffcbcf45cb2a43d118db419d2e5d0c9de2ef2aa09eb900e5f68ec5e8e49db6`  
		Last Modified: Sat, 24 May 2025 00:23:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff5d903c04ccd00920f42fe293681f173c3027bd53d9a5e4121ac2b9cebbc`  
		Last Modified: Sat, 24 May 2025 00:23:20 GMT  
		Size: 22.0 MB (22021514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
