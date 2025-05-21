## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:4de7188a91f9615b0e54ec52f6869b180fc9109540f0aa20c85e1a1605d63469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:rc-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:af8fe33abc64add24c5a660d2e8a4d6c865d66a1297abd74b6f34848704ca95a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496126139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c231a89c8c540782e47ae99ba7cafa11af86ce0dfd5449c3fdb55fe8dc40d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 21 May 2025 19:21:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 May 2025 19:21:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 21 May 2025 19:21:50 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 19:21:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Wed, 21 May 2025 19:22:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 19:22:02 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 19:22:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Wed, 21 May 2025 19:22:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Wed, 21 May 2025 19:22:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 19:22:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 19:22:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Wed, 21 May 2025 19:22:14 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Wed, 21 May 2025 19:22:23 GMT
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
	-	`sha256:5828b1d5056860a3145b8515ba785b73b260c1cf3762a1350b0c81b4c2360886`  
		Last Modified: Wed, 21 May 2025 19:22:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515c8bc9f80c41e610675c2d4bc3240aab88fcc8fab5b13a750c28c3997de0b3`  
		Last Modified: Wed, 21 May 2025 19:22:29 GMT  
		Size: 397.4 KB (397414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9560460cf41c809f4b1c9a61d2c76b34fda054e103523f078d2d9bcdad349289`  
		Last Modified: Wed, 21 May 2025 19:22:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3baeb53de79a25e2fe403e7cd7fd207b6961bb6d91cf763b76b075a4409a5a`  
		Last Modified: Wed, 21 May 2025 19:22:28 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31518ef9116c05f1ec049019a0a660132a615284421d1c8e16d4d6a6c504c89a`  
		Last Modified: Wed, 21 May 2025 19:22:29 GMT  
		Size: 20.5 MB (20486363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a3c4c1f351e3bf258db48d860e360b42999606d8854a9caf419b6ae1dfb16e`  
		Last Modified: Wed, 21 May 2025 19:22:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7ddc75fb8d9296856367045675b2b6e2f0cb76321ae59f2781c11cbc0d2b70`  
		Last Modified: Wed, 21 May 2025 19:22:27 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5b3e936f34b43ccf863432052c4f40c674abaff996b8fadb05dcfa5359f45b`  
		Last Modified: Wed, 21 May 2025 19:22:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2372d324f0b634ad04df3ea9d288d15817ba70a2bc0e99d14f754567e2fb208c`  
		Last Modified: Wed, 21 May 2025 19:22:28 GMT  
		Size: 22.3 MB (22293001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6105ff81ead97ab635757e03b3b81873fa445e468b9ef872b4d16a2de83f117`  
		Last Modified: Wed, 21 May 2025 19:22:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbd42d2405e6431827eb0be8f5095dc38ce3a456d531c79f0670e6512027cf`  
		Last Modified: Wed, 21 May 2025 19:22:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37d1e1eef0577977318037531b7e88c626cef1cd9b5473f86de4b8c23f8b8ae`  
		Last Modified: Wed, 21 May 2025 19:22:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1522133e64bad38c46a174ce2224768882fde27928d8e3300eb395d7d0f677`  
		Last Modified: Wed, 21 May 2025 19:22:28 GMT  
		Size: 22.2 MB (22171886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:320a0cb433446b6ac816503c9854d7500eb893bafe0236fae2b28c3fe28fb02b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338847921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f44a15a8419330d12560dfc0ecc0fba0ed4d9664e9bfa03a8d2b0be6f9026c4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 21 May 2025 18:55:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 May 2025 18:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 21 May 2025 18:55:42 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 18:55:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Wed, 21 May 2025 18:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 18:55:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Wed, 21 May 2025 18:55:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Wed, 21 May 2025 18:56:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:56:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 18:56:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Wed, 21 May 2025 18:56:06 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Wed, 21 May 2025 18:56:14 GMT
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
	-	`sha256:17a572c0d8d247a98c0feb1d38ac0c823b872b573006139693bf058e81cd5797`  
		Last Modified: Wed, 21 May 2025 18:56:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8535b393fe908829e4d46f3369758334836cdf47468fcda83ab668911446125`  
		Last Modified: Wed, 21 May 2025 18:56:23 GMT  
		Size: 356.2 KB (356225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655f676294e559a4f77b18b80e61f4fe7c21f98b3296817855c4e84e7889e630`  
		Last Modified: Wed, 21 May 2025 18:56:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa5ad4966dbfeef28ebece837fea8a851e5338eabc784328f30524606fa07c6`  
		Last Modified: Wed, 21 May 2025 18:56:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903e4ee133f378350c992a54e81d0ceb90cbfcf088037d3ac03ff7475f6cc6b9`  
		Last Modified: Wed, 21 May 2025 18:56:24 GMT  
		Size: 20.5 MB (20452194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f21535de8ceef52db74127eba2f2407463e383956144c83571eac032fae348`  
		Last Modified: Wed, 21 May 2025 18:56:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c38c12212eb2518743648d835e2ed0a8c836477978d36c2bfe77246f3b9ce2d`  
		Last Modified: Wed, 21 May 2025 18:56:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db54d1860a9bb76f5f4d53d05fa7aac3fbfa7867cab7ac989ae19ec53e232140`  
		Last Modified: Wed, 21 May 2025 18:56:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec2b9ae64ed178c7f8be1c9ba3f9b8790db3dd8f94207912dd75287367ec94`  
		Last Modified: Wed, 21 May 2025 18:56:21 GMT  
		Size: 22.3 MB (22261564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97beec82bb6981d7bb752516b65f50b58d7ec03a5c59b7f8183fd07090995e6c`  
		Last Modified: Wed, 21 May 2025 18:56:18 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab01ed306726174ea51a9052d2c65fd94e6b9d1425f71ebda5b5b4b2682ac58`  
		Last Modified: Wed, 21 May 2025 18:56:18 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fc186633c32c34b9fbed7853a9700eb449908b837b0e6f52b5efedca0f815e`  
		Last Modified: Wed, 21 May 2025 18:56:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792850ece974cbb5efe4c205611637a2bd0b2c09b766f588d470bea443677f9d`  
		Last Modified: Wed, 21 May 2025 18:56:21 GMT  
		Size: 22.1 MB (22138199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:80b5460ce7c073a352022d4779e463c7ce6c7135ebcbfdb0357341415d6624b2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248999838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5287560491ecdba0147705c8eab70e27fa4da959c2acc8f307e35b97fcab36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 21 May 2025 18:52:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 May 2025 18:52:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 21 May 2025 18:52:51 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 18:52:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Wed, 21 May 2025 18:53:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:53:03 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 18:53:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Wed, 21 May 2025 18:53:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Wed, 21 May 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:53:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 18:53:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Wed, 21 May 2025 18:53:15 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Wed, 21 May 2025 18:53:24 GMT
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
	-	`sha256:02cd9ecb4783184f0f8066184b845d7ccd229b4697c49aefb4c5b00bf274f85e`  
		Last Modified: Wed, 21 May 2025 18:53:33 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80f1a52b0526972b316a694465248fbc1b764f31c742a66ab9c496d6712e936`  
		Last Modified: Wed, 21 May 2025 18:53:33 GMT  
		Size: 374.6 KB (374645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0422ba1599a2f60608e4b8ebd8278976fd9f9b0ec072c7976724bea9b358448a`  
		Last Modified: Wed, 21 May 2025 18:53:32 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ba00207166380abadd97d6959a79a383711ae45c9dea93011cadbf476fa529`  
		Last Modified: Wed, 21 May 2025 18:53:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b9f27689919945411185e2fca547cbc225ec5d566be37c2173f69be1200f02`  
		Last Modified: Wed, 21 May 2025 18:53:33 GMT  
		Size: 20.5 MB (20470381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f368b28356aac5ae2cf16508aecbfe75be440e793a5d3c255055da4ec06d119`  
		Last Modified: Wed, 21 May 2025 18:53:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90eacfd946d5a5206606ed1cabde824a17eeae64b8ac68049cae679bfccded2`  
		Last Modified: Wed, 21 May 2025 18:53:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28304dfe649d9f377cde9902b25127b7e60836606ad6dff33b87d2a0e6acf02f`  
		Last Modified: Wed, 21 May 2025 18:53:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4114fa6594030822b65aba522697ce0a30c73ab4778ae86b9384f0708d5424ab`  
		Last Modified: Wed, 21 May 2025 18:53:31 GMT  
		Size: 22.3 MB (22277593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc6a91474d8aad759566c70185d03b4fb70bd06dc6b61b1581226843533e8a3`  
		Last Modified: Wed, 21 May 2025 18:53:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19947b9ecd02212141da9e653fa1af8d58e22ff286c35369268f50c77c8bb00d`  
		Last Modified: Wed, 21 May 2025 18:53:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26646e154e6f57595e08f1dcd971a1d42274ecdc6f57a73d7a60fa8bce81541a`  
		Last Modified: Wed, 21 May 2025 18:53:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1931e55347cef22880403f1757ee98c01ca0620c3bda8993f6259fa5bd2ff396`  
		Last Modified: Wed, 21 May 2025 18:53:31 GMT  
		Size: 22.1 MB (22148142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
