## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a9266b0f45c2b149896e562c8414e4edc2f32d5f40c73cc8e69a23ce4a967d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
