## `docker:27-rc-windowsservercore`

```console
$ docker pull docker@sha256:ae9e4f643320087e8d9325c01834b365f6d72cb6ca6ff3250fd735806e9450cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27-rc-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:3cc46ce17eba4c8e79dba10dfde41b6376a1d108162d0cb1f4b22a6e939c8bc6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520627919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c8132f6d8fc4b49ae6ee6e0b3f5df786b5331459eaa10635f99f0f3c07b3d1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 13 Sep 2024 18:58:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Sep 2024 18:58:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 13 Sep 2024 18:58:47 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Fri, 13 Sep 2024 18:58:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.3.0-rc.1.zip
# Fri, 13 Sep 2024 18:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 13 Sep 2024 18:58:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 13 Sep 2024 18:59:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Fri, 13 Sep 2024 18:59:00 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Fri, 13 Sep 2024 18:59:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 13 Sep 2024 18:59:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Fri, 13 Sep 2024 18:59:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-windows-x86_64.exe
# Fri, 13 Sep 2024 18:59:12 GMT
ENV DOCKER_COMPOSE_SHA256=8603f4e6936e752793f7edf3f45ed67cb1b8ed8c7b1dabc5721384299bfebd7f
# Fri, 13 Sep 2024 18:59:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add4b0d245f7ee3cb505aa482e81bc11a0b20b29260af3c84344beb6cd5581ef`  
		Last Modified: Fri, 13 Sep 2024 18:59:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ee1e5ed99cc4d2b8e143f25f3fe5cd14f3ad2fd755b95b993671fa77720288`  
		Last Modified: Fri, 13 Sep 2024 18:59:30 GMT  
		Size: 352.5 KB (352541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7aadcf9eb550ba7345a0e4bbd26f780264c8d95bef3be4452ce1f561da74a3f`  
		Last Modified: Fri, 13 Sep 2024 18:59:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a5a4ca391d71d386c356f0283aecffff2fccfe606774537219a92e497352ab`  
		Last Modified: Fri, 13 Sep 2024 18:59:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ce43b903466ad60b3c7c5fba1da74c6c86d64bad1a44ec68b37b6c430ef1d7`  
		Last Modified: Fri, 13 Sep 2024 18:59:31 GMT  
		Size: 18.9 MB (18883873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e74afbd05af617e1d011b4bec143b15e2e92cf70b4ca886f349f4770ab48f36`  
		Last Modified: Fri, 13 Sep 2024 18:59:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555120e2d7f1edfad8e874bf0ac40ae684d6bee6e51e94b3a9c544626a9fd989`  
		Last Modified: Fri, 13 Sep 2024 18:59:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3f4859e784dcecdad6d6b622312f63187f4d9778eb958f1ddc5760e674e5e8`  
		Last Modified: Fri, 13 Sep 2024 18:59:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e6062ca34e806e5d138a4ddfabdc1968a9660432c027a5c2a9ba39a2637286`  
		Last Modified: Fri, 13 Sep 2024 18:59:28 GMT  
		Size: 19.3 MB (19277377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d3db2bceee7d40b49d8391bd946ac376ae96304c058d472d6f678e954d2a90`  
		Last Modified: Fri, 13 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cf4647561d5a19a1c3e0c836c17540694f0ee78bc65a5f935986d88bceca00`  
		Last Modified: Fri, 13 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1779e1c24b901dafd652dbbafe10ff623f47618e4d13a14d16c6a61d51f9d519`  
		Last Modified: Fri, 13 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab0e25e0b7d0c463fa631baca221ff45d8e5dbfa95318eebc2f1627eda8dd69`  
		Last Modified: Fri, 13 Sep 2024 18:59:28 GMT  
		Size: 19.9 MB (19910106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-rc-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4460f3ce02badf6f8cbc5e604ee3e7ede3eb9a67cfc58fa34fb888e5a319fe34
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778688223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7362cd8797766c6974ae0f252d547a9528b22c7cf2e217c454015d19d5e441`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 13 Sep 2024 19:02:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Sep 2024 19:02:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 13 Sep 2024 19:02:29 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Fri, 13 Sep 2024 19:02:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.3.0-rc.1.zip
# Fri, 13 Sep 2024 19:02:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 13 Sep 2024 19:02:44 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 13 Sep 2024 19:02:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Fri, 13 Sep 2024 19:02:45 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Fri, 13 Sep 2024 19:03:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 13 Sep 2024 19:03:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Fri, 13 Sep 2024 19:03:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-windows-x86_64.exe
# Fri, 13 Sep 2024 19:03:04 GMT
ENV DOCKER_COMPOSE_SHA256=8603f4e6936e752793f7edf3f45ed67cb1b8ed8c7b1dabc5721384299bfebd7f
# Fri, 13 Sep 2024 19:03:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5b2a56b1294bb42f14de2b93125178a1dab32a6fb1c710dd21165619bbe3bd`  
		Last Modified: Fri, 13 Sep 2024 19:03:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e751a300c7f21c5f257a02c3d37957bc0c086888351cf3f9ba23f2bcb2ed8927`  
		Last Modified: Fri, 13 Sep 2024 19:03:30 GMT  
		Size: 339.5 KB (339466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9027565737b42c3b7d10c4fa8921edaec7c1fe7e1027931ab89da97c95a58c`  
		Last Modified: Fri, 13 Sep 2024 19:03:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486d811f971529ac60838d9a2c312435789373e44a4b3a664decb547ad6de00d`  
		Last Modified: Fri, 13 Sep 2024 19:03:29 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7469756e7f75c2c4548e828812a8171562a8dba59f6f9d62ab87ced07ef7584`  
		Last Modified: Fri, 13 Sep 2024 19:03:30 GMT  
		Size: 18.9 MB (18885743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9869745de4c52405c2cbe9128123c3cce344c8ba2e77e024021bad7465db191`  
		Last Modified: Fri, 13 Sep 2024 19:03:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f8970616a050f75d02fb22ffed814b91e26daabc82eb2988d55ba4ae904c91`  
		Last Modified: Fri, 13 Sep 2024 19:03:28 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c78a9f6e37080e8d747c47f83982c6b5aa0625042e7d4af05fc90cccb9716d`  
		Last Modified: Fri, 13 Sep 2024 19:03:28 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b55e730e49d2bc55e6dcf6515fe02b75c3ee7ac602328508777364e5287bb7`  
		Last Modified: Fri, 13 Sep 2024 19:03:29 GMT  
		Size: 19.3 MB (19278060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d975764db384c7c1c478ff0088991d1c106e808efe6117629a68e57dbc87a9b5`  
		Last Modified: Fri, 13 Sep 2024 19:03:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f38c98e1a4d62c0fc88635903a5e720833ecd0c148f50c7f41afb950a650804`  
		Last Modified: Fri, 13 Sep 2024 19:03:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7cb00fb9682c6fa0afbec4ab5a1b272f76efdd08fdd630d3653121eb0cc299`  
		Last Modified: Fri, 13 Sep 2024 19:03:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eac0463b9f845876bd053999cde5dfd8c064879f81ef78a7f0ad7339bc03e20`  
		Last Modified: Fri, 13 Sep 2024 19:03:29 GMT  
		Size: 19.9 MB (19904776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
