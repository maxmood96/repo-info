## `docker:25-windowsservercore-1809`

```console
$ docker pull docker@sha256:43f4713d50f858037905b212f590c2be6a5cf95311134531a5e661eabf6e430a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `docker:25-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:1bd52789ecfedbbd95fdc33ff99532cb9cf49a46c5725b5b880224729e606157
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295966213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5919a5eac69ace23b117efa9169a367626729558086ebf81497e1e48ed9b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Thu, 25 Jul 2024 21:00:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 25 Jul 2024 21:02:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 25 Jul 2024 21:02:27 GMT
ENV DOCKER_VERSION=25.0.5
# Thu, 25 Jul 2024 21:02:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Thu, 25 Jul 2024 21:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 25 Jul 2024 21:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Thu, 25 Jul 2024 21:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Thu, 25 Jul 2024 21:03:04 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Thu, 25 Jul 2024 21:03:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 25 Jul 2024 21:03:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Thu, 25 Jul 2024 21:03:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Thu, 25 Jul 2024 21:03:36 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Thu, 25 Jul 2024 21:04:03 GMT
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
	-	`sha256:bca9d7e7173350e3ea6aea13ccbccfdfd2b402cbddb57b1d22cd316d1b51ba49`  
		Last Modified: Thu, 25 Jul 2024 21:04:13 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9e325cbe4150ecae3c6de94f2e8bd49aa4d37d3e8b3866270b48ebee1b11c4`  
		Last Modified: Thu, 25 Jul 2024 21:04:13 GMT  
		Size: 496.0 KB (495995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec29bf930ede0703a7074db221320565d7bc7ca1986a4d794e17c4e3f39517b3`  
		Last Modified: Thu, 25 Jul 2024 21:04:11 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2442dbf170ca0fbf58e74fb340646460c1c4952c05eb5a6d6c856616821ebfc`  
		Last Modified: Thu, 25 Jul 2024 21:04:11 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a05f61bfc9c11898b244ea9a6bbd986d7d4c0e91c40834bb38a4a9ee1527ee`  
		Last Modified: Thu, 25 Jul 2024 21:04:13 GMT  
		Size: 18.1 MB (18077056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d064f6d195f350ab2dccdbce91222d108b079b09b9ade7b640e0952499343db`  
		Last Modified: Thu, 25 Jul 2024 21:04:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d1cb822018bf7817199cd9ab0f2720e1ce279a7838bbec65f5464f3361e77c`  
		Last Modified: Thu, 25 Jul 2024 21:04:09 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58353cf03d3f1e1d325f88129754b713e9313d6766b6af10e402baff5b01331e`  
		Last Modified: Thu, 25 Jul 2024 21:04:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea56d6e5f1c3440d2917212b5f535ebf909be910a00b7f9e12f0a4187aa10a80`  
		Last Modified: Thu, 25 Jul 2024 21:04:11 GMT  
		Size: 19.3 MB (19260904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05477869929ac80233b6d6a211501061507bb72d8d0721a2e934971e2210806d`  
		Last Modified: Thu, 25 Jul 2024 21:04:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09e900f66acd2c7ee9fb8e685ffa111b3807d4ce60df95f82bdee57dd8553ca`  
		Last Modified: Thu, 25 Jul 2024 21:04:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f02160bfc92bcba62b87236bdb05b0fa829a89cadf35244dffb5411000d30ab`  
		Last Modified: Thu, 25 Jul 2024 21:04:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6058bce4f1ed2bffa59c45d9efe6f6f8986f0fe32e106066b88b2802b48b423`  
		Last Modified: Thu, 25 Jul 2024 21:04:11 GMT  
		Size: 19.7 MB (19691130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
