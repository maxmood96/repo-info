## `docker:25-windowsservercore`

```console
$ docker pull docker@sha256:6db575706d6cc46931174b32d61f86fbeacbadf9d193919162251e65ce7dd5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `docker:25-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull docker@sha256:9734bceb9744c54e1a853bb1fd0f1db22fe1772f99cbf83995871e76d1cdbc7f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169575869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cf3f914b2938a05aae07b735d6d9948ef0d81fc71bf76ff5cf89bbb2ef873d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 22 May 2024 22:54:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 May 2024 22:55:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 22 May 2024 22:55:54 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 22 May 2024 22:55:55 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Wed, 22 May 2024 22:56:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:56:12 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 22:56:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 22 May 2024 22:56:13 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 22 May 2024 22:56:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:56:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 22:56:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Wed, 22 May 2024 22:56:28 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Wed, 22 May 2024 22:56:38 GMT
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
	-	`sha256:526b66fa82fe7c7dfff7dacc419dc815015321fb516fa5d3aa789a789a43586c`  
		Last Modified: Wed, 22 May 2024 22:56:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f248ed46debc382cdc6f344951bbbbd61935ecde28629f49880abca2a162796`  
		Last Modified: Wed, 22 May 2024 22:56:44 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97c108b7a2f972a4f7d1bfb784996a1cbcfd8b746d08bdec4b8d74f9e1af56f`  
		Last Modified: Wed, 22 May 2024 22:56:43 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0126f1ea09470d3cf8e42dcd281cb94a1a4a2939c03b32e795b8a068a2aef6`  
		Last Modified: Wed, 22 May 2024 22:56:42 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdcff025c15a38be1b55c22ddf0d4fbef8cbdece0ae85b13e9fdf94849e274c`  
		Last Modified: Wed, 22 May 2024 22:56:44 GMT  
		Size: 18.0 MB (18037916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a689b649515e09a06f8cbff8db74642245aeb249ab79ffe16f5dfd54572c71`  
		Last Modified: Wed, 22 May 2024 22:56:41 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894a38aa56a69899c1d7b8b1765dc5a384c3320bf62925866947db283a43b65e`  
		Last Modified: Wed, 22 May 2024 22:56:41 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7ee39062970bfdc8cb5adb418e3474b2038e88bc8f195cffffe2331dce3ad4`  
		Last Modified: Wed, 22 May 2024 22:56:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153efff34ff8b91bad2c7c4cf5fcddb51ce60a935bdd38295649336635028672`  
		Last Modified: Wed, 22 May 2024 22:56:43 GMT  
		Size: 18.9 MB (18897609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7f4e8cd7a951f73ea6f90bdb11e4060ac9091c5a854c906e40e02f7c53d1ac`  
		Last Modified: Wed, 22 May 2024 22:56:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186fa6ef0b15ee8123d26930a4acb353273e30a9f8688b66565544a48ef745d`  
		Last Modified: Wed, 22 May 2024 22:56:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640b23f896aa928ba32ccf034983a7baeaeacfb12cdc4c555d4d9e0d4f8ee070`  
		Last Modified: Wed, 22 May 2024 22:56:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9625d6cedcee3f2ca8c1b3e80e4e8556926fc53412c45aab07de371695e420`  
		Last Modified: Wed, 22 May 2024 22:56:43 GMT  
		Size: 19.6 MB (19597122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull docker@sha256:c080ed4c31af16cfb9bb1eb907a435a845550d0054395a0f1fad0ac604934c94
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2236845538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4947447fc786153512c21bc2d537968a97b377fff4ade49363e0529972e305d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 22 May 2024 22:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 May 2024 22:56:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 22 May 2024 22:56:45 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 22 May 2024 22:56:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Wed, 22 May 2024 22:57:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:57:16 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 22:57:17 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 22 May 2024 22:57:17 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 22 May 2024 22:57:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:57:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 22:57:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Wed, 22 May 2024 22:57:48 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Wed, 22 May 2024 22:58:14 GMT
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
	-	`sha256:2b031c4c4f1cf1ae6904bb4ae3aa2f2800ed159db0698aa767492ec2517a9894`  
		Last Modified: Wed, 22 May 2024 22:58:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e34afff4b29125f3bd19e4bf756a7685760f4d98dd051a9ea3ab0f73e711da`  
		Last Modified: Wed, 22 May 2024 22:58:24 GMT  
		Size: 484.5 KB (484508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b741b4336051a3e263df23513a739bd5ece9294da37953cbfe1b1da2669df7`  
		Last Modified: Wed, 22 May 2024 22:58:23 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46d465852c9253dd22a217c6edcf691c89a1c27cbd1658769a18aed090c2afa`  
		Last Modified: Wed, 22 May 2024 22:58:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76267212d7123dabf5544649bde450af9fa52a05362c36929f7f094c1e09e5e9`  
		Last Modified: Wed, 22 May 2024 22:58:24 GMT  
		Size: 18.1 MB (18076717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adc33686f5dc049177c2aed326ae443fd38321932069df89fc12970f3e011d5`  
		Last Modified: Wed, 22 May 2024 22:58:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d894d61d19b1d89e39cab61988fee5265fe2e6a7d895f7eee0650ae833947d37`  
		Last Modified: Wed, 22 May 2024 22:58:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1367f99f044ff0be20ffee491ea0796fa49965d7eeb92c0c484bc5f48ac5c3c`  
		Last Modified: Wed, 22 May 2024 22:58:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e760dd82670df54b6a12b3d2fb69345c8934f7dc971abc1da134cc2529a81844`  
		Last Modified: Wed, 22 May 2024 22:58:21 GMT  
		Size: 18.9 MB (18930600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656abdf944dc53666b8cef733762182504358ec7e49e51e8fe2abaf4b29264c7`  
		Last Modified: Wed, 22 May 2024 22:58:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba164a53559cf38416f49f06b427245e3c3ecc177f249cc476fd30d45e0c25`  
		Last Modified: Wed, 22 May 2024 22:58:18 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17e7625a5acdaf868fcb1902ed844ad8bfd82e0b5337575368c67f57de8b419`  
		Last Modified: Wed, 22 May 2024 22:58:18 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66144400c9e95197fb31f2d1502fe863f8ec3db337dcb1f7677f84b359c68943`  
		Last Modified: Wed, 22 May 2024 22:58:21 GMT  
		Size: 19.6 MB (19630558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
