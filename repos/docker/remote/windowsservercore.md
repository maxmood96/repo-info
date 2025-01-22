## `docker:windowsservercore`

```console
$ docker pull docker@sha256:8a74d0322bf882a83816a3144ef4e7c137d3fcb82f2db3c924dc0b5fbee9b21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:8738aa95416baf37d2ac650fa06aad1ac30491d96bf76f4706cbf9e596c11ce6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561298078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e710eea17af51d51562291309fa2b38baac54d7534fa4b5064c95da80b08c7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 19:34:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 22 Jan 2025 19:34:11 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 19:34:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Wed, 22 Jan 2025 19:34:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 19:34:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 19:34:23 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.windows-amd64.exe
# Wed, 22 Jan 2025 19:34:23 GMT
ENV DOCKER_BUILDX_SHA256=61123c807345d35525bc242bb182526cb0c10310eaf107bbcc97695be528c141
# Wed, 22 Jan 2025 19:34:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 19:34:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 19:34:33 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Wed, 22 Jan 2025 19:34:34 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Wed, 22 Jan 2025 19:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4623b3a80e15523c37025df0abfc8d3472d4b321fcf5030a4ca68f644606a0`  
		Last Modified: Wed, 22 Jan 2025 19:34:51 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95690585cbae61bf0b1ce60650f636093b14227666d53ad828f976b8e0400077`  
		Last Modified: Wed, 22 Jan 2025 19:34:52 GMT  
		Size: 398.2 KB (398191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029994a70aa04c265187ccaafdc20afd120104e7ee242bffa2d6d03b82c3fa1f`  
		Last Modified: Wed, 22 Jan 2025 19:34:50 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfc04ea9c6d8bed97ad758708b6b55a54df17d453c49a1df5015bd790a5f23b`  
		Last Modified: Wed, 22 Jan 2025 19:34:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543d538f2d7f68a76f78c826d06948ebea095b2bb2e51df35e32b7151ce5749`  
		Last Modified: Wed, 22 Jan 2025 19:34:52 GMT  
		Size: 19.2 MB (19212641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc56b97d2537900b8080a6f2df840ca6157d20eee0bb8eea252a94b084754d`  
		Last Modified: Wed, 22 Jan 2025 19:34:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f16f248b38a7f536b327c7de28ddf058e17cd31e3ccb5864e86f93168e1eef`  
		Last Modified: Wed, 22 Jan 2025 19:34:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905ad1bcca9ca2a06892b11f067b8ae4832ded7c13cfdb89ea5a4e1e6665790`  
		Last Modified: Wed, 22 Jan 2025 19:34:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9492105e37e29f96da3e8970e7db76c85efcad0a375ae7905c55e2ec3a47c193`  
		Last Modified: Wed, 22 Jan 2025 19:34:50 GMT  
		Size: 21.2 MB (21183762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba95801ab3cdddd6546482d46b0581c91186460ed919fe3caabda8013e65527`  
		Last Modified: Wed, 22 Jan 2025 19:34:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eab4c6ba7b43bca3523d9edf80674e258e34b120dd04aca877ea577d752aa5e`  
		Last Modified: Wed, 22 Jan 2025 19:34:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bad5a26e89d40c2b42c1fec86c81717231e566401408b370209a4cc32059ed2`  
		Last Modified: Wed, 22 Jan 2025 19:34:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d949e7138c7f2adabada256d9151550b9ce92c1934e2e0b5708729967e3a7620`  
		Last Modified: Wed, 22 Jan 2025 19:34:49 GMT  
		Size: 20.2 MB (20214126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:f487420a3562f387d41b7300b3af749a3be8510d4a2308758a6def6a950931c4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323241515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38a5c149770b85dd28da0d8d342e17595533f90b779a65f270eb4b05b1a0d45`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 19:29:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 19:30:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 22 Jan 2025 19:30:55 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 19:30:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Wed, 22 Jan 2025 19:31:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 19:31:13 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 19:31:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.windows-amd64.exe
# Wed, 22 Jan 2025 19:31:15 GMT
ENV DOCKER_BUILDX_SHA256=61123c807345d35525bc242bb182526cb0c10310eaf107bbcc97695be528c141
# Wed, 22 Jan 2025 19:31:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 19:31:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 19:31:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Wed, 22 Jan 2025 19:31:26 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Wed, 22 Jan 2025 19:31:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d69d7b1f3492404b3fbf4b458db167cddaf1e4d695e3bfca657c6ae44af302`  
		Last Modified: Wed, 22 Jan 2025 19:31:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fd5886e7bfceda69a8b8ab4a48ac5f45c90cf476852f953c9a4422384e31c2`  
		Last Modified: Wed, 22 Jan 2025 19:31:42 GMT  
		Size: 360.8 KB (360821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bcb64d7130550a7f8b53fa95fd9c3b23baf7f4458490daa4ce3fe4b4248bd3`  
		Last Modified: Wed, 22 Jan 2025 19:31:41 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f84a2a4da7975a0b9c8a0d69c00de6f28d68d3dcfb4d084e56337834e23f0c5`  
		Last Modified: Wed, 22 Jan 2025 19:31:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e7b8568c83315eb21b5deb30a7a3eb2fdd461927bc1f00242d425488bbffdf`  
		Last Modified: Wed, 22 Jan 2025 19:31:43 GMT  
		Size: 19.2 MB (19167781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39f00d3092ec26d063dd2a0cfbc130b508cec4d702c75fc8a12fd6ef94d3f3`  
		Last Modified: Wed, 22 Jan 2025 19:31:40 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4925e34b1a29301b3a0e9958244243792432ee96e98467a157f0c3c8ad72b490`  
		Last Modified: Wed, 22 Jan 2025 19:31:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff8995ade954c14d51ab28b59a51b8dabee148a76dcdcbdfe22bc89ae919d54`  
		Last Modified: Wed, 22 Jan 2025 19:31:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90c3867b712d242cadd78e02b2781aa3ad0084321d596b50cdbd9874d2b5e1a`  
		Last Modified: Wed, 22 Jan 2025 19:31:42 GMT  
		Size: 21.1 MB (21141927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5709458e0b9e396e0e72bda2011a52d869c5e4d9e100f2cfd4c7cdd6ef64b339`  
		Last Modified: Wed, 22 Jan 2025 19:31:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83a3e46d62a059516c22168ed9ee2c23b38d62349316d5db956ce8069c4ebc7`  
		Last Modified: Wed, 22 Jan 2025 19:31:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0fc10422fb7f442c131f1fdee13eb470bd2302a2abf58dbf20a66d3471a098`  
		Last Modified: Wed, 22 Jan 2025 19:31:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff2786219ccaa990d210e115f4b9782696f82df961fae7fba12325893c12911`  
		Last Modified: Wed, 22 Jan 2025 19:31:42 GMT  
		Size: 20.2 MB (20174186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:76ad0f7103ff786ac89a66d0b42a24b839cc626c3eebe9e03a2cce76eddbc41e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183013128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335189a32d62231db6612eb446761c2630e34cd3d0983f82d78a452cf3362aeb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 19:29:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 19:31:15 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 22 Jan 2025 19:31:16 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 19:31:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Wed, 22 Jan 2025 19:31:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 19:31:35 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 19:31:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.windows-amd64.exe
# Wed, 22 Jan 2025 19:31:37 GMT
ENV DOCKER_BUILDX_SHA256=61123c807345d35525bc242bb182526cb0c10310eaf107bbcc97695be528c141
# Wed, 22 Jan 2025 19:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 19:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 19:31:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Wed, 22 Jan 2025 19:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Wed, 22 Jan 2025 19:32:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93afba7fb970855c1ddf9b0f3091830388ee0546f5af752598227c79d86042cc`  
		Last Modified: Wed, 22 Jan 2025 19:32:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b8887dcb2ea4a956a3651f2a21c65800ee83d862239391d7c1ae623ea8d95f`  
		Last Modified: Wed, 22 Jan 2025 19:32:16 GMT  
		Size: 338.3 KB (338262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04743ae40fed017dcd78cb8bd6ffed61d89a9e9d68232e6f0fea38af98aa25d1`  
		Last Modified: Wed, 22 Jan 2025 19:32:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a77bc0a341102a70dc984240bed913f37664caff8f7a789dcd1e25793dd06a3`  
		Last Modified: Wed, 22 Jan 2025 19:32:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a23481ff498647575cdb0eb478504132c920ceb8637facf27305a86cc487b`  
		Last Modified: Wed, 22 Jan 2025 19:32:16 GMT  
		Size: 19.2 MB (19161808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da64303ab75712faa759e3a6ee73cb292ceb2b9c793e59c741362cdc5b4ce426`  
		Last Modified: Wed, 22 Jan 2025 19:32:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868df40f0d9ec9e896f07edebcf7e8dfe8f84a96dd04b2c0da0c264a7bca6424`  
		Last Modified: Wed, 22 Jan 2025 19:32:14 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e874d39ca205dab7e3fc3be0b947d1bfa75346b93cc103e9fb09ff1a8f04c822`  
		Last Modified: Wed, 22 Jan 2025 19:32:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0827fdca682a4a4d5d97a70d0822480927f3fb3dcacb0473ee0d04a91e66d80f`  
		Last Modified: Wed, 22 Jan 2025 19:32:15 GMT  
		Size: 21.1 MB (21127062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e741ad32c4a5aadd55ffc26a8a78d748131b7db221f73a3b9f8a1e97f4243f4`  
		Last Modified: Wed, 22 Jan 2025 19:32:13 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0861fe2eb5e270ae3eaa9fb0df01b0775debc3d56855ee9da811664f8e2bcfd`  
		Last Modified: Wed, 22 Jan 2025 19:32:13 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f60e9eb31040efd0afd664b5f9b9006b2370f654b87f7bf70e1f8bf5d431d`  
		Last Modified: Wed, 22 Jan 2025 19:32:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c00d8ed4567d42ab7dc157fc26f90efb32a642888bbe3d1f678b73573731ff`  
		Last Modified: Wed, 22 Jan 2025 19:32:15 GMT  
		Size: 20.2 MB (20162140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
