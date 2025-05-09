## `docker:windowsservercore`

```console
$ docker pull docker@sha256:763cd7ab8f74e051bf11a7ca466bbaf3a43fece45c9e4f2dad9d2491cca213a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:4ccb6c991dd74c258b0a81186edeb90078284bf7868cd6229e64b904feaf302c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459732365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63714859c74e91240eefa337a42c1e598680505bff97dedb00a7f0bc1389aea7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Wed, 07 May 2025 18:32:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 07 May 2025 18:32:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 07 May 2025 18:32:53 GMT
ENV DOCKER_VERSION=28.1.1
# Wed, 07 May 2025 18:32:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Wed, 07 May 2025 18:33:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 07 May 2025 18:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Wed, 07 May 2025 18:33:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Wed, 07 May 2025 18:33:07 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Wed, 07 May 2025 18:33:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 07 May 2025 18:33:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.0
# Wed, 07 May 2025 18:33:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.0/docker-compose-windows-x86_64.exe
# Wed, 07 May 2025 18:33:20 GMT
ENV DOCKER_COMPOSE_SHA256=9916ce82e444bb68e539ab36b947c2edb95f74e5a640c2661255f2c340b5cfee
# Wed, 07 May 2025 18:33:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22921e3ab6c5efd79126d7b585b9662a46f531bea91ab8bbe89589ced76f3ac7`  
		Last Modified: Fri, 09 May 2025 12:18:45 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a7dcb894df5c8b61d49608702a3aa54639715a6579dfcdd38267512627e410`  
		Last Modified: Fri, 09 May 2025 12:18:46 GMT  
		Size: 381.5 KB (381462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231b6b67c8c492cfe88623eceb316dc412d6c2f2b20129b748c5e1efce4b6a71`  
		Last Modified: Fri, 09 May 2025 12:18:45 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2949e8ccba79103f9c7dc2641e0087ab6ac874547c98d1bc9583d51078eff48b`  
		Last Modified: Fri, 09 May 2025 12:18:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f2e8fa625a918a2559842565dc67a65b26e1b9e889094e98bdbf38d6ebd3c3`  
		Last Modified: Wed, 07 May 2025 18:33:38 GMT  
		Size: 19.9 MB (19916530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf15783e93b1eee0a7bfaab79219d4072e4ffe1de96dfd182f24321ae576734`  
		Last Modified: Fri, 09 May 2025 12:18:45 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a6b05e54c87d00fbf3780f914b7b18b04acc4b6556aed0e6dc5a6a6c39fe2d`  
		Last Modified: Fri, 09 May 2025 12:18:45 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24cda0de71389806c3606237a322864557d14666704712020cffa71f4869937`  
		Last Modified: Fri, 09 May 2025 12:18:46 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229788863bc3cad2edfb77f5bae705ea18d0d2bdcb95d51cf5e00ee4351e6909`  
		Last Modified: Wed, 07 May 2025 18:33:36 GMT  
		Size: 22.4 MB (22379423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682e77b9e62531589283552fb3c08071ce46004ac75bad354cf02576a197a99a`  
		Last Modified: Fri, 09 May 2025 12:18:46 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc16bdfe2f2f4086f6a7e264e6484afc6b9d7ca99e7899de33982fcedf3a73`  
		Last Modified: Fri, 09 May 2025 12:18:46 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267336a44bf64337c1a5943fe87e1a2bc1d704339bc18398428ea65b3aba784e`  
		Last Modified: Fri, 09 May 2025 12:18:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132e9db793bc65d39032c50e2140f23833dd94f4f351aff6532915fe1d208ef1`  
		Last Modified: Wed, 07 May 2025 18:33:36 GMT  
		Size: 21.9 MB (21881450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3566; amd64

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

### `docker:windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:ad7ad2528e029afdd061a7b53f64cc32ec4aac4c944d9598009e1316b7c183c3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230021409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22855d5358bc6b2a008600a91875c0fe528cdfe074e011b437f764fa7bbe90d8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Wed, 07 May 2025 18:25:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 07 May 2025 18:26:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 07 May 2025 18:26:44 GMT
ENV DOCKER_VERSION=28.1.1
# Wed, 07 May 2025 18:26:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Wed, 07 May 2025 18:27:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 07 May 2025 18:27:05 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Wed, 07 May 2025 18:27:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Wed, 07 May 2025 18:27:07 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Wed, 07 May 2025 18:27:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 07 May 2025 18:27:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.0
# Wed, 07 May 2025 18:27:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.0/docker-compose-windows-x86_64.exe
# Wed, 07 May 2025 18:27:23 GMT
ENV DOCKER_COMPOSE_SHA256=9916ce82e444bb68e539ab36b947c2edb95f74e5a640c2661255f2c340b5cfee
# Wed, 07 May 2025 18:27:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba30853a0109501ede96b9d1f5cb43b595e85ec9486f9aa68fbcf060da49db39`  
		Last Modified: Fri, 09 May 2025 00:40:34 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df45538ec8cb2564b89c1547428b8d83db7c149cdc298ccd41deae398e73a66`  
		Last Modified: Fri, 09 May 2025 00:40:34 GMT  
		Size: 363.2 KB (363243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3dc1ff84cf2cd833a4760eb93a58db18c74017429646f7553c0724f114d59a`  
		Last Modified: Fri, 09 May 2025 00:40:34 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b463d09e0500c3f423af97d8291ff23b01d3764770ef2d1160c6c31b6e66d`  
		Last Modified: Fri, 09 May 2025 00:40:36 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe44c907328c6f61ecfe578a4f7bf0dabd80dd4cfa283bfc1196b43487b1fcc`  
		Last Modified: Fri, 09 May 2025 00:40:38 GMT  
		Size: 19.9 MB (19903186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4069886a077dd4101aef9aa608d98a900205b66de42fce75002dcf3823cc1b`  
		Last Modified: Fri, 09 May 2025 00:40:36 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b562c27b9daaeacbf61de04505c6651b1f5444fa8192ea39c5dd7184632020b`  
		Last Modified: Fri, 09 May 2025 00:40:37 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d190ab207dfd43e8b0ee21bd8321eeea635d360db6f18bb7ae3cee7231b6186b`  
		Last Modified: Fri, 09 May 2025 00:40:38 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a9600c92f6a537f21437c5f857fe2824195ceb8e78f4cca722ea5471ccbcb3`  
		Last Modified: Fri, 09 May 2025 00:40:42 GMT  
		Size: 22.4 MB (22363747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792800c1c92ffc2a9bd935ae607ba65c0518e6eca75a69dc4e5815e5960ee7f`  
		Last Modified: Fri, 09 May 2025 00:40:40 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597f4f5f43bc8ac61d2be0630d454063275171b1a400305261e744dd12b59edc`  
		Last Modified: Fri, 09 May 2025 00:40:40 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83b77cb813106a7e38bc9afdcc79b8d31f5fbb01a3ac24bf97613cad35622f6`  
		Last Modified: Fri, 09 May 2025 00:40:42 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e1e9959fa8c31f581937a3a62f3f50ce1ce9a185e0e3a4404ad35dfaeed50d`  
		Last Modified: Fri, 09 May 2025 00:40:45 GMT  
		Size: 21.9 MB (21853185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
