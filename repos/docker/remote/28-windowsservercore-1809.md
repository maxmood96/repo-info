## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:b1b84b973346b7b28665244361df5bd8e939ca5a9b53888cd5e0941ed4540aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:2c6a8960392e2d7fca08c0e6df7d278587fe1093f6da8b1d707559975c3ce115
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248819976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe7c270036f1aa74dfc024274330c8d4dbe5e3b053150389d95c889fee56bce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 30 May 2025 18:00:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 May 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 30 May 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Fri, 30 May 2025 18:00:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 30 May 2025 18:00:38 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 18:00:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 30 May 2025 18:00:39 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 30 May 2025 18:00:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 30 May 2025 18:00:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 30 May 2025 18:00:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 30 May 2025 18:00:49 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 30 May 2025 18:00:58 GMT
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
	-	`sha256:35f4a2ef7fb12e6b7fa7395b6c758f7cfad5970e545a91633a30f9a19b69ec06`  
		Last Modified: Fri, 30 May 2025 18:01:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312642460bb65b424998daab15c7c0118ffdff383bab63095c0e936ba91940bc`  
		Last Modified: Fri, 30 May 2025 18:01:08 GMT  
		Size: 362.2 KB (362170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5e8d995e1f8f16f00d6849fcf4eb70cf2ac7da208f1085a70c27d91836bd51`  
		Last Modified: Fri, 30 May 2025 18:01:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7c00a5c88f267259fc3aa32ad5dd91d83ea71572f0dd0902ff80f1a43e6392`  
		Last Modified: Fri, 30 May 2025 18:01:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710748b13f3a3af594a4efd38cb8707e498c23d4bc4e803d58c0091e5d71d730`  
		Last Modified: Fri, 30 May 2025 18:01:08 GMT  
		Size: 20.5 MB (20456190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bab35b0a6b3ddc07de4bda0a130b14c87ace34ef856078970bec68733e755dd`  
		Last Modified: Fri, 30 May 2025 18:01:04 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65995b7a1806914254cfdf189fc4ff79187b934346deb55c85076645368f9c92`  
		Last Modified: Fri, 30 May 2025 18:01:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfa68bc1c270d0feb737429e87ac90ffed98c2b8bcea1dc40426db5896ed5f4`  
		Last Modified: Fri, 30 May 2025 18:01:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4673d74fc6a9adfdb4cc2b24ff77cf4095ddba48ffe7e3098c7e3be7c40d4b98`  
		Last Modified: Fri, 30 May 2025 18:01:05 GMT  
		Size: 22.3 MB (22264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354a6f9f775c4eda61724c0bc99d4cf1a610ad0182da4116f52d9a1663c65755`  
		Last Modified: Fri, 30 May 2025 18:01:02 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebdfbf479625a9397bea78fb82ecf6db77263c6bb55e4753d1cb800b6c36d9b`  
		Last Modified: Fri, 30 May 2025 18:01:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ac18a988b51febf8ba1ddf38e6a960bdc33aa8552d8fff73ac80d74c542eae`  
		Last Modified: Fri, 30 May 2025 18:01:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dac3766e21ab67cf0360ab80f75b298370ffefc69b8c4676f18f41c4bf3f0b`  
		Last Modified: Fri, 30 May 2025 18:01:05 GMT  
		Size: 22.0 MB (22007661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
