## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:683cb42bfa096b82aafb52a6e9a7770a2e6a587d99597d1b0a831dad23bc44d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:526a41abe0fa633d055ea2277721319b391ad0cb29238ed528c1c4fb865d2ea5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2196457944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1c328a5bd4ded6a7578228bfbc79086fa4e6dd6a701501dbbdcf588503d374`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 24 Jul 2024 02:03:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jul 2024 02:04:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 24 Jul 2024 02:04:40 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 24 Jul 2024 02:04:41 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 24 Jul 2024 02:04:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 02:04:57 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 24 Jul 2024 02:04:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Wed, 24 Jul 2024 02:04:58 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Wed, 24 Jul 2024 02:05:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 02:05:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 24 Jul 2024 02:05:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Wed, 24 Jul 2024 02:05:09 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Wed, 24 Jul 2024 02:05:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc30258fb25bba20d93604f52659026f8378f156da7e8ae5ef6af96027f2201a`  
		Last Modified: Wed, 24 Jul 2024 02:05:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb72da1f10781ed658f1acbcb46c3c85b452b72e4cc9f24481d728763672c732`  
		Last Modified: Wed, 24 Jul 2024 02:05:29 GMT  
		Size: 358.6 KB (358599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b38629fe8b8ee4b8e8ca96e948701e87960c26f8642e5a794d8ce790e4edd0d`  
		Last Modified: Wed, 24 Jul 2024 02:05:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb8e9f82c92fc3c30d5009bd896293dd88660e54240d3e7560132016b3e2e64`  
		Last Modified: Wed, 24 Jul 2024 02:05:28 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552f93e7fa80a440fb9eb9daa202c0f341fc3011f170c877e973303aad6e1fe4`  
		Last Modified: Wed, 24 Jul 2024 02:05:30 GMT  
		Size: 17.5 MB (17534188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8159159a5492b54f6a31c3ed7ffa6fcf1237c73390b3b5729d9ba278b19c9468`  
		Last Modified: Wed, 24 Jul 2024 02:05:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ebe9650c20e3ad8a3e996c95909a188333942289d35be48a462a722f03c324`  
		Last Modified: Wed, 24 Jul 2024 02:05:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f68044a4bf951fd1b0a3266aa3f53878add3e9555e72b460276ef9099af7121`  
		Last Modified: Wed, 24 Jul 2024 02:05:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c021b96d66d1ec5de001b652566a04f27b4c017a7381d83ab7c7e0f8f96cc1`  
		Last Modified: Wed, 24 Jul 2024 02:05:27 GMT  
		Size: 19.3 MB (19258562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed94fd1993b82368c7d73a3c21570521586063f954bdbf01321affddd86544a`  
		Last Modified: Wed, 24 Jul 2024 02:05:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f759b28448225c7cd6016a5332da994e50fe83d6b18f6ee4e78664857b82d92e`  
		Last Modified: Wed, 24 Jul 2024 02:05:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0500836580d35e6d353d0d8b166ca7f539bf06580c6388a733ac9160173d58e`  
		Last Modified: Wed, 24 Jul 2024 02:05:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a0f5cc18cf1b88a3ab1f68f1a832f51c9b0093b8eed10f59dc95fe632f9d06`  
		Last Modified: Wed, 24 Jul 2024 02:05:28 GMT  
		Size: 19.7 MB (19694719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:2c29a86bdaf0bb77677826496ba18363372a8eac0b9e8bcb77d7685dc7ab8105
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295438743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de75beefc047078810b27441693e65b335ef9a0eb32b20c2463fddc1effb803f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 24 Jul 2024 01:08:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jul 2024 01:09:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 24 Jul 2024 01:09:18 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 24 Jul 2024 01:09:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 24 Jul 2024 01:09:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:09:46 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 24 Jul 2024 01:09:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Wed, 24 Jul 2024 01:09:48 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Wed, 24 Jul 2024 01:10:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:10:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 24 Jul 2024 01:10:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Wed, 24 Jul 2024 01:10:13 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Wed, 24 Jul 2024 01:10:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85872446d0fdc095844eb22ca326aea840d66b1532222bff450e83fbea642ffd`  
		Last Modified: Wed, 24 Jul 2024 01:10:44 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a15713bce77def72cb79ad73bf8ea05345cfb017faa728536afee992f1ab3d`  
		Last Modified: Wed, 24 Jul 2024 01:10:44 GMT  
		Size: 498.7 KB (498669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8681ffef0997f8f0ebd8d146ea125578d42d5c19f9efaceaf13c55cce7952b1`  
		Last Modified: Wed, 24 Jul 2024 01:10:42 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ad19253b9ce88f4cd537a76e16e82e970366488537e3b7e39a5b7323156904`  
		Last Modified: Wed, 24 Jul 2024 01:10:42 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ca42fa4e95bce8abb3b28d3e12396b7876468f9cc84581caae4b16fd242ce5`  
		Last Modified: Wed, 24 Jul 2024 01:10:44 GMT  
		Size: 17.5 MB (17542057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0869c3c3711fcea3b7f47d52a1cf4195c888abab151959727b42597b64eb077`  
		Last Modified: Wed, 24 Jul 2024 01:10:41 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf2dbba887f1fefccc406be694e299f8dd5a4c7704fd58d140af53a5b2ef72c`  
		Last Modified: Wed, 24 Jul 2024 01:10:40 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58844b993bd3b92f24b5c119141ee187f24533de1c300e85f6e77de251d2e5dd`  
		Last Modified: Wed, 24 Jul 2024 01:10:40 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4538466b9caeef81d0f9f9e275c52012f6b99162e471359945d0c91057bd3cb`  
		Last Modified: Wed, 24 Jul 2024 01:10:41 GMT  
		Size: 19.3 MB (19263814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fc17d0302ed06054301a5bcbdd17c294c767323496ce47b0520d177450bbf5`  
		Last Modified: Wed, 24 Jul 2024 01:10:39 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029998499d8392a2874287e105dcda1b70c05fedb8feb51a5f4782896e4bc5c5`  
		Last Modified: Wed, 24 Jul 2024 01:10:39 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42507910a89321140c73f52b6c5b86ad545ec33c2d27ae7911b8b34dd654dcc`  
		Last Modified: Wed, 24 Jul 2024 01:10:39 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7605448ed2870b536974a3e91b7cdb1ee55f3336c28ffdf1cb7706185bb45b`  
		Last Modified: Wed, 24 Jul 2024 01:10:42 GMT  
		Size: 19.7 MB (19692549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
