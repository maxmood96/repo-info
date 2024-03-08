## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:bf633d19d62adc9ba442e47bd6e99e91d0fdc2dba81100d00dc4c1cfc0b7d64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull docker@sha256:cf1d6b5cd1243c1ecbdc99de19b5d11752abd4bfd7fab5fdc6072175564c123d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136440693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3114f93bf32c622021784e779352d839eecfdb12c8a12a98cde9a62dbe8db7e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Fri, 08 Mar 2024 16:55:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Mar 2024 16:57:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 08 Mar 2024 16:57:00 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 08 Mar 2024 16:57:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Fri, 08 Mar 2024 16:57:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 08 Mar 2024 16:57:34 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Fri, 08 Mar 2024 16:57:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.windows-amd64.exe
# Fri, 08 Mar 2024 16:57:35 GMT
ENV DOCKER_BUILDX_SHA256=001dd8c707862d7c7a7bc17ebb024922ee304bddad1bca11da5b3b3ff18effa6
# Fri, 08 Mar 2024 16:58:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 08 Mar 2024 16:58:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Fri, 08 Mar 2024 16:58:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Fri, 08 Mar 2024 16:58:07 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Fri, 08 Mar 2024 16:58:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7603f6103964c04a5b0815666abc74135a333d80b63d2fba55fbda26edbeca21`  
		Last Modified: Fri, 08 Mar 2024 16:58:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e8c69f6b6568435a7f2f807f52c639309da0285bcf823e2e01b0e8851c2ba5`  
		Last Modified: Fri, 08 Mar 2024 16:58:45 GMT  
		Size: 498.8 KB (498786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ed8e5b348163603aecb12ba5bc412e6d376ade07420ad15be24d0646c04b31`  
		Last Modified: Fri, 08 Mar 2024 16:58:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79b685568a95650e36fb7033546e7b448c8622871650a4ae60134d0a8765cd3`  
		Last Modified: Fri, 08 Mar 2024 16:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb317331a3698317d0b72389fa29d1eebe3c4216ddf551706253c70b12934f`  
		Last Modified: Fri, 08 Mar 2024 16:58:45 GMT  
		Size: 17.6 MB (17551360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcfbf049752b4c4635b63a662f6f1df1e4dc737f1b6de942a440a1c5d5e5dbb`  
		Last Modified: Fri, 08 Mar 2024 16:58:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43242d3ce205d6255f92b83f67fdf1aecd58aef1cf8209d76989790dc7c9b88`  
		Last Modified: Fri, 08 Mar 2024 16:58:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0cfdee36504c930169c2267cbee8335b2549aa26b79481bc6d287e89b45e51`  
		Last Modified: Fri, 08 Mar 2024 16:58:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab99ca7e253f9caaea3845b2b901d93ed9ffff84c9b757639e7dbac2b3c9b01f`  
		Last Modified: Fri, 08 Mar 2024 16:58:43 GMT  
		Size: 18.8 MB (18841796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff903f7ecfb9431c8d0f95692a22c96626b2df9c8d7cfcaa4d37a83efe7ff9`  
		Last Modified: Fri, 08 Mar 2024 16:58:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49966d9118fc7f50881980f1eb48edf3b6d9a395ef78185b24407fb5c400ef93`  
		Last Modified: Fri, 08 Mar 2024 16:58:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e61d81e888c7e4c0734e26b9ad14d3b7697250ff0ea568c1e0b4aaf1188d7d`  
		Last Modified: Fri, 08 Mar 2024 16:58:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeb3a0a7e675aef3065c5c0ef8b9f8ffac2571a2c8596a878a1b2d814702645`  
		Last Modified: Fri, 08 Mar 2024 16:58:43 GMT  
		Size: 19.1 MB (19088269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
