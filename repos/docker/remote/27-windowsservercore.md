## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:f7fa9f17566277d98e0116a2ab443cd0f28687ca8118216c68ede6a75146efb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:d47c97125d8835d042874822448b6a98af49dafa8b9854ba0d1c243107c14386
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858140900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d31ee9a2bac20520801e37390313b44c969e1779b9c7b138e81ea6cf3ad863`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 09 Nov 2024 02:00:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 09 Nov 2024 02:01:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 09 Nov 2024 02:01:31 GMT
ENV DOCKER_VERSION=27.3.1
# Sat, 09 Nov 2024 02:01:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Sat, 09 Nov 2024 02:01:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 09 Nov 2024 02:01:48 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Sat, 09 Nov 2024 02:01:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Sat, 09 Nov 2024 02:01:50 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Sat, 09 Nov 2024 02:01:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 09 Nov 2024 02:01:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Sat, 09 Nov 2024 02:01:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-windows-x86_64.exe
# Sat, 09 Nov 2024 02:02:00 GMT
ENV DOCKER_COMPOSE_SHA256=30be0d2d5df4d032ffeee3f8c5e6dccc2ef1b2911732055778c3584e9e69bb4b
# Sat, 09 Nov 2024 02:02:09 GMT
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
	-	`sha256:54e9e67e8d34124ddf9ffb4a1453b68ac4af00a8a449032d28a6f87e3ddc34c7`  
		Last Modified: Sat, 09 Nov 2024 02:02:15 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924c0d0a2e21ed9d53768c18809caace888baab8ff625b22cff168c98046c130`  
		Last Modified: Sat, 09 Nov 2024 02:02:15 GMT  
		Size: 491.6 KB (491570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc542f1bd75100f5f9c316f0602b11b197f94749a76300e9941b2d347e84f0fe`  
		Last Modified: Sat, 09 Nov 2024 02:02:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818fdd6a6c15286af2daf125e7daa70823f524607fb5cc0bebce9b9e820cbe70`  
		Last Modified: Sat, 09 Nov 2024 02:02:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb43de8b5e806e003d84fe036c15996fdab73f0bac0011b93a60ef21bb59842`  
		Last Modified: Sat, 09 Nov 2024 02:02:15 GMT  
		Size: 18.9 MB (18888371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf19b351dcf1bd4bd9123722fab21b0a3638bcd6979015e8a8130128eb4a46`  
		Last Modified: Sat, 09 Nov 2024 02:02:13 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17273258aaa080810cf13f6dfeaeb03bbb65aba4f8630130a6afad8e4b543dc0`  
		Last Modified: Sat, 09 Nov 2024 02:02:13 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7d51b36ba0c8dcb048be2ef2537a53eaa6d6094ff641cdcbff1a02cd7ac576`  
		Last Modified: Sat, 09 Nov 2024 02:02:13 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5437969c6de67fa94dac6140161b154a63aacccfcc21ce562badce5a49bfb532`  
		Last Modified: Sat, 09 Nov 2024 02:02:18 GMT  
		Size: 19.4 MB (19413083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d1d6afe3de492b2a69c2d4c2bdf5514fc52789866be4a92fa338ebdcfdb94c`  
		Last Modified: Sat, 09 Nov 2024 02:02:12 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd51147d11027d829a46296251c526c985e11d7f615ad553446538e2880970c9`  
		Last Modified: Sat, 09 Nov 2024 02:02:12 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee4ca672ae5991980fd5660c6876942564a196ab051521a63a2b5db26b1e228`  
		Last Modified: Sat, 09 Nov 2024 02:02:12 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a430f9e470e2a96aa462b243e98b9e378c3e85bef726020c47111f815b2f7e`  
		Last Modified: Sat, 09 Nov 2024 02:02:15 GMT  
		Size: 20.0 MB (19994527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:36fff4b36dcb72d13b59308b9e45568c08e3dc33cabd7b61f892e82570bcf01d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960584016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a033d3c1334172bd8eb939f925e507d59d70beeecd502ba074d45a257f6d4bc5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 09 Nov 2024 02:00:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 09 Nov 2024 02:01:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 09 Nov 2024 02:01:53 GMT
ENV DOCKER_VERSION=27.3.1
# Sat, 09 Nov 2024 02:01:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Sat, 09 Nov 2024 02:02:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 09 Nov 2024 02:02:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Sat, 09 Nov 2024 02:02:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Sat, 09 Nov 2024 02:02:16 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Sat, 09 Nov 2024 02:02:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 09 Nov 2024 02:02:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Sat, 09 Nov 2024 02:02:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-windows-x86_64.exe
# Sat, 09 Nov 2024 02:02:31 GMT
ENV DOCKER_COMPOSE_SHA256=30be0d2d5df4d032ffeee3f8c5e6dccc2ef1b2911732055778c3584e9e69bb4b
# Sat, 09 Nov 2024 02:02:43 GMT
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
	-	`sha256:981072dad5cad414e228dd5cc1f29b1a24d07fda15433c37c4be7dc8b9bf35ab`  
		Last Modified: Sat, 09 Nov 2024 02:02:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4cb8be10c094edf193acbec41ba12daad2bc831f4aeb0b8296732cc13376eb8`  
		Last Modified: Sat, 09 Nov 2024 02:02:52 GMT  
		Size: 485.5 KB (485522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc023edc9c003e20975c8cf3039ef023e4e1858b895d8c59aea35ba5ca769a8c`  
		Last Modified: Sat, 09 Nov 2024 02:02:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170621191a7b6ad3ec7115765d8ca1ecbb976e970db5ca2155d19d0edb06d086`  
		Last Modified: Sat, 09 Nov 2024 02:02:50 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906245bc644ed3fb87a941ccbe789460fa81d29dfd9a3c63fbbaa631829d6cf7`  
		Last Modified: Sat, 09 Nov 2024 02:02:52 GMT  
		Size: 18.9 MB (18881456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d185602cd44e554c78e083b18bc282cb6773245ace93a43f843ad6b428a722c`  
		Last Modified: Sat, 09 Nov 2024 02:02:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c2ff02028cb935ab90b1aa4056ec1cbcdda808abc54e7f168de2a0fe79385b`  
		Last Modified: Sat, 09 Nov 2024 02:02:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eaf88e4c7b81bf3dc1ff5e026bab4aa9d423b43dfc125fd2bbe383fa54c394`  
		Last Modified: Sat, 09 Nov 2024 02:02:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7a859c2f2516d726d48bd863080234e1c5e2b73fec175c324e817fb75dec1`  
		Last Modified: Sat, 09 Nov 2024 02:02:51 GMT  
		Size: 19.4 MB (19403317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1ac19e8cb39cc1a89b115ea962e9791c744196b089375b15489339d86dfcd`  
		Last Modified: Sat, 09 Nov 2024 02:02:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58a74e535b4ed041e9add4367888b7811042c9bda8b086631c141d48721bcc4`  
		Last Modified: Sat, 09 Nov 2024 02:02:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e72ab7f3f6742a61832ae3ba33e9ae14f915bbcec0e2ba1a585b2617e64b32`  
		Last Modified: Sat, 09 Nov 2024 02:02:47 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe31d316b4700918dae3b519eac6cad74a4bee0a5f990769ff553a15ece1193`  
		Last Modified: Sat, 09 Nov 2024 02:02:50 GMT  
		Size: 20.0 MB (19976790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
