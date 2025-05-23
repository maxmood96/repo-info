## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:baabc0c921758ec088b967f76ef87ecd1cd24f6a4b68fc5e603dd62a9d11c031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:a9861fcb9a1972cf3d9dc4a094ef0f5beca4f00b01b64fd618aedc7ab5190c1a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495991611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cc67af46b5e62bdb0404bcb8f5ea9ef4dec705722be631c896a2f6bbca3cdb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 23 May 2025 18:57:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 18:57:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 18:57:58 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Fri, 23 May 2025 18:57:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Fri, 23 May 2025 18:58:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:58:10 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 18:58:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 18:58:11 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 18:58:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:58:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 18:58:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 18:58:23 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 18:58:32 GMT
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
	-	`sha256:ff54e8b809d0fc15bbb9fdccdb4e1e022f38d6938445e20977987076ef2fc7e4`  
		Last Modified: Fri, 23 May 2025 18:58:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be32dbe002dde1e8b06d156bf2104262105927cf524ee73803dbfd4e99f17d1`  
		Last Modified: Fri, 23 May 2025 18:58:37 GMT  
		Size: 395.7 KB (395665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1acadac8783fc9c49eb7dda900ba04e1d32c1dfe5353efb8cfd084ee4182ad`  
		Last Modified: Fri, 23 May 2025 18:58:36 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cced0cef928328eac8d95b64529f05ade4cdf96186f92e2cad3ee4a3b5d90d5d`  
		Last Modified: Fri, 23 May 2025 18:58:37 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ca838340cd64183ae866446a0aa1ff84c1e7d542f5cc0293f60a7ceee98db5`  
		Last Modified: Fri, 23 May 2025 18:58:38 GMT  
		Size: 20.5 MB (20484787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeaf6241b97f268ce3e5fe968e9bdecad3dc2083cad1a14e6eeb8259d75c997`  
		Last Modified: Fri, 23 May 2025 18:58:36 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd027542bd8127c85af3baba0ff9a6f8dc349709faff64e3a72272b5f5526c2`  
		Last Modified: Fri, 23 May 2025 18:58:36 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf90bc45a46edd7a1d96cc4f1e744c13e86b62b5d72f1a67c3636c82f73a8c6`  
		Last Modified: Fri, 23 May 2025 18:58:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa42009a2a8c8788f6640d664a9563fecb6cb24ba58c0100399a95454a7fa6b`  
		Last Modified: Fri, 23 May 2025 18:58:38 GMT  
		Size: 22.3 MB (22290682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ff92887ff05816c2a3292c2eb8e153e8d4e19427ff9c91d8cadece506cc1a3`  
		Last Modified: Fri, 23 May 2025 18:58:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fda46de098be5f0e4009ddc1880a22a2993d744e2f8de46820f458914eaf27`  
		Last Modified: Fri, 23 May 2025 18:58:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577bddf4989761749d3ddbde37877d8baa440d13def0c184d1bb2ceb84d9cf5a`  
		Last Modified: Fri, 23 May 2025 18:58:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c700e9bf462908b0357c41dea43f149528a7cc921b60e27661b378c53416f3`  
		Last Modified: Fri, 23 May 2025 18:58:37 GMT  
		Size: 22.0 MB (22042937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:96d43ae4d991ddfa53c9ab8d3da5be764d4ea3c7add0bdc1eebdede609ade246
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338721222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139aa7d79ea5a31db763229aca954ab4c22dd08f84558a45eceada6d12eb03c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 23 May 2025 18:59:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 18:59:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 18:59:45 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Fri, 23 May 2025 18:59:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Fri, 23 May 2025 18:59:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:59:56 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 18:59:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 18:59:57 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:00:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:00:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:00:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:00:06 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:00:14 GMT
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
	-	`sha256:78e15449054f393fa0be69bca57f4e37d030e59e0093c42f2ae60f2d70ca111a`  
		Last Modified: Fri, 23 May 2025 19:00:21 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6791f2711b3497f5ff9d281a8db42412a13f4aa4285881dc4ac8fa74af397d28`  
		Last Modified: Fri, 23 May 2025 19:00:22 GMT  
		Size: 356.6 KB (356587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219cafef75b1d6a6b9c1f7ca38f30c9afa381312521a90442c9996eb9f357bf9`  
		Last Modified: Fri, 23 May 2025 19:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193197c4313525e2b4e9b28aca7c4e42f069b7ea4428f0dac55968d1a15adbf0`  
		Last Modified: Fri, 23 May 2025 19:00:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640d8f49b99add9a4d820be6aa4f072ac32dd189eb7cdaf4a93a18d692aa4a32`  
		Last Modified: Fri, 23 May 2025 19:00:22 GMT  
		Size: 20.5 MB (20452117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea33b3f215c80e7e531cebba8d66a1849473b85e5d3555bed94e4761fc22e524`  
		Last Modified: Fri, 23 May 2025 19:00:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcebc271467f124e68de72ac2407b0912809580b158cad6ee3f8af5f56d5cf8`  
		Last Modified: Fri, 23 May 2025 19:00:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0fedb0f306e9ecc03e3df7711e85e11e72853f3af38261b23411ea49c86925`  
		Last Modified: Fri, 23 May 2025 19:00:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d9f486d4d9cb9136298e740017cf02265c70a2ff79622e69066e220124d687`  
		Last Modified: Fri, 23 May 2025 19:00:20 GMT  
		Size: 22.3 MB (22261452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2081484829036cf12b2e8f03c9ca478d45a06d3ef055ffe7d4db39a9677f73b4`  
		Last Modified: Fri, 23 May 2025 19:00:17 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8293f261f2933e7722de6ab1967364997211b609cd9cc11da8759d6101ad4ad`  
		Last Modified: Fri, 23 May 2025 19:00:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603c129d87c2e5edf0eeed364436892c2e0237ce73c3023f1a0b0966f7ac0030`  
		Last Modified: Fri, 23 May 2025 19:00:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584775f0f553495fbe9410171084e3bf52f13ad12755a2b281947130912e2134`  
		Last Modified: Fri, 23 May 2025 19:00:20 GMT  
		Size: 22.0 MB (22011394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:924c86bc3a9fc179bab73e288cad586676a7023d45d940d498fdd7d1ad1831fd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248824402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991ad5d102fd3b905e33a019775558e68fa88e771acf1a2dea33c37b8ebb6046`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 23 May 2025 19:00:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:01:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:01:02 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Fri, 23 May 2025 19:01:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Fri, 23 May 2025 19:01:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:01:17 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:01:17 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:01:18 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:01:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:01:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:01:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:01:29 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:01:37 GMT
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
	-	`sha256:0e555802a505ed93037f12aa40cebc24cf11c8053e7ace1faadfa6035d38f1bb`  
		Last Modified: Fri, 23 May 2025 19:01:44 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0cdfbb416cc8a034dc282e75221c0e34725794d358fefeeeafa250d3604c82`  
		Last Modified: Fri, 23 May 2025 19:01:44 GMT  
		Size: 362.5 KB (362461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8610806d6388e89a34a2b2d46166909375114b2594b423432e7714f6541dc0`  
		Last Modified: Fri, 23 May 2025 19:01:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157756351d34596af48a01e8399354519b4c2c92cf8b05435dff6d5b3e0ea4cf`  
		Last Modified: Fri, 23 May 2025 19:01:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e68a7cb6ad30c239d7398513c126cdb9c7a725f0545296bf09029d3138f33`  
		Last Modified: Fri, 23 May 2025 19:01:45 GMT  
		Size: 20.5 MB (20458301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2f1e7a0e2392f34706ac96dea30ae03e436b6b26f5de80c8e08dd32670ca3b`  
		Last Modified: Fri, 23 May 2025 19:01:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d16edf1ccbee2c9ecb9c1f7172e7ac6f1c2b0daaf287d93c7ee879754069b4b`  
		Last Modified: Fri, 23 May 2025 19:01:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd63157335803f860cc1a732c46b3771058d179c166fd7bc5a4a4bce8c051b56`  
		Last Modified: Fri, 23 May 2025 19:01:42 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a986d6490f08747b34df8e7044051beef1911f8e15c1d641ee03ac5ea485f4`  
		Last Modified: Fri, 23 May 2025 19:01:44 GMT  
		Size: 22.3 MB (22266069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97da940e2e4a9176ef14000dbcc2ee5451f31258ad0b97faf4a56e1e201acf9d`  
		Last Modified: Fri, 23 May 2025 19:01:41 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976ae6fc1e026b0c77c5adff2b781cf41d187d95c34c5c576e820376f8387be2`  
		Last Modified: Fri, 23 May 2025 19:01:41 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffa20c6445b805be5816601dddd00954ef4579d69e0349dc5994a8b2fde602b`  
		Last Modified: Fri, 23 May 2025 19:01:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cdc56bd7dcafb656337ad50372afd3a0c57c7433968a55e085782d82226abb`  
		Last Modified: Fri, 23 May 2025 19:01:44 GMT  
		Size: 22.0 MB (22008201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
