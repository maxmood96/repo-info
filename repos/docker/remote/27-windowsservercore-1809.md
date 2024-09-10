## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:498644c5c8316f5838bb0230478d1d6a6a2d605565f77cee2ce21c0397ba2ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
