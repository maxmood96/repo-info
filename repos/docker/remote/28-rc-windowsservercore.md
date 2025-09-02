## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:f874a670e8c4d0b5a5e150e3a1333decfcf7f485c384271a0211481dacd4edb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:a88d081e37d3b64f6f6f138962ae5dcb0160001b23668eb3e9c82ad77cc8c6f6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565563928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b83e8499a24ce9751032d44e101ec49ae9c64c16dfb36eb8b4d75e469c4372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 02 Sep 2025 18:09:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Sep 2025 18:09:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Sep 2025 18:09:32 GMT
ENV DOCKER_VERSION=28.4.0-rc.2
# Tue, 02 Sep 2025 18:09:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.4.0-rc.2.zip
# Tue, 02 Sep 2025 18:09:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Sep 2025 18:09:44 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Tue, 02 Sep 2025 18:09:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.windows-amd64.exe
# Tue, 02 Sep 2025 18:09:45 GMT
ENV DOCKER_BUILDX_SHA256=1e89de288c9897990220d2ee695b50956d42a3a0792c0b070e9fee7711b9f896
# Tue, 02 Sep 2025 18:09:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Sep 2025 18:09:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Tue, 02 Sep 2025 18:09:56 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Tue, 02 Sep 2025 18:09:57 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Tue, 02 Sep 2025 18:10:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be4765a327e0d3b7d0c6c3dbc3ab9bb393fba5dc24a78e1c83a9568031eaf84`  
		Last Modified: Tue, 02 Sep 2025 18:13:46 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338738520f02ddcd51370fde96ec28789f7c4d04e611a007b140155f18c543c5`  
		Last Modified: Tue, 02 Sep 2025 18:13:46 GMT  
		Size: 378.9 KB (378897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e56ec25fb72d87897de6005300ab26d5bdf3d90f54e290eea5f7799e03c4f9`  
		Last Modified: Tue, 02 Sep 2025 18:13:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41206e4bbc21887d568ba9ab99fc1c8460a94b69b84abd850dbf716ab8f2cb0`  
		Last Modified: Tue, 02 Sep 2025 18:13:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9daccab393e2ebc09edd518d897acb1e70e20b144c89700829f01069f79c2cf`  
		Last Modified: Tue, 02 Sep 2025 18:13:49 GMT  
		Size: 20.8 MB (20799665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e2d73f769b4c7252cb14cbf61e9aeb8768e58074ccd2d97b2b7a458d076452`  
		Last Modified: Tue, 02 Sep 2025 18:13:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25442f5d9b02d54c0340a99965b285121f6374edaf10f2f6782cb3c04ff1ae48`  
		Last Modified: Tue, 02 Sep 2025 18:13:47 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789aa916ae797e2a5f9dfb5e41b445023f679f2e893b0051ba4e4533c3d4fe71`  
		Last Modified: Tue, 02 Sep 2025 18:13:47 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a8e5df3650a25c941790f74e3a69a96de9e649afce9ee2ccd855b36831924a`  
		Last Modified: Tue, 02 Sep 2025 18:13:48 GMT  
		Size: 23.1 MB (23128815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af26078ec376bfda2523111f41876c06ccc58e29f4460301dc149cd2f2ad7572`  
		Last Modified: Tue, 02 Sep 2025 18:13:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a46cfb643f2acba39d8b0b7a70ebd29e05388e538775ef36f6a2c4494aea70d`  
		Last Modified: Tue, 02 Sep 2025 18:13:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2c83c727c36a0f99461635a81831d447cc2ca68c2defc7ef792270312a2f4`  
		Last Modified: Tue, 02 Sep 2025 18:13:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06987a46b9c5636a86f5f6fd9be152b40389382b284a4c215f2bc8d0b1e356d6`  
		Last Modified: Tue, 02 Sep 2025 18:13:49 GMT  
		Size: 22.4 MB (22414299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:a937bbed072d521be6a982c216a819bba6335ed11f213e4843892552c02c24fe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348336904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c91ad57bf664bb401468d97ca8bc4e4f734de476d57791547d5ad2185e2e20`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 02 Sep 2025 18:02:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Sep 2025 18:03:16 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Sep 2025 18:03:17 GMT
ENV DOCKER_VERSION=28.4.0-rc.2
# Tue, 02 Sep 2025 18:03:18 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.4.0-rc.2.zip
# Tue, 02 Sep 2025 18:03:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Sep 2025 18:03:36 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Tue, 02 Sep 2025 18:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.windows-amd64.exe
# Tue, 02 Sep 2025 18:03:38 GMT
ENV DOCKER_BUILDX_SHA256=1e89de288c9897990220d2ee695b50956d42a3a0792c0b070e9fee7711b9f896
# Tue, 02 Sep 2025 18:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Sep 2025 18:03:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Tue, 02 Sep 2025 18:03:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Tue, 02 Sep 2025 18:03:55 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Tue, 02 Sep 2025 18:04:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8687826872210445ed9fb3dffa5934a5221d8146b07b19f820f9d25c054879e`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc1d1d0f77e1b1e002281108d6969f49c9370bb0926d533ef040bdb9783b89d`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 357.7 KB (357681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f047d82a6729e7ab112b8c091ace1605ae595f5752615b55251e6ce9bbc05`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3542a0e15238c26719c6623c8ba79233c1b0b99788106a8298dfa8c140eb6e4`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e7e9b72d1ab1e0b04a5b3491513b291d42a1f45a949d0209fbef15d2f2c962`  
		Last Modified: Tue, 02 Sep 2025 18:04:45 GMT  
		Size: 20.8 MB (20781508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ba49eec070de62c60b421b5409ed589beefdde9e101527c46b727a2e041b9`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ef258a913cdf6e4443767c05bab0463eaa17f3fc7a8ee6191dd10941739a4b`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b2a123b70288ec9dffbd4cb120874e4a70985d932b08fddb9f83319af30c82`  
		Last Modified: Tue, 02 Sep 2025 18:04:44 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b712d514e93a8e6c91ea0f936b63a5a844aa09aade4a46de7b6180ff85876b8`  
		Last Modified: Tue, 02 Sep 2025 18:04:57 GMT  
		Size: 23.1 MB (23104919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9fef658903d23785dafcd499b3756d01cb8401c0325d32b795a033f14396f0`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bbdbc8dd63dab152d88d182a5c0f700081c9228d26910935a6327229cac312`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3087fa9bec1c057ff92b30b8c72d00d1f2a98bdc0bb9a6e8b726bdf8e7f02b`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065d834d32d703b390759c11a3f92c9754f0a5528ea89c840add6db996837a7e`  
		Last Modified: Tue, 02 Sep 2025 18:04:46 GMT  
		Size: 22.4 MB (22389245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
