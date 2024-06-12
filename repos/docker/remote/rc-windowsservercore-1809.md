## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:6d60ad807785f7d1213d6b0688dff44ccc48e086da6bd156b0110c5c7cf80dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:cd2aaa4d4dfd8aef01f6ae79f92734aea1c8aa1c4e3dc57b9ecca81bb561476e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181643688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16b59e8f36f575a28f084f768c49c61b35ffde29a7cea0372c83b671a2efc4a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 20 Mar 2024 20:48:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 20 Mar 2024 20:50:20 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 20 Mar 2024 20:50:21 GMT
ENV DOCKER_VERSION=26.0.0-rc3
# Wed, 20 Mar 2024 20:50:21 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc3.zip
# Wed, 20 Mar 2024 20:50:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 20 Mar 2024 20:51:00 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 20:51:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Wed, 20 Mar 2024 20:51:01 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Wed, 20 Mar 2024 20:51:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 20 Mar 2024 20:51:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Wed, 20 Mar 2024 20:51:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-windows-x86_64.exe
# Wed, 20 Mar 2024 20:51:39 GMT
ENV DOCKER_COMPOSE_SHA256=27289c82fe3ee64eaa415ae47f028f7c6af6ab347f1af4fde0e0d7d2b4a84dbb
# Wed, 20 Mar 2024 20:52:15 GMT
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
	-	`sha256:764d4a4841a5f8b4025a6263873f5d752c5e0de5c2cdfed58798cc3db20509c8`  
		Last Modified: Wed, 20 Mar 2024 20:52:21 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5178e692e1ecd2bc3a9f6e8ffde4ac5f5e5cb039cce28d2bff021f3e25c0d252`  
		Last Modified: Wed, 20 Mar 2024 20:52:21 GMT  
		Size: 485.0 KB (484963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb807c3e08c67f6a4dae1359815268e8710ef0e5f4419811e0a2fdee18cea5c4`  
		Last Modified: Wed, 20 Mar 2024 20:52:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c29775ed22e904acf66f2ace048749abe0872df7e731765fb83e291276d53b`  
		Last Modified: Wed, 20 Mar 2024 20:52:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cf62e5e3ac639aeba806bfc67cc3179915ae2ea21ca0eb9ebacc7e4487cf43`  
		Last Modified: Wed, 20 Mar 2024 20:52:21 GMT  
		Size: 18.2 MB (18153794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eba8cbd9d8bfa22f6c4023ed2a589ba14c0d0aab43490bbb0cd5938c897b2f1`  
		Last Modified: Wed, 20 Mar 2024 20:52:19 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18aac1bfb7e7b19e396c172e3f09ab0ef23e7b178a3f6d54e1236d2819ae21af`  
		Last Modified: Wed, 20 Mar 2024 20:52:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e763210c6ad0564ab110d7218b3e80bf73ec0a7bb27943a0f96275026596b69c`  
		Last Modified: Wed, 20 Mar 2024 20:52:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c5c8c3b9f61c91b017d3da6d1081634dcb6ec72d98a4746774dc6da54ae29d`  
		Last Modified: Wed, 20 Mar 2024 20:52:20 GMT  
		Size: 18.8 MB (18821228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37461aaca9c91d9f641390b3cfc96491f0a3f7c023c2317740ae0cd4286bdd3`  
		Last Modified: Wed, 20 Mar 2024 20:52:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc080107918da7ff52d39cc5f4f663399c7e9125884a778ce6f62c373262939`  
		Last Modified: Wed, 20 Mar 2024 20:52:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506fe4477ba9bcb1f02d0aeab05c7ec57c4cc810617735767c51282b15bf0321`  
		Last Modified: Wed, 20 Mar 2024 20:52:17 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c971a4035bd1c0a60fb06fc8841e5d2f3e42b7e43fbf3299c63bd4f405fda6`  
		Last Modified: Wed, 20 Mar 2024 20:52:20 GMT  
		Size: 19.1 MB (19072066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
