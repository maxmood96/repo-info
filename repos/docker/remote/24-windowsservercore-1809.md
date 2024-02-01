## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:878019d525ff25808959250c4d83cb372d4aeb8df1fdae8e92785408e7517bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:a27f8172b4f76110d71932ca824fd4f92ae23470aab8e449ebf87040decb16cf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2124842490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eb5987607378bd7e3355df08d5d3eac3ba4cdb9982cc35c0778f6135ed4af7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 01 Feb 2024 18:57:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 01 Feb 2024 18:59:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 01 Feb 2024 18:59:32 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 18:59:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Thu, 01 Feb 2024 19:00:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 01 Feb 2024 19:00:04 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 01 Feb 2024 19:00:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 01 Feb 2024 19:00:05 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 01 Feb 2024 19:00:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 01 Feb 2024 19:00:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Thu, 01 Feb 2024 19:00:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-windows-x86_64.exe
# Thu, 01 Feb 2024 19:00:32 GMT
ENV DOCKER_COMPOSE_SHA256=eb60363d21a5c85eff2d2e18a4ed94d84d5016be59471d77d520046fdd888aa9
# Thu, 01 Feb 2024 19:00:58 GMT
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
	-	`sha256:9aa56036979a8df3922ae85f6ed34cc76aafc7934e15d8121dcfc4121bd09d98`  
		Last Modified: Thu, 01 Feb 2024 19:01:09 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c385be3d8e35802208caf58bf04f65689cad1d95b4e3190b552a303d48f35f1`  
		Last Modified: Thu, 01 Feb 2024 19:01:08 GMT  
		Size: 496.8 KB (496760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd75d680fbf49ebd5d7d0d1fdfcb6592dbce988a5f8e7eab07b21ed8095c2ad`  
		Last Modified: Thu, 01 Feb 2024 19:01:07 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f727bdef6ae9582b3c46ec95593331c04ce4262bca3c0f528af5d2b1c249bf`  
		Last Modified: Thu, 01 Feb 2024 19:01:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7e7ee6e29e71b1c61911c41845dd2adba485ec75ceff2db34194931aaa930`  
		Last Modified: Thu, 01 Feb 2024 19:01:15 GMT  
		Size: 17.5 MB (17542245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9016dae0c711fd44c75bb47b487c0fba27e51d5a9dbc81984267e102849856ff`  
		Last Modified: Thu, 01 Feb 2024 19:01:05 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284f67a428287b385cd97d81c0d1d1634bea5c613924d89269bb366352d94dcc`  
		Last Modified: Thu, 01 Feb 2024 19:01:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d93ea8d94c4c708f38c93f00d9f4dedb675e9fb4c173245d4b976a18c89ebfc`  
		Last Modified: Thu, 01 Feb 2024 19:01:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211d3a6b2ef943f79283a227290e818d134255754c42b5bd63592360df21ad12`  
		Last Modified: Thu, 01 Feb 2024 19:01:11 GMT  
		Size: 18.0 MB (18022201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05089c85ebb31f4a8026e595df9ebb06ec7044e4c01eea7075563298ae1930eb`  
		Last Modified: Thu, 01 Feb 2024 19:01:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77d23bb2be528523f1021e54ad869937d827383f3dc45c87fe5f78c8b46d900`  
		Last Modified: Thu, 01 Feb 2024 19:01:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7045a7ddff8b910f7ba1704a5ac58989f8a67d7f2122dc602a96a1c7df686608`  
		Last Modified: Thu, 01 Feb 2024 19:01:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1295f59313cbe156460c76fe7722327aae4f2772e615ff01fbed423bc4fc77`  
		Last Modified: Thu, 01 Feb 2024 19:01:06 GMT  
		Size: 19.0 MB (19047052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
