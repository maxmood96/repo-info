## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:02118c1b06c1b6bb9d05ab37b35dd94c7e1c0dd592fe9aa0d5faa5ad53c93968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:ddb0a03b0b93e0ef151365a1434ec28ed6dcedd9830e53bb8d3e256794561d28
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542448283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c5b22d1a4412c091b93195a1cbdb70a7010ec0fb5cda5b879e7bc889ad8328`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 01 Jul 2025 22:21:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Jul 2025 22:21:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 01 Jul 2025 22:21:35 GMT
ENV DOCKER_VERSION=28.3.0
# Tue, 01 Jul 2025 22:21:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Tue, 01 Jul 2025 22:21:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 01 Jul 2025 22:21:53 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 01 Jul 2025 22:21:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Tue, 01 Jul 2025 22:21:56 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Tue, 01 Jul 2025 22:22:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 01 Jul 2025 22:22:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Tue, 01 Jul 2025 22:22:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Tue, 01 Jul 2025 22:22:14 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Tue, 01 Jul 2025 22:22:27 GMT
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
	-	`sha256:4d4247be1ba846daa3fff1f91d7704490c45e0f0c7e12c764e4684cbd59a9e8b`  
		Last Modified: Tue, 01 Jul 2025 22:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d996ab8536fd774b1d71f41f17c80420cedc365048a69eef4a3c829bd35c6fe6`  
		Last Modified: Tue, 01 Jul 2025 22:26:01 GMT  
		Size: 412.5 KB (412534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c6813a65aefe518242d4d1ecdb5870d73d6f36c0661b88016cf58359fe2abd`  
		Last Modified: Tue, 01 Jul 2025 22:26:01 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ac121381034a13bb8d6cbbc4d3c2805d53bbb818250c193fc421a6b11e6bff`  
		Last Modified: Tue, 01 Jul 2025 22:26:01 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8b902a8c9c76695b5fb602b442f6406ea61913e1b8b8bf00edb27efbed12c1`  
		Last Modified: Tue, 01 Jul 2025 22:26:05 GMT  
		Size: 20.9 MB (20880164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbd32a271337fcd4512191cb2e51d6b9b54e5cf312eaf1d2f8c738b2b0a8cbe`  
		Last Modified: Tue, 01 Jul 2025 22:26:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bd85d458d3583353d6ff0631e4d6bdf340ade92ba6a701660c538c7a53c515`  
		Last Modified: Tue, 01 Jul 2025 22:26:02 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1155815a14f75299d5b217ec0ef7eb2a956cfff7e9e420e8af15a27ac85b46`  
		Last Modified: Tue, 01 Jul 2025 22:26:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debb13848925fea7d77377b2dd535b14d115dca262f9714e4522d9624b8d1cff`  
		Last Modified: Tue, 01 Jul 2025 22:26:09 GMT  
		Size: 22.7 MB (22702460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba26e010f890be0f132fb8f7ae42e6cda9271e214372b36dffa3f6a66a658b34`  
		Last Modified: Tue, 01 Jul 2025 22:26:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb8a9ee7267f07d620a05e3b72043b7601b4db3f35518b3161c04931f3bd0f7`  
		Last Modified: Tue, 01 Jul 2025 22:26:01 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a648ceae9075bb26a548ad0a941ba9ce339ebf4ccb7efe730e00b1b5c8dd21cb`  
		Last Modified: Tue, 01 Jul 2025 22:26:01 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e651bbfe20a3e05a42d6cd43ae8e74d5a1d21023072f1a2b1df09bdabbdf46b1`  
		Last Modified: Tue, 01 Jul 2025 22:26:04 GMT  
		Size: 22.3 MB (22267376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:aecbec852b14417d690dbbd9c656a3ebbed312c00f77d3f15ca656c87ad2877c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346347326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08d2472f43cbf29b8fba22451ab4fc567400e71ff4ed8e946d4bd3a591060ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 01 Jul 2025 22:15:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Jul 2025 22:15:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 01 Jul 2025 22:15:52 GMT
ENV DOCKER_VERSION=28.3.0
# Tue, 01 Jul 2025 22:15:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Tue, 01 Jul 2025 22:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 01 Jul 2025 22:16:06 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 01 Jul 2025 22:16:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Tue, 01 Jul 2025 22:16:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Tue, 01 Jul 2025 22:16:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 01 Jul 2025 22:16:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Tue, 01 Jul 2025 22:16:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Tue, 01 Jul 2025 22:16:20 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Tue, 01 Jul 2025 22:16:30 GMT
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
	-	`sha256:c34ce2f5ffab9d2b30062e78bf38c25924659f8d7881c852e9a2cf0a0bb637ce`  
		Last Modified: Tue, 01 Jul 2025 22:16:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969f7b465d669090673f3f405ce3a9fce184900e34d885809e2e71ace719778b`  
		Last Modified: Tue, 01 Jul 2025 22:16:49 GMT  
		Size: 364.4 KB (364396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5a7dd1cd0ff401ad6b175a8f65c1b735c6ed12a4f5a1407764ef3f632b6a87`  
		Last Modified: Tue, 01 Jul 2025 22:16:47 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1c43f0d57eb84cf04e76de54b0978f850b8772535af13269ba4f2fdf433cde`  
		Last Modified: Tue, 01 Jul 2025 22:16:48 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f539bae843e9ea19d2a645d48d8a16eb5c6271c1a2a1c25012424366e68d37`  
		Last Modified: Tue, 01 Jul 2025 22:16:50 GMT  
		Size: 20.8 MB (20835793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8e43637f2bd629de2ad409b17fa90d2b0614b91b32c9b0ef6c5e2543059e4`  
		Last Modified: Tue, 01 Jul 2025 22:16:48 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde35242eaddb77fae19293d16f2fe8f3a5a5318be6d1705136ab167fdce692d`  
		Last Modified: Tue, 01 Jul 2025 22:16:48 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d664af8a3f6ed57c353cc0e34e23ca120fefa63d9cf59af538c3a262557fc910`  
		Last Modified: Tue, 01 Jul 2025 22:16:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85391cf02d7428040023878c265d32c88cc36adf7427d6ce36568069b35db8c`  
		Last Modified: Tue, 01 Jul 2025 22:16:51 GMT  
		Size: 22.7 MB (22662267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2a71e03dac42a09ad963912aca025dc348a957514f5db834d13f8f00fd9ad`  
		Last Modified: Tue, 01 Jul 2025 22:16:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdaf45a9d75254e2ef1f770965514be74d43302d6a44137b9f424c0f3474ab1`  
		Last Modified: Tue, 01 Jul 2025 22:16:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a8dcdcf488191a982ee37748eb2ba4fa9069256e5b969b628fe90fd720da9`  
		Last Modified: Tue, 01 Jul 2025 22:16:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ccd5ef92bed481c28528d9058b1c45cf1d044de6af4fb2ee565c46addfb760`  
		Last Modified: Tue, 01 Jul 2025 22:16:46 GMT  
		Size: 22.2 MB (22221555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
