## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:4e6ea45e298acb239e4143610c332202faf399f4f66df3eaa7a51500d2560b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:562488161c3ad138e726a9615c8bca16f4a935d4e60d2cb302546e9643b99f20
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198189951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1f2fb0df4d83855e9fddccb8e161f55aadb7f717d60377dd0e6bf41423f6b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Thu, 18 Jul 2024 18:55:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jul 2024 18:56:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jul 2024 18:56:39 GMT
ENV DOCKER_VERSION=27.0.3
# Thu, 18 Jul 2024 18:56:40 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Thu, 18 Jul 2024 18:56:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 18:56:59 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Thu, 18 Jul 2024 18:57:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Thu, 18 Jul 2024 18:57:00 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Thu, 18 Jul 2024 18:57:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 18:57:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 18:57:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Thu, 18 Jul 2024 18:57:10 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Thu, 18 Jul 2024 18:57:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ee5e0e94deb413583a5d116a86201c9279ddb4b684c8debdf6fc2444d95663`  
		Last Modified: Thu, 18 Jul 2024 18:57:27 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64532f2636f76e00674e9c274c11766c2214d9bb3863a9cbf048a3040674f89`  
		Last Modified: Thu, 18 Jul 2024 18:57:27 GMT  
		Size: 358.9 KB (358867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69cb55d00b08252d86638a63a1663985509e212904f2f2344d670cc225ecf0b`  
		Last Modified: Thu, 18 Jul 2024 18:57:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa5c1d90f09451a538d947aa900f4ef75dff1b953366acec8f41582de6b234`  
		Last Modified: Thu, 18 Jul 2024 18:57:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773876cac59cd03db2a2642e68f6d2003bf7d7f2e595189f4737f111bb9332f`  
		Last Modified: Thu, 18 Jul 2024 18:57:27 GMT  
		Size: 19.3 MB (19267858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6912aeffde20d84a5249f1b29eb9ada7001948dc1c59a2aa26bea41a15547116`  
		Last Modified: Thu, 18 Jul 2024 18:57:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593a3ef8cab098c5748bcec4a892b18c68173f3611ad1678a3a2e715b5af0626`  
		Last Modified: Thu, 18 Jul 2024 18:57:24 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1f3c8eb625b0ac2e82dd98ac894daf40ea65150a8d9000e278c1f9ce6e77f`  
		Last Modified: Thu, 18 Jul 2024 18:57:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f414aa6667504cebf139d43e72ddef4f323c6717ea24b3f837cbd9ed7117b1d0`  
		Last Modified: Thu, 18 Jul 2024 18:57:25 GMT  
		Size: 19.3 MB (19258675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e306dd43745eb88370448a5c04b4f494499a9ec6b0a737ec6ea92e83681ee79b`  
		Last Modified: Thu, 18 Jul 2024 18:57:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ddfa6506a357d64afcaab516df903dddaf7d5652d362e3fdbf3f8e45db7fe0`  
		Last Modified: Thu, 18 Jul 2024 18:57:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6040768cad9b6fd9f07b82cd06ce12276c2e897862b78ccf8dcd79f0d31cb61`  
		Last Modified: Thu, 18 Jul 2024 18:57:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfc5808e2bea92a2457c75950437aae259c36002f0ae7b10b8eaf9f332ae457`  
		Last Modified: Thu, 18 Jul 2024 18:57:25 GMT  
		Size: 19.7 MB (19692684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:cfbe1f1bb0716cbee1935234a98f9b06e7acad74a01927c053481aaec69eeb86
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297226774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f9bea8bcd0807b6e6f6c2419ec9faaef9f4ce68bc811c75f71de5442fac3c4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Thu, 18 Jul 2024 19:07:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jul 2024 19:08:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jul 2024 19:08:03 GMT
ENV DOCKER_VERSION=27.0.3
# Thu, 18 Jul 2024 19:08:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Thu, 18 Jul 2024 19:08:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 19:08:31 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Thu, 18 Jul 2024 19:08:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Thu, 18 Jul 2024 19:08:32 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Thu, 18 Jul 2024 19:08:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 19:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 19:08:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Thu, 18 Jul 2024 19:08:57 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Thu, 18 Jul 2024 19:09:21 GMT
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
	-	`sha256:ce210684a5d0bcf4dfb2672ad46979b18f73951830a2d01e178ac097e003b00f`  
		Last Modified: Thu, 18 Jul 2024 19:09:26 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776b6265c91faa2d0d3d551f7e3909a998e13851be4f5b988751415ce6e87ec7`  
		Last Modified: Thu, 18 Jul 2024 19:09:26 GMT  
		Size: 506.6 KB (506632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27581f5e63a84762646d651d19360c8c4656238ac31e8c8328e073a44bcf297a`  
		Last Modified: Thu, 18 Jul 2024 19:09:25 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ae451925f092538d6e38d94ebe0c2a5bc3e941be74e4e68c57cd1ddc5c3d6`  
		Last Modified: Thu, 18 Jul 2024 19:09:25 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48471da9bd7d742b927f7ed2f94503428d14ba3541898cc099876e8491c9b2df`  
		Last Modified: Thu, 18 Jul 2024 19:09:27 GMT  
		Size: 19.3 MB (19290494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0876984e328064ee0ad126981449f981f1f0ba15a6a280da1ef192945c1c4025`  
		Last Modified: Thu, 18 Jul 2024 19:09:24 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786edfa58be3744599a3de2544787125351ddd0f95d227e2c47be664dba55a96`  
		Last Modified: Thu, 18 Jul 2024 19:09:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001a487fb773f04c69254cea4aff9cd0da5fd078a5c4c55a1a99a5d2676a1390`  
		Last Modified: Thu, 18 Jul 2024 19:09:24 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362fae40432553e9c6371a0083e2121cd650a05e7557316e26c8c7b4e6e6e63a`  
		Last Modified: Thu, 18 Jul 2024 19:09:26 GMT  
		Size: 19.3 MB (19278128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb9c577352a544f212cd152e1d45ed865aeb0ecae4560d806b820dc6a112741`  
		Last Modified: Thu, 18 Jul 2024 19:09:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a4ff8cd324b3de49ad9ace444e3712116e2c15f5c10696cb00ff377f759f67`  
		Last Modified: Thu, 18 Jul 2024 19:09:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cecd4c80494b7abec22aa951bf22f29936425f201a8d5c8cec980d5da28190d`  
		Last Modified: Thu, 18 Jul 2024 19:09:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0262134c3a596a937fb7886519454ae1fb8b37c1a14b0a92e74f486851f3457e`  
		Last Modified: Thu, 18 Jul 2024 19:09:26 GMT  
		Size: 19.7 MB (19710454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
