## `docker:28-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:e8964a31fd06b5aa59e2e7e4e878b247bc1ada97258b6bcb43c652d057ce0cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:28-rc-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:06a79cffaf68da7926340d24f845fed320e9b64a7665900d4f3a658f405722bd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf536d35ae666d87e1e0cfe20748723083eaeef7c27cb3e48c587ce7311ee8c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:35:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:36:29 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:36:29 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Thu, 13 Feb 2025 00:36:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Thu, 13 Feb 2025 00:36:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:36:43 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 13 Feb 2025 00:36:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 13 Feb 2025 00:36:44 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 13 Feb 2025 00:36:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:36:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 13 Feb 2025 00:36:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 13 Feb 2025 00:36:54 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 13 Feb 2025 00:37:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4744c3deb7b0b1d3f73097efb8605ad7bc1e941ec01a931aa2a97912359064`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725d9f5f9555ce801b3f3893ceb61bf76e797d392ec7e25267f5d060f28b80b9`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 345.1 KB (345141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee6b84b196406beb2b27cc661bc230baa83a1b0f1ae2e511369eed9f96be72`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb3e79be924c98aba3ba8112f16a6b2e6c8b34afdd869c1a2e9b0dc9852aed0`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8ef434a7dce698dd2e4c2b8022fa086933e72d19da2e141af2ad423e525dce`  
		Last Modified: Thu, 13 Feb 2025 03:09:37 GMT  
		Size: 19.8 MB (19772525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c150dd7cb9e15b3f07bebff1e0c9449ee9a894a3f85b9d38fa4e31b752af9808`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d1f12873ef1acfc6cfd03ad66fb9a471f0cd82c0c01455cfbb7b19084a01d8`  
		Last Modified: Thu, 13 Feb 2025 03:09:36 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd950211f965779fc2b9a8daf81948ebb9452b4ebdf7da7f09ede59b849767`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bc156f4fd48cda0f3da6ea579ccf40bb38784f6796cad7ea1ceb5ea5ea5a91`  
		Last Modified: Thu, 13 Feb 2025 03:09:38 GMT  
		Size: 21.1 MB (21138227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2327512adfc75585b198cf66a7f0d6522c9d2619288b4417fef0077d2145c33`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d81f2d6c8458fe74a35abfe34ff2bda06bf100fcf3c706b0a83bace3fdc98d0`  
		Last Modified: Thu, 13 Feb 2025 03:09:36 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f12f5bad9a67f336fd3f4138c09542665a9c36569648739ae4754422dcb369`  
		Last Modified: Thu, 13 Feb 2025 03:09:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce536efa2be640d3253db0f0f6ef0aa3ab5e21c78032bbc64395d746d6aff5`  
		Last Modified: Thu, 13 Feb 2025 03:09:39 GMT  
		Size: 21.8 MB (21815437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
