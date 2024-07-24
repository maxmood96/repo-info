## `docker:26-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:2d06b21f29c9ccb54ecd1c9e37fdfe843edcb74a438be47c1a8a43c6f499b427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `docker:26-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:b89d17c3a47fc9bfb8c221b29e949736e696a93eb463aff732069dd901dbd349
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198179047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac569a1f7f05e6f0188fe8e3ef1be040ade889141d93bb20e2a041803f9b0c3f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 24 Jul 2024 01:08:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jul 2024 01:09:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 24 Jul 2024 01:09:39 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 24 Jul 2024 01:09:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Wed, 24 Jul 2024 01:09:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:09:55 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 24 Jul 2024 01:09:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Wed, 24 Jul 2024 01:09:56 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Wed, 24 Jul 2024 01:10:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:10:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 24 Jul 2024 01:10:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Wed, 24 Jul 2024 01:10:10 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Wed, 24 Jul 2024 01:10:18 GMT
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
	-	`sha256:647e63b507940faf95fa4f5c1d5ac23f3c09c516eb78cc335615f4c87915c7ed`  
		Last Modified: Wed, 24 Jul 2024 01:10:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccccd487274ed39a983fff5b8c15d16f1c4115d9c9ede7578876501665918d2b`  
		Last Modified: Wed, 24 Jul 2024 01:10:28 GMT  
		Size: 358.6 KB (358611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9c2814a989681e1f7b4ccb4e3e6191cd9154d8286d149b09cdb0c893b2ee4d`  
		Last Modified: Wed, 24 Jul 2024 01:10:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97942dc570b7ad46adceff144cc2e121de9f9d729780706290568de1769a28`  
		Last Modified: Wed, 24 Jul 2024 01:10:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e1930638e4b38f1a8f1e01db8714fbc9944c481b9a7793e927f87592d6f57b`  
		Last Modified: Wed, 24 Jul 2024 01:10:28 GMT  
		Size: 19.3 MB (19254276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455f633a4c57db81888ff0a7f9007f329eb41b5e6ecef6387b0991425d02237`  
		Last Modified: Wed, 24 Jul 2024 01:10:24 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9908fae71e09279ac3cb07658c7b40c68665474df0174e29c3bbbb5e2dddd7`  
		Last Modified: Wed, 24 Jul 2024 01:10:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9358d8f4859b8a78f53e8814e0c01c6905116b5de744780a0d17370e40c033`  
		Last Modified: Wed, 24 Jul 2024 01:10:24 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e5238512c98ed7932e11b35097dbf4b5b85fbecb31bc8dadac6a8d144dbc3f`  
		Last Modified: Wed, 24 Jul 2024 01:10:26 GMT  
		Size: 19.3 MB (19259151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f434fecd01b30c0c586bc564a2411d0246db63e8a03e0c83d6878a67b0858f9`  
		Last Modified: Wed, 24 Jul 2024 01:10:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3f8c880274c3b9faa8d9f521a51a074d5f5b76b089047f1530bf84592b380c`  
		Last Modified: Wed, 24 Jul 2024 01:10:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4323006e68741530acae7ed5ac203cfd585cebe7c7f0bb91ef4759d627c9ec1a`  
		Last Modified: Wed, 24 Jul 2024 01:10:22 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31f05220d9e4e3a9cb1e0404355728f3569d57d24476b59e60e39a6675a4d88`  
		Last Modified: Wed, 24 Jul 2024 01:10:25 GMT  
		Size: 19.7 MB (19694881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
