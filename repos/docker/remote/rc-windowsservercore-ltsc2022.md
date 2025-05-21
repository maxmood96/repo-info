## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ecce54ebbd91d9703303e786fc3a710faa2e1919a0f7c3355e1c6e0cff515b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

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
