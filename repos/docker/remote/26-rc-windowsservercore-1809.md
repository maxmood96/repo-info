## `docker:26-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:55376d9373eddc7488bcea2e677fd6213d3fc4239c34649156b3f67298ad9a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `docker:26-rc-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:543b3730b07d2b99da8dd99ec9710394ae13b6a066776567d95f7cda0ca7de9a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181622105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b24a5123f74a5de96d81dab5e5a7190ff488cea6dbb7599e33a6dfea3829db4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 18 Mar 2024 23:10:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Mar 2024 23:11:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Mar 2024 23:11:33 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Mon, 18 Mar 2024 23:11:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Mon, 18 Mar 2024 23:12:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 18 Mar 2024 23:12:02 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 18 Mar 2024 23:12:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 18 Mar 2024 23:12:03 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 18 Mar 2024 23:12:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 18 Mar 2024 23:12:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Mon, 18 Mar 2024 23:12:31 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-windows-x86_64.exe
# Mon, 18 Mar 2024 23:12:32 GMT
ENV DOCKER_COMPOSE_SHA256=27289c82fe3ee64eaa415ae47f028f7c6af6ab347f1af4fde0e0d7d2b4a84dbb
# Mon, 18 Mar 2024 23:12:55 GMT
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
	-	`sha256:c8020eb2d98c691d0727ea9fa8ab9f12a77126009eba0dba71007184b2211c8c`  
		Last Modified: Mon, 18 Mar 2024 23:13:04 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3ab33904625356327587728dfe1460ffa81dea55e7aa2ab3e9fac76b871667`  
		Last Modified: Mon, 18 Mar 2024 23:13:05 GMT  
		Size: 490.4 KB (490418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014c6d377101847480473ea0618d5499e629f1d026fb0a6614cef4eed9a35e82`  
		Last Modified: Mon, 18 Mar 2024 23:13:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987a4cd16f91ad0ec59e1fb954e04789e46eb4e22717fe1360203eee2267544b`  
		Last Modified: Mon, 18 Mar 2024 23:13:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9817e2b64f85bfbd2346b1e545c5844015deb8cb84645ed39e6d97adb4c43770`  
		Last Modified: Mon, 18 Mar 2024 23:13:05 GMT  
		Size: 18.1 MB (18102727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484deedd297e6ec099143e032dc8a54ba9e35258d2ee799babda2963f313d130`  
		Last Modified: Mon, 18 Mar 2024 23:13:01 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4318ab0536a56a12af7311add4cd8c0a0fce1f493210f28515600ab72e04ed62`  
		Last Modified: Mon, 18 Mar 2024 23:13:01 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78005a0d87b2794ebf3aff10bc242cd450745843e6df24d3421d46e1a89bed7b`  
		Last Modified: Mon, 18 Mar 2024 23:13:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941d5b78e32d43071e2eb8e5b285d5a3265fe36881da326a7dc5430abfd45822`  
		Last Modified: Mon, 18 Mar 2024 23:13:02 GMT  
		Size: 18.8 MB (18836017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a446706ad211660fb9cd61772514f9698621523d25c3108ede1b84d90fc19`  
		Last Modified: Mon, 18 Mar 2024 23:12:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a822864adaa2e25e8a6d2e6bd759ada36a0a69881a2a5a35e38fee8a5f549b1`  
		Last Modified: Mon, 18 Mar 2024 23:12:59 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811e80d4f1bad3ad7a844af8108379d2abd3cb21913afd9fc22feaa44aec7258`  
		Last Modified: Mon, 18 Mar 2024 23:12:59 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cdb5d87b6e0c98f782b65c156a551ef65b479f7d02959f6b0a99caab5f5c1d`  
		Last Modified: Mon, 18 Mar 2024 23:13:02 GMT  
		Size: 19.1 MB (19081143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
