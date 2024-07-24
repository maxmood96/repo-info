## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:960783b29ff87edcbb5c8aa5ef32e5218d5b63256cee42f488259eb6f7892a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:6f0c35dae00a2eae9912acc55b1cdfeb185c0b7b6df9b36c73a88dffb2aed8fa
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297194236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf03627dc2f97f6e82b89c114b9c08999195e61a949753a98f5359c58ae59dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 24 Jul 2024 01:08:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jul 2024 01:11:29 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 24 Jul 2024 01:11:30 GMT
ENV DOCKER_VERSION=27.1.1
# Wed, 24 Jul 2024 01:11:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.1.zip
# Wed, 24 Jul 2024 01:12:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:12:08 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 24 Jul 2024 01:12:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Wed, 24 Jul 2024 01:12:09 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Wed, 24 Jul 2024 01:12:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 24 Jul 2024 01:12:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Wed, 24 Jul 2024 01:12:38 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Wed, 24 Jul 2024 01:13:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be9bdce5f994ccd7b442f38003d833a7ccd05bfccde358c8b0b1eded942ae58`  
		Last Modified: Wed, 24 Jul 2024 01:13:08 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8dcb3cf3e0e757661c18029d323cac7f3fae1ca682b232ce59915342c5ae426`  
		Last Modified: Wed, 24 Jul 2024 01:13:08 GMT  
		Size: 498.8 KB (498849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb89d32e9eb61900e1788d40fa4ae88f37cc999dd8520e2877efa8ea9c5560da`  
		Last Modified: Wed, 24 Jul 2024 01:13:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56274307b802cd55cd67ab8e0e784171f54e761527b96839f011c89b4657cb13`  
		Last Modified: Wed, 24 Jul 2024 01:13:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba9a36a82e2ffa0f57bdc1612eddddc6715dfd95ed45312adb1f55556b8eaab`  
		Last Modified: Wed, 24 Jul 2024 01:13:08 GMT  
		Size: 19.3 MB (19300032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9613d78e0a76afeb8af738bd876c4c8e904224cd594cae2597fb4c59dc9e959`  
		Last Modified: Wed, 24 Jul 2024 01:13:06 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acf6ec8949d5f53a98e85bcd4a4d4d0fd229f9466cd2b25b2c5508d823465fd`  
		Last Modified: Wed, 24 Jul 2024 01:13:06 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38da8c187d6ca95a572a7d49dc27ba2a9e29a64ef9584e41455f56edca99da5f`  
		Last Modified: Wed, 24 Jul 2024 01:13:06 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a6b466e33d0a1039c4fbdd697caa9e590fef7b9d1af8f791629c1238fdcd7`  
		Last Modified: Wed, 24 Jul 2024 01:13:08 GMT  
		Size: 19.3 MB (19262571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b9a3b01112f5d1f49dd1ab9a87186cdd730a8619bd10805b08e1dba614733c`  
		Last Modified: Wed, 24 Jul 2024 01:13:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173b8d18a9506257866ac72ff81b3ed73fb1df9227bd63d8df4aed32746b79b`  
		Last Modified: Wed, 24 Jul 2024 01:13:05 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167afd8d5ba8e20cc33e2cced00ff0ea66e2f05f292d2029d0ba26205bb7e5dd`  
		Last Modified: Wed, 24 Jul 2024 01:13:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a028fec79640db266de433d1feec943f2cbe84ca7081ed0aa8da42d07a6484`  
		Last Modified: Wed, 24 Jul 2024 01:13:08 GMT  
		Size: 19.7 MB (19691663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
