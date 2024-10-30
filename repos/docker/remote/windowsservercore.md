## `docker:windowsservercore`

```console
$ docker pull docker@sha256:86d10bde8a5a0363f08c6756700c89d60f5b901bd1bac30e6b9f2b4d0386c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:8b68e796fe0afb36dfe0fe7a31237eb3ac7750bd2975757cf18a2cefbd03273f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857906598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdad2a89a5e019d9ac743fccd0a42c42102194938018459d6014f5298201fc15`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 30 Oct 2024 18:00:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Oct 2024 18:02:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 30 Oct 2024 18:02:02 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 18:02:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 30 Oct 2024 18:02:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 30 Oct 2024 18:02:19 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 30 Oct 2024 18:02:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Wed, 30 Oct 2024 18:02:20 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Wed, 30 Oct 2024 18:02:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 30 Oct 2024 18:02:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 18:02:31 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Wed, 30 Oct 2024 18:02:31 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Wed, 30 Oct 2024 18:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac00ebd338ab435e7708698a78fc7980c506abecb81fa1bbd2bd872b5f1faa6`  
		Last Modified: Wed, 30 Oct 2024 18:02:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da5553c7a87aa7cc32998e3caea362956197dcb830c169a7350d46c66cc37b6`  
		Last Modified: Wed, 30 Oct 2024 18:02:50 GMT  
		Size: 492.1 KB (492084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49d3c6359179e798e515b9878d2755eb1f09b96c8f9bac72aba2c1a908c5e41`  
		Last Modified: Wed, 30 Oct 2024 18:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d049fc6aa3807dc00ce7e98a2ca6950b4f069f75957bfb60c49c74f2d7b7691`  
		Last Modified: Wed, 30 Oct 2024 18:02:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38afd2937232ba61cf615f6eb7c2b92c6e718737a215b64152eac020bcff3db2`  
		Last Modified: Wed, 30 Oct 2024 18:02:50 GMT  
		Size: 18.9 MB (18853440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5d9930ac1a47ae14bcbb46a895bef74c80bffdca6d4e53d677e8137694967b`  
		Last Modified: Wed, 30 Oct 2024 18:02:46 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a86de5a8acd3f8b45f5d56699f9530be8b97645bc8ed732f937d0701560f85d`  
		Last Modified: Wed, 30 Oct 2024 18:02:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9728a8a87c67ebcafa4a6d07e9440a294dc5960179c0e8c162d5fdb4466ec9f5`  
		Last Modified: Wed, 30 Oct 2024 18:02:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7747c5fdf3f0965294c826dd648f2b2d7ed4c903332a93efef6b31299bc31cf`  
		Last Modified: Wed, 30 Oct 2024 18:02:48 GMT  
		Size: 19.2 MB (19247620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03442abe19f965387271b9790e7b3a450c7f69228aeb13057ec06398e4466be7`  
		Last Modified: Wed, 30 Oct 2024 18:02:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b606815e9c288e109059a5475a3adda2a5ab78e7ce351ba2d96792d9e4e72eea`  
		Last Modified: Wed, 30 Oct 2024 18:02:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a66ac09378abaadc268cdded1bb9ebe3875b4025535eb7c12bb66f4d42bab9`  
		Last Modified: Wed, 30 Oct 2024 18:02:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720de7a0af8449f891ab3ccde622a52cdffa89c5d5db1ae0d75a07ee8c48db4d`  
		Last Modified: Wed, 30 Oct 2024 18:02:48 GMT  
		Size: 20.0 MB (19960302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:b79a3eac3047b12643a0232286ae9e15f1101839b03f4b2b806b11e89521f440
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960448055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d3239f3a3db6c638b4491b8324ba6fa0f529d3f31d65e83c01d7933d6e821e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 30 Oct 2024 18:00:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Oct 2024 18:03:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 30 Oct 2024 18:03:10 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 18:03:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 30 Oct 2024 18:03:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 30 Oct 2024 18:03:35 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 30 Oct 2024 18:03:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Wed, 30 Oct 2024 18:03:36 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Wed, 30 Oct 2024 18:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 30 Oct 2024 18:03:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 18:03:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Wed, 30 Oct 2024 18:03:51 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Wed, 30 Oct 2024 18:04:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ecdf82d8e13162ba0139708845c91031495beb34272b1f16fdc5b7e4e3a02e`  
		Last Modified: Wed, 30 Oct 2024 18:04:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586bef5b3711e3278cc812ed163b334458667bd5b421ab4db3f7ed26844c3081`  
		Last Modified: Wed, 30 Oct 2024 18:04:07 GMT  
		Size: 482.8 KB (482782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b2f304bd7ca9d255de8e4f7d31dd9692d6ecceaa18d80f03510ab25150665b`  
		Last Modified: Wed, 30 Oct 2024 18:04:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adcfcd385af8f4333f98a9ac980040d67f6772da2b63c7d1e78966783765fc1`  
		Last Modified: Wed, 30 Oct 2024 18:04:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290945a85028a15f32dbd91ed6aee8829d81abd7e9b01cdce418858b075128c`  
		Last Modified: Wed, 30 Oct 2024 18:04:07 GMT  
		Size: 18.9 MB (18880825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e36e635f542f6bda3c4f25e4847f701e677415f0198e4f5ce02b2ba9664eb19`  
		Last Modified: Wed, 30 Oct 2024 18:04:04 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b875954243f2ec81ee862509db36aeb97e86a8e6e633a446feba4bdcae3841`  
		Last Modified: Wed, 30 Oct 2024 18:04:04 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4495a71dbbbc61c4d49faf55c64aeaac6b8c056cd2cb3eeeaabe8960f97975d4`  
		Last Modified: Wed, 30 Oct 2024 18:04:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132fc1a0674a18e71d326d1867a6390aed04f3e816b99971bd669180cc01ada9`  
		Last Modified: Wed, 30 Oct 2024 18:04:06 GMT  
		Size: 19.3 MB (19271051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0034d8c303e4dd911b94dde039045d85beec8ad7dbdabbf9755fb6d55de47f1`  
		Last Modified: Wed, 30 Oct 2024 18:04:03 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea965ed297f69433c228d1fcaae4d36353721e44b5b3d1f625ddd0322df8f4ff`  
		Last Modified: Wed, 30 Oct 2024 18:04:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ae7d32baf203c523d9dc0250ef867dbbdb737f4b169fbe3f3dded539626d81`  
		Last Modified: Wed, 30 Oct 2024 18:04:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3c64a3463b69150371e650ce74bf1416427f7a18f201d20f356a6dfd56c700`  
		Last Modified: Wed, 30 Oct 2024 18:04:06 GMT  
		Size: 20.0 MB (19976495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
