## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:2bca5e71626ddb386778c18b8e4d91edbd5cc4942e90d2ac0bcd7489ee6f6494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:ffd0f031e019132610dedc7c5a2730a86d2313cb3e79a932b4bb119aebcbcc9d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338060649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9915ba114b30694d6670ff88da97b948644dc7bd9027835aae5add80473ba963`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Wed, 07 May 2025 18:25:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 07 May 2025 18:26:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 07 May 2025 18:26:08 GMT
ENV DOCKER_VERSION=28.1.1
# Wed, 07 May 2025 18:26:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Wed, 07 May 2025 18:26:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 07 May 2025 18:26:28 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Wed, 07 May 2025 18:26:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Wed, 07 May 2025 18:26:30 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Wed, 07 May 2025 18:26:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 07 May 2025 18:26:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.0
# Wed, 07 May 2025 18:26:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.0/docker-compose-windows-x86_64.exe
# Wed, 07 May 2025 18:26:43 GMT
ENV DOCKER_COMPOSE_SHA256=9916ce82e444bb68e539ab36b947c2edb95f74e5a640c2661255f2c340b5cfee
# Wed, 07 May 2025 18:26:54 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c691244db141c5df69e5f42ce2f48779598a6468117b2ffe4263c1b2c9d09356`  
		Last Modified: Thu, 08 May 2025 17:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db902bc64877ceae3ae2525965d2c92f1ee0e66a48c0403d7815a8c169c92cd`  
		Last Modified: Thu, 08 May 2025 17:18:51 GMT  
		Size: 357.9 KB (357858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b30615dd72096dc91241f77d594e51a6a119260bfe075163d83662398b9293`  
		Last Modified: Thu, 08 May 2025 17:18:51 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2feda4ed39e476990d6e204268c3ca04bbd91e2de736c9b0063e3ddbe20ab2c8`  
		Last Modified: Thu, 08 May 2025 17:18:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5f81d2ca3d1d102f8d1f8f40bd731092c42b044eab26f50ccd4e5d1b0b0a84`  
		Last Modified: Thu, 08 May 2025 17:18:55 GMT  
		Size: 19.9 MB (19896364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d79efdd35f8094c18089c12c8761cbbaa7bb6158c46282bac9abb8a968ca47`  
		Last Modified: Thu, 08 May 2025 17:18:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a734969415ad69fed274344b8d0d78c9039d2d1771b8147e218e8ba31f42aa26`  
		Last Modified: Thu, 08 May 2025 17:18:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4d3455df67b61c274f8459be2243a404445b7f33ad13906c28a068f05e410`  
		Last Modified: Thu, 08 May 2025 17:18:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55570dc912c9e429d9126bfdf61b264d795dfc01aa594c3b3d5306981e8b21b7`  
		Last Modified: Thu, 08 May 2025 17:18:57 GMT  
		Size: 22.4 MB (22358838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f141bb571e876e276748a5b15318da114267e4f23e81f321e7c2ecde9140be00`  
		Last Modified: Thu, 08 May 2025 17:18:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ae9155cee8ed9a9d9736129cdbec11b7270ae4324b92b84ab72024842db425`  
		Last Modified: Thu, 08 May 2025 17:18:55 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d8bad372841c27de5ab20edc1c99b5796365ca025995890105310679e8b6e3`  
		Last Modified: Thu, 08 May 2025 17:18:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5ab04535a0a8928faf7da0ec73002b2402a8f57be314c1060353f730fceda1`  
		Last Modified: Thu, 08 May 2025 17:18:59 GMT  
		Size: 21.9 MB (21853489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
