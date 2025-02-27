## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:72fbdf9a1589337f3caeba7da90ef16a7885d2333db02a8ffdeef1d01c451f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:9f39f3e36bd0db102888bf04d8d52f8e6f1753cf0ab7e591e6e51a9f81ed6e65
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201748762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef1d801cdb38f6efda957494a496df60a03478aca505754ccbbff81685d59c2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Wed, 26 Feb 2025 23:33:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Feb 2025 23:34:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 26 Feb 2025 23:34:02 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 23:34:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 26 Feb 2025 23:34:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 26 Feb 2025 23:34:15 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Wed, 26 Feb 2025 23:34:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Wed, 26 Feb 2025 23:34:16 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Wed, 26 Feb 2025 23:34:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 26 Feb 2025 23:34:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 23:34:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 26 Feb 2025 23:34:26 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 26 Feb 2025 23:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e9f17482bed208c01b8dca8dfe66f10c5230ef4c0c3c8cad13d214f0f4f9d`  
		Last Modified: Wed, 26 Feb 2025 23:34:45 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed2ec8abc9902916400c0d1c10d4250a312bfc8b8c9c49b48d1b73bcbb9a828`  
		Last Modified: Wed, 26 Feb 2025 23:34:45 GMT  
		Size: 354.5 KB (354495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdd4f8630c5e53b3962882378d3504217ac80207c770416d34534a5d60c74f2`  
		Last Modified: Wed, 26 Feb 2025 23:34:43 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ebbc173b01de19a0369a9652da5bd1bce2dd6f7665125e1c164f41ce785d3e`  
		Last Modified: Wed, 26 Feb 2025 23:34:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898d918f8c29d0f4379dfc295d7b1cb5793193740a413341ebad5eeef1b8b26b`  
		Last Modified: Wed, 26 Feb 2025 23:34:44 GMT  
		Size: 19.8 MB (19827101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841b4019abaffa129d36787e795997e278aed80117661ab161cc2b438ba24fb1`  
		Last Modified: Wed, 26 Feb 2025 23:34:41 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3a0bf01b618f47c3dfe78845ef114bb3039ddfb4d7e4d98d77b7034b903810`  
		Last Modified: Wed, 26 Feb 2025 23:34:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941d7f01b1a05147deeb991aff19c10bc4bbe5d633b4e8f8b3270c321be5f8ac`  
		Last Modified: Wed, 26 Feb 2025 23:34:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b5286049e36c5d5db8fa246ecbeae606a90d40c9a7c1266eef087a227e20a6`  
		Last Modified: Wed, 26 Feb 2025 23:34:42 GMT  
		Size: 22.8 MB (22753639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2659cfcb2ab491dbb8865fd55ad128ca163c0fcca381e7d24f7e96aecbfb0b8`  
		Last Modified: Wed, 26 Feb 2025 23:34:40 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b288e355b4f4d5c4026984b508af94e940dd1aaba1f7e1ae635d363a03c6955e`  
		Last Modified: Wed, 26 Feb 2025 23:34:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bf47db51955e7a6c6eec58ba2927e02f52c22524c96c13577b758d019943fd`  
		Last Modified: Wed, 26 Feb 2025 23:34:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5bdc2130a92dad46b4c1895cf18bc5106acd4304fa6fec4c57582f19aac9fa`  
		Last Modified: Wed, 26 Feb 2025 23:34:43 GMT  
		Size: 21.9 MB (21893077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
