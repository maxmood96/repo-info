## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:e44dacda967bcfb8e86873b35a93069bd77ee0a23631222ba53cc2db46c843d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
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
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
