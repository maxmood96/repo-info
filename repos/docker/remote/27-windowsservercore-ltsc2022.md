## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:db3ccde733db716c9738f43bc138f1501f5fdd358a8e0fc89d0285b4a69788df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

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
