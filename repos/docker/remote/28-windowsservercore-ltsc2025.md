## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:21b7d8e9ae146bc83e8649d01d18aa2bf5a10a9ea1a65357d6e8d459c8085ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:4d46ceb145cdff708ee3bd2396ab9a745ef246c938eeff856713212b9e7de7e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459570471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0832d260304133a8b78b6b087074ddfc8185cb3a5248cbf64a41db34c13e09b0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Thu, 10 Apr 2025 21:48:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Apr 2025 21:48:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Apr 2025 21:48:27 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 21:48:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Thu, 10 Apr 2025 21:48:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 10 Apr 2025 21:48:40 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 21:48:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Thu, 10 Apr 2025 21:48:41 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Thu, 10 Apr 2025 21:48:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 10 Apr 2025 21:48:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 21:48:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Thu, 10 Apr 2025 21:48:54 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Thu, 10 Apr 2025 21:49:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd15627c1275aa6132f31f7febc0eb977de2385825ea21d72f3c18165889df9d`  
		Last Modified: Thu, 10 Apr 2025 21:49:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d912d86d6258640664ce12b122fb8ebb3b9680488a5f450100ba8b15cd0b1ab`  
		Last Modified: Thu, 10 Apr 2025 21:49:18 GMT  
		Size: 366.5 KB (366456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1674f7dd1960b4e489c9159566ec3f0e085eac49f49b6cbc7d4aeb28190b71f3`  
		Last Modified: Thu, 10 Apr 2025 21:49:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80f3e11bf0b6bc30d94841e1cea9e2434298e1253112e8f87a0c64004b69665`  
		Last Modified: Thu, 10 Apr 2025 21:49:16 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9111018a9f7fad636866fe4908c302005ddb91f23ad6a4a5fd378dedb6293197`  
		Last Modified: Thu, 10 Apr 2025 21:49:18 GMT  
		Size: 19.9 MB (19876863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d128ec093425b8e3d7dcdc0d3e045c3496a23fcfa837c4e1973fe8b348a612`  
		Last Modified: Thu, 10 Apr 2025 21:49:14 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5aeb01d6f678d1b9dca1baae4929cf38e70690d1489f20208915a6aa436c6c`  
		Last Modified: Thu, 10 Apr 2025 21:49:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8032644dcfca1c3b4874d575b20854210335a635a45298c0f872691a5267c95`  
		Last Modified: Thu, 10 Apr 2025 21:49:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c60586b0e8dbb76efb64fbed303abcdfb78cbd6ac396ffb0fad18728dd438f`  
		Last Modified: Thu, 10 Apr 2025 21:49:15 GMT  
		Size: 22.8 MB (22780461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0cbfaf52c3cdec2bfc34f30089dde1427e038af84064194e35be8c2b24e555`  
		Last Modified: Thu, 10 Apr 2025 21:49:12 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd76d74eccb260c67b7edaba5252ac8ca99f776d2a78537782a037593a8b167`  
		Last Modified: Thu, 10 Apr 2025 21:49:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c84975fe1731b231df94bb44c244b2cf48071fffc0498f6ecff443c9f4e4f20`  
		Last Modified: Thu, 10 Apr 2025 21:49:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8eb40bda031aef7284bc4b20fea9d5f8851485a7ca70270b8c0039658a466f`  
		Last Modified: Thu, 10 Apr 2025 21:49:15 GMT  
		Size: 21.9 MB (21855444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
