## `docker:27-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c68bdfb265f8b44bdcdbd856c52b597a0adc9e70d38d1073c2dcbeb23e26818e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:27-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Mon, 27 Jan 2025 00:02:38 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Mon, 27 Jan 2025 00:02:37 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Mon, 27 Jan 2025 00:02:50 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Mon, 27 Jan 2025 00:02:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Mon, 27 Jan 2025 00:02:47 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Mon, 27 Jan 2025 00:02:50 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Mon, 27 Jan 2025 00:03:03 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Mon, 27 Jan 2025 00:02:59 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Mon, 27 Jan 2025 00:02:55 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Mon, 27 Jan 2025 00:02:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Mon, 27 Jan 2025 00:03:04 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
