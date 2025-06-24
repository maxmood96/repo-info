## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e2cdd6a57683c1c1e3702694a157ebe3c86ec9a3ae7d3f1be3c7931ec7e19741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6d36a4dd31a6e8e9089973e626e80844736ffd2caf26420883e0233ae22ae4fa
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541990230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdfdc9ed275d56351166ae8346b0b37912133426c8c01ccf080528b48e988c1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 24 Jun 2025 18:31:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Jun 2025 18:31:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Jun 2025 18:31:10 GMT
ENV DOCKER_VERSION=28.2.2
# Tue, 24 Jun 2025 18:31:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Tue, 24 Jun 2025 18:31:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 24 Jun 2025 18:31:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 24 Jun 2025 18:31:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Tue, 24 Jun 2025 18:31:26 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Tue, 24 Jun 2025 18:31:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 24 Jun 2025 18:31:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Tue, 24 Jun 2025 18:31:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Tue, 24 Jun 2025 18:31:37 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Tue, 24 Jun 2025 18:31:47 GMT
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
	-	`sha256:e60d9c363e28952ba91cfa2dedb99ba52bc28be941457d28ab0fe34b05a9b062`  
		Last Modified: Tue, 24 Jun 2025 20:08:40 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5deee4d15825181e582b4cd94669df3605233fd763369b9de5695de6c5cf92a`  
		Last Modified: Tue, 24 Jun 2025 20:08:40 GMT  
		Size: 401.5 KB (401545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ca7a62cfdfc8369a9bbf6577fadcc1dd65f57a777de234e4cb74aeda209ef5`  
		Last Modified: Tue, 24 Jun 2025 20:08:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125619808c89d2f04d7709ddccf0a51d79e3340c0bb94315e33f3c3f33546923`  
		Last Modified: Tue, 24 Jun 2025 20:08:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e24fad4212b27f95ff0408c6627dbd1e4951be3b73ed6144a84eb7ed8a09175`  
		Last Modified: Tue, 24 Jun 2025 20:08:43 GMT  
		Size: 20.5 MB (20490184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de7fdcaa3495104b97116690395691553b4a173056ffc54d4182962cac5821f`  
		Last Modified: Tue, 24 Jun 2025 20:08:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf20b16e6762c1294f3bcc32adbb774ac8e21ce659ff4063ecbfd9ebaed5e83`  
		Last Modified: Tue, 24 Jun 2025 20:08:41 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4be037c7eeb331991e2ba51bf8c02ea9f6b196d70537aeedda8e33a85c9124`  
		Last Modified: Tue, 24 Jun 2025 20:08:41 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad4adac830307c4b39586f0445107d0f8942b935177a1b3807d9d2a37a6f45d`  
		Last Modified: Tue, 24 Jun 2025 20:08:49 GMT  
		Size: 22.7 MB (22686724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea8c437fa9cbeafad82b04c5b41a0109a331d4d435e9cce77fb343b663ce818`  
		Last Modified: Tue, 24 Jun 2025 20:08:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca7187c9bcebf36d87cb5930d2e5ae54d49a4912cb1ab0d8fdcb6080b484f84`  
		Last Modified: Tue, 24 Jun 2025 20:08:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91a1219b5be807b02e57c6c64cf0795e61fb32484c3b2567c1ec1d9913927d1`  
		Last Modified: Tue, 24 Jun 2025 20:08:43 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f299587256b519e0a1035d7c75cea5f36aeadc9c008c064e240b24e3b38e1e3a`  
		Last Modified: Tue, 24 Jun 2025 20:08:46 GMT  
		Size: 22.2 MB (22226002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:47090ef1033cf65c96b7d9ef5347b3ee5e2338760b162134e62b201432d75779
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345839802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21a28b6e60030937fb91d70b82f1d3f3fcfeca3e11f7dba4a22bba6a81caab6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 24 Jun 2025 18:25:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Jun 2025 18:26:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Jun 2025 18:26:25 GMT
ENV DOCKER_VERSION=28.2.2
# Tue, 24 Jun 2025 18:26:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Tue, 24 Jun 2025 18:26:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 24 Jun 2025 18:26:49 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 24 Jun 2025 18:26:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Tue, 24 Jun 2025 18:26:50 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Tue, 24 Jun 2025 18:27:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 24 Jun 2025 18:27:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Tue, 24 Jun 2025 18:27:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Tue, 24 Jun 2025 18:27:05 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Tue, 24 Jun 2025 18:27:16 GMT
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
	-	`sha256:fc03c6c047256b1984f8349212389f86c231b9244dafeaa1e0d3609d441ed96c`  
		Last Modified: Tue, 24 Jun 2025 18:27:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5fd874d7d5caa215f985bf04b7424a5dfb4075ee19d728735974f114048bdc`  
		Last Modified: Tue, 24 Jun 2025 18:27:35 GMT  
		Size: 365.9 KB (365930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7fb61211421f45d92f676ab3eacd8af9d258ddb0a75785d97c5bf455a4498a`  
		Last Modified: Tue, 24 Jun 2025 18:27:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12498e5a4e8c28ca867efed76210de2a67a0d2e3aaf7a44c3741a8c4cdd56157`  
		Last Modified: Tue, 24 Jun 2025 18:27:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05098dc55c356aa8c534ad8079ae6f01eb95c2a0fde6cca587c597a6ed956c05`  
		Last Modified: Tue, 24 Jun 2025 18:27:40 GMT  
		Size: 20.4 MB (20426963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb281c078d4484e0c9fd64447450edf81965a59f87573ac60a8ca8a207592674`  
		Last Modified: Tue, 24 Jun 2025 18:27:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7726c253c9d167e360bd9f3a9ca47b206400279de2fa9a49427a991a457343`  
		Last Modified: Tue, 24 Jun 2025 18:27:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07abaa3834c64ec52eb9fe01c18bc6f8e7dcd278df4c06d3b7a62b5c917946c9`  
		Last Modified: Tue, 24 Jun 2025 18:27:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddfdfb8304fa81e6ccfcccd76601f42924d7a093e7c565d9a2ce2ec09d46644`  
		Last Modified: Tue, 24 Jun 2025 18:27:44 GMT  
		Size: 22.6 MB (22625653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd739707b8290f94595aafecd6674c3812b8c50864e784760ec4593a5a6838f`  
		Last Modified: Tue, 24 Jun 2025 18:27:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77f83da1c1caacb9d4da26dd99a6786027fd1382de120a58aec7dd33a11ec0d`  
		Last Modified: Tue, 24 Jun 2025 18:27:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc058fb3e13deba36cdea4f490ba99d5d1c020ae7e6dc543716dc92e00f5a4c`  
		Last Modified: Tue, 24 Jun 2025 18:27:46 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2366c95adaf8fd0e70f29f988e6c2ebeb6995df6db5d68a6445b744fce3a28c5`  
		Last Modified: Tue, 24 Jun 2025 18:27:50 GMT  
		Size: 22.2 MB (22158120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
