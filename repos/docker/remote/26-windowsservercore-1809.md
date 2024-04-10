## `docker:26-windowsservercore-1809`

```console
$ docker pull docker@sha256:80908f0f99ab9d4f188a9aa03c05db96c94ded90a3fbd34a8e972a4e3b8316c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `docker:26-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull docker@sha256:527c25e2e21965d9ea3562044494c65282a15ce6e466f47d090e20d0ff5e8598
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221363845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b25a58fb8993e75fc436fe83c6e7e6667400fdf218924650ee765fdaf85730`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 00:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 00:01:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 00:01:03 GMT
ENV DOCKER_VERSION=26.0.0
# Wed, 10 Apr 2024 00:01:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.0.0.zip
# Wed, 10 Apr 2024 00:01:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 00:01:33 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 10 Apr 2024 00:01:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Wed, 10 Apr 2024 00:01:34 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Wed, 10 Apr 2024 00:01:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 00:01:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Wed, 10 Apr 2024 00:02:00 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Wed, 10 Apr 2024 00:02:00 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Wed, 10 Apr 2024 00:02:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9a02ad73a710d80ac4121ad8626deeacbadb9849803f8d8abb4781ac318ca7`  
		Last Modified: Wed, 10 Apr 2024 00:02:30 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfb4d0c4ef2dc269217b8eaf2000721d33181b6dc3dd58deaafeead4ba4f2e7`  
		Last Modified: Wed, 10 Apr 2024 00:02:30 GMT  
		Size: 464.5 KB (464514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f207e54329ba659e2db48827a3ccca590bbe8f42abc3e48956f636ae8baeb2a`  
		Last Modified: Wed, 10 Apr 2024 00:02:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7621a0ab0cd5df9c2883e548bd06ce872cffe6fa657db3da8d521097315c80`  
		Last Modified: Wed, 10 Apr 2024 00:02:29 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d36af13929b1908245ef06150b53967c5b11dd0c55a557d46af09a217c28b0c`  
		Last Modified: Wed, 10 Apr 2024 00:02:31 GMT  
		Size: 18.1 MB (18135172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1193a9463f4d308f6539e5662f7f8305b196d52d26c6841cf093f209737b9be9`  
		Last Modified: Wed, 10 Apr 2024 00:02:28 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7002686fb3edffeb6e40520614146811c0e55ee0a0099b0e69b16ff881e526e0`  
		Last Modified: Wed, 10 Apr 2024 00:02:28 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3111e1f15a4c44b174ad57f24ad9626f326bf0e019f8c4b28ab8a4b4d225e9ef`  
		Last Modified: Wed, 10 Apr 2024 00:02:28 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a590c7a27ab908a4b84f6ba3d590bc40f4fbf7e5f175a6519b23f1ed4c4b345`  
		Last Modified: Wed, 10 Apr 2024 00:02:30 GMT  
		Size: 18.8 MB (18812686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2daf59a0ef70f4f5ebd2fcde3116b06f37b1d40d7246b50d32f93c403f6f69`  
		Last Modified: Wed, 10 Apr 2024 00:02:27 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21c853909e0f66c54588d9f5a830c4cd3f747ed0fcde93b089f9002cbca6c4f`  
		Last Modified: Wed, 10 Apr 2024 00:02:27 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7935cc1d06225b9e5cfaa9570e02ef38c614405a006c3060cf0ca6c41a537757`  
		Last Modified: Wed, 10 Apr 2024 00:02:27 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a79117c266fc96590f1ae5616abdfec64cc54082d5d04e92d99d55f4e59bd26`  
		Last Modified: Wed, 10 Apr 2024 00:02:30 GMT  
		Size: 19.5 MB (19511267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
