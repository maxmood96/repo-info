## `docker:26-rc-windowsservercore`

```console
$ docker pull docker@sha256:712ac16bffafddb395da2c0e8e8d9abe87438c2f839d207d9579d4c6681db7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `docker:26-rc-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:a6ad8ae9e11f219ce5403b17e5c19b854f0535bf111897b8dd34553011b701db
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013956756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93be2f101abfbe5aeb68e1992b81bbee19b716c1e3bae089dcfc24853a78d526`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Thu, 14 Mar 2024 17:57:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Mar 2024 17:57:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Mar 2024 17:57:24 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Thu, 14 Mar 2024 17:57:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Thu, 14 Mar 2024 17:57:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 14 Mar 2024 17:57:34 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 14 Mar 2024 17:57:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Thu, 14 Mar 2024 17:57:35 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Thu, 14 Mar 2024 17:57:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 14 Mar 2024 17:57:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 14 Mar 2024 17:57:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Thu, 14 Mar 2024 17:57:44 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Thu, 14 Mar 2024 17:57:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5f033b4a2f0dd657701163d15da54d3976388e52603d6ea0bf2b2b12295cc7`  
		Last Modified: Thu, 14 Mar 2024 17:58:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cb4b0993a579aec3d8569bc663298410706d341ea2951d6b223616072e41de`  
		Last Modified: Thu, 14 Mar 2024 17:58:00 GMT  
		Size: 489.9 KB (489878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e00cf3f431030a26deef39dd3ed7c29df3a396d6af90bce50b3ab94e97cd17`  
		Last Modified: Thu, 14 Mar 2024 17:57:59 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874dbf50f399ded22bd3705109bd57a3ec05b0fed0855543f382dd27f8e0acf0`  
		Last Modified: Thu, 14 Mar 2024 17:57:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c874b1370dba27dd43180dff7b6dfd1b8cb5b041482a74ed7906a27871d49c44`  
		Last Modified: Thu, 14 Mar 2024 17:58:01 GMT  
		Size: 18.1 MB (18093938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ddae5243f8191ea6508b60a70964f38954cadc1c2d885446b0b3957f3004f7`  
		Last Modified: Thu, 14 Mar 2024 17:57:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3394c9fa02510fc8bbfa5fbeaaaac51ddfbcafaa7d0f1587e0978a0f7aae32fb`  
		Last Modified: Thu, 14 Mar 2024 17:57:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b88b5fe4d36cf47f91066f36b131354335a2dec7c5d13ce2070c4b923f85c25`  
		Last Modified: Thu, 14 Mar 2024 17:57:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231357fc64e83e91d1181a475718f8cab10228b1d267e44b7e3932e85d8cc4ef`  
		Last Modified: Thu, 14 Mar 2024 17:58:03 GMT  
		Size: 18.8 MB (18828437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be297b25a223a9a6bf054f1922af88bfd923c8ac80de5117603cb751511964c4`  
		Last Modified: Thu, 14 Mar 2024 17:57:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6338d284c39b2932588dc7b778df1d29bd48aa2934810df16a879c1aa4e04ad`  
		Last Modified: Thu, 14 Mar 2024 17:57:55 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c3cfc99862aecd93a61dec31bd6c3b0f04f5d6b38072cb25aa835dcda9f60`  
		Last Modified: Thu, 14 Mar 2024 17:57:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204309f9a690bc58df49d92515dc9396180a7542602c3513f574686ab43e4580`  
		Last Modified: Thu, 14 Mar 2024 17:57:58 GMT  
		Size: 19.1 MB (19073916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:26-rc-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:78833eaa534cb3e4a2added066b5aa89fc9ddf24dad6737b17546ab0dc6e3273
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181609166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7cf7b5897103b52e0f4cc39c46e2b01e60cfb9c06f1ad8b32844ab16f4a3ff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Thu, 14 Mar 2024 18:01:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Mar 2024 18:02:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Mar 2024 18:02:24 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Thu, 14 Mar 2024 18:02:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Thu, 14 Mar 2024 18:02:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 14 Mar 2024 18:02:52 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 14 Mar 2024 18:02:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Thu, 14 Mar 2024 18:02:53 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Thu, 14 Mar 2024 18:03:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 14 Mar 2024 18:03:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 14 Mar 2024 18:03:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Thu, 14 Mar 2024 18:03:18 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Thu, 14 Mar 2024 18:03:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865bc58a8393f10d639c8a6a2301c6ca0a7f68578e5fbbb60235110d2637cd80`  
		Last Modified: Thu, 14 Mar 2024 18:03:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c9eb6cad110a7baf31b6c643489a08a48b058d7bf52d38a44eac8b290ce7de`  
		Last Modified: Thu, 14 Mar 2024 18:03:48 GMT  
		Size: 488.0 KB (488038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4601b1860c77c87a416e9048bdadd771988f2ed55a05ab0d5387bbb29f6e62aa`  
		Last Modified: Thu, 14 Mar 2024 18:03:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79be21492e24a1fc29463dd608e1ac18ae849e8cf07bd2e4aee92ffc96071f03`  
		Last Modified: Thu, 14 Mar 2024 18:03:47 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b655744468255c1b36e9f3b51e6749ee7770f7de20f48bbdf43238cb68a18551`  
		Last Modified: Thu, 14 Mar 2024 18:03:48 GMT  
		Size: 18.1 MB (18102440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bfbf5d94b170883b24bbe831f4db93dd5e61da633f3ba37dfa3b9c0db360cf`  
		Last Modified: Thu, 14 Mar 2024 18:03:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4abeacea86e56a0e8cd87a877502b901430daf90d641d3bfceb627966aff6d`  
		Last Modified: Thu, 14 Mar 2024 18:03:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b43be6599f34c1e432a2ed3a41ea1c5651621b45c5be4baa9c8f43dab9f060`  
		Last Modified: Thu, 14 Mar 2024 18:03:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5345c2558a39d4cc53d7db60bfcc455bb184e8de4e83ee4cdb8efbf45b5eaa`  
		Last Modified: Thu, 14 Mar 2024 18:03:47 GMT  
		Size: 18.8 MB (18833324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85d7f324aca774653b8bdde54c891e414c2189865c96673bb86850ccc02c00f`  
		Last Modified: Thu, 14 Mar 2024 18:03:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ec425c8c3ecd10bbb7e4d5ea7fcdbeee6a8903e4878da998c650f390eba6e7`  
		Last Modified: Thu, 14 Mar 2024 18:03:44 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a3fd0efa7f04616343b4b0ff54e3ef352292c1dc58c1ef65ca29624ba4bdc3`  
		Last Modified: Thu, 14 Mar 2024 18:03:44 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e604dad8a5e382183c07fb574490950dfedcd198f536cb9549b93cabbb2ae31`  
		Last Modified: Thu, 14 Mar 2024 18:03:47 GMT  
		Size: 19.1 MB (19073796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
