## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:079e64e60592185c083242443133b554f88c98cc577c7e7a6e42380cea7ec749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:57668e0b62b87ca0689c630ff25037e8fa5dba1ea32850ac5213d83bee2629d5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125355089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32dcd6648be5d66a87145f6967dc56e91ebaf415235ff5788000bdca761c21d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Fri, 19 Jan 2024 19:56:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jan 2024 19:58:29 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jan 2024 19:58:30 GMT
ENV DOCKER_VERSION=25.0.0
# Fri, 19 Jan 2024 19:58:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.0.zip
# Fri, 19 Jan 2024 19:59:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jan 2024 19:59:03 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 19:59:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 19 Jan 2024 19:59:05 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 19 Jan 2024 19:59:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jan 2024 19:59:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Fri, 19 Jan 2024 19:59:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-windows-x86_64.exe
# Fri, 19 Jan 2024 19:59:31 GMT
ENV DOCKER_COMPOSE_SHA256=6c94193c282d5fba71563c617fe8ddf8dce9355fb1d0ae93609221c590d06fcb
# Fri, 19 Jan 2024 19:59:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173261c7d76f7731c645ee859b4773786d7e2a738b5171706c8ace61e05e99d`  
		Last Modified: Fri, 19 Jan 2024 20:00:08 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8a5eedd61147fae6ca520f02f1ec7cb56193b568db43c982776c407ab20d94`  
		Last Modified: Fri, 19 Jan 2024 20:00:08 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb87d5d5a1ed6085c92752754f74fc48f71a51777ffb6e73b1d945ebee4b9771`  
		Last Modified: Fri, 19 Jan 2024 20:00:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ec0d5ec65e5384f8299766257c079ecfea03aaa81945b51c65b69a2de9c3df`  
		Last Modified: Fri, 19 Jan 2024 20:00:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89036e72efb6dc142bfc001e3d8d4d9bbdc1eb7899411b34945f548a858d00`  
		Last Modified: Fri, 19 Jan 2024 20:00:08 GMT  
		Size: 18.1 MB (18074275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff77026dcff958d025d7f1cd3fddfc8fe6057f41fdb295c5b0a26a3e283eeb1`  
		Last Modified: Fri, 19 Jan 2024 20:00:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c437f728f4db1be5aa00f5446d469980a132ba7852f5deea5d722dc2ca704d6`  
		Last Modified: Fri, 19 Jan 2024 20:00:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8c624e397799dfae64ad1634055abb153d449481b65d7f4eb1bc7176579f7`  
		Last Modified: Fri, 19 Jan 2024 20:00:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781b9e60725ba21ec51aa2386a286f0041009fec19f71be24f4e38cc4de4c3a6`  
		Last Modified: Fri, 19 Jan 2024 20:00:04 GMT  
		Size: 18.0 MB (18021866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af3bc34dd63971cf6b7986866fc7f2ccf8b1ae751b914c4785b9c36aed9b503`  
		Last Modified: Fri, 19 Jan 2024 20:00:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c9e510ee0a9f52741ff87a85e4e9a1264753e21e6a879af0f2136060cabbdd`  
		Last Modified: Fri, 19 Jan 2024 20:00:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850fc6804413c679e358a5be5c77fad94a002369955a323eca6e77583e9b80a`  
		Last Modified: Fri, 19 Jan 2024 20:00:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5772d55423ff6ffd9aa6bf5044f9e4dfa0e48d2813e8ea60b7884a0ded579a`  
		Last Modified: Fri, 19 Jan 2024 20:00:05 GMT  
		Size: 19.0 MB (19028347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
