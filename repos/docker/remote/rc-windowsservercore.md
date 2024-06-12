## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:d64aadaea906e22ae8189596c41be0a84200df57b5efb60d045dfaf4d6ac7f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `docker:rc-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:8e9b7f579eeed6b6bfa6b812aa6421567b3b21f98b894f3c73bc10a4420a258b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2014036580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9c3a6ed400cfb64b2d3954b2077d61cedb97d54741b3f7c5ba2a884ab49bb6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 20 Mar 2024 20:48:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 20 Mar 2024 20:49:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 20 Mar 2024 20:49:15 GMT
ENV DOCKER_VERSION=26.0.0-rc3
# Wed, 20 Mar 2024 20:49:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc3.zip
# Wed, 20 Mar 2024 20:49:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 20 Mar 2024 20:49:32 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 20:49:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Wed, 20 Mar 2024 20:49:33 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Wed, 20 Mar 2024 20:49:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 20 Mar 2024 20:49:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Wed, 20 Mar 2024 20:49:43 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-windows-x86_64.exe
# Wed, 20 Mar 2024 20:49:43 GMT
ENV DOCKER_COMPOSE_SHA256=27289c82fe3ee64eaa415ae47f028f7c6af6ab347f1af4fde0e0d7d2b4a84dbb
# Wed, 20 Mar 2024 20:49:51 GMT
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
	-	`sha256:206e8f69eab2e35563ac66720b6396899db7243d4d46a6eed0b2dea9dc1e76c7`  
		Last Modified: Wed, 20 Mar 2024 20:49:57 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb53a71a076c9a99f72d8210590380d9de013cdcff25bc3b3b59a4f41a8d4fd8`  
		Last Modified: Wed, 20 Mar 2024 20:49:57 GMT  
		Size: 504.4 KB (504407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacacf4670e854afd85a3e9ef31656cad216cf935eb3ea0ef04643f35841f620`  
		Last Modified: Wed, 20 Mar 2024 20:49:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050ec089498b16adeec0ae1c99b1988385a619872fc1ab9f6f48077c48ef042e`  
		Last Modified: Wed, 20 Mar 2024 20:49:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801a2ac38ebed4188e2dc20b7df234962d041608fd4a12c7d7107bf78204ae64`  
		Last Modified: Wed, 20 Mar 2024 20:49:57 GMT  
		Size: 18.2 MB (18151531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e8f68349edfbbb10b79bbceed666f799c9b4f21dc292e99d885166d37b71b2`  
		Last Modified: Wed, 20 Mar 2024 20:49:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71dc2bbf4f96721e07633ab0674e46bafc95010dc65b7f712e43ad6c96c9a8e`  
		Last Modified: Wed, 20 Mar 2024 20:49:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b801278ca721e11d1021f1973f6bfff856599db8f8cab675a4376e5b5cf61b2`  
		Last Modified: Wed, 20 Mar 2024 20:49:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7610067473e9890d8e50db9a8bbec6a03a24bbb9baf84480fb03782212c469`  
		Last Modified: Wed, 20 Mar 2024 20:49:56 GMT  
		Size: 18.8 MB (18829593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465e1a33cfd90ad7620a706d561f5e05f75359607a6137072a185675a118d545`  
		Last Modified: Wed, 20 Mar 2024 20:49:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078e27dfe73234fe37712af369781eb447136071aa03060c863e11d0fb3f5657`  
		Last Modified: Wed, 20 Mar 2024 20:49:54 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47b657972645625adb0824c3dd6e18c0b5e17b3163d7fb49e1fceedd4f8bf4b`  
		Last Modified: Wed, 20 Mar 2024 20:49:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f09107c595e752b2d5fe476d9d5268603827e8f05b9396e889700fe19d76fd1`  
		Last Modified: Wed, 20 Mar 2024 20:49:56 GMT  
		Size: 19.1 MB (19080420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.17763.5576; amd64

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
