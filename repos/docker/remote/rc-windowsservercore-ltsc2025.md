## `docker:rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:072127492846591148d78f73b4191283099be8385740b1904365aa95e9a7f82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:008491dd4704ab1b8a11df2c2facbaae62cbf13f1f3eb084bf59c309b55bf805
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496039642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df88a74a802c68bb96f4a42a9403c9e15c8a1dc8559ba8ec6beb8ba7cc8b0d63`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Sat, 24 May 2025 00:25:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 May 2025 00:25:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 May 2025 00:25:38 GMT
ENV DOCKER_VERSION=28.2.0-rc.2
# Sat, 24 May 2025 00:25:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.2.zip
# Sat, 24 May 2025 00:25:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:25:49 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Sat, 24 May 2025 00:25:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Sat, 24 May 2025 00:25:51 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Sat, 24 May 2025 00:25:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 24 May 2025 00:26:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Sat, 24 May 2025 00:26:00 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Sat, 24 May 2025 00:26:01 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Sat, 24 May 2025 00:26:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591ba866027e847bba934488c6162e7f9d007b94b3b6d849fcce274949614c3a`  
		Last Modified: Tue, 03 Jun 2025 14:28:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8c1fc070f7bb573566de5c32cac8a2a6465d1697557b6ac1219222aa6dc242`  
		Last Modified: Tue, 03 Jun 2025 14:28:06 GMT  
		Size: 405.5 KB (405542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b85ea38920df696011cd0d57850acede8d48effdee3c10c75c2bb91de923b5e`  
		Last Modified: Tue, 03 Jun 2025 14:28:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26217a3bfd56af5065ff92996301c310a1096a4199b876eb6afcba46613f405`  
		Last Modified: Tue, 03 Jun 2025 14:28:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6557f003920af4df18087d6072faccead9b88ba01434eb9ad218344f8edfca6e`  
		Last Modified: Tue, 03 Jun 2025 14:28:10 GMT  
		Size: 20.5 MB (20489398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47333bd02d7ea1e47e8d0a2a36b5eb4efecc86049965ae4fff31ed276140cf00`  
		Last Modified: Tue, 03 Jun 2025 14:28:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96671e2a307f6b7d41b0cf48acc54016c7bd4e28abf00a331c4ede591d82cce2`  
		Last Modified: Tue, 03 Jun 2025 14:28:12 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3fc6280d51c1f957a0cdea9702249e7af68e485b407594cdaeba1bfdd22ba`  
		Last Modified: Tue, 03 Jun 2025 14:28:13 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93922b4be4088d515b79ea36629984a45aaaa39cb1c540609622e346a5feca3`  
		Last Modified: Tue, 03 Jun 2025 14:28:15 GMT  
		Size: 22.3 MB (22306332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89696783c489b4ddcc75986af4711459af9206ccf5d1f5d64277beb4cc2040d4`  
		Last Modified: Tue, 03 Jun 2025 14:28:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3123ea3daae986d99a1a59cede98e9186600bb4d21dd67262a898ae4787b1763`  
		Last Modified: Tue, 03 Jun 2025 14:28:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75679fd384131448db62fc009bae9aa84d06bf1c4d1110f01546af3405da9155`  
		Last Modified: Tue, 03 Jun 2025 14:28:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bafdc1f5c25287448a070f7cfe47a9d43268f2c00891a0eb223c8f976641db`  
		Last Modified: Tue, 03 Jun 2025 14:28:21 GMT  
		Size: 22.1 MB (22060849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
