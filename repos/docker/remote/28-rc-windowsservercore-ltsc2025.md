## `docker:28-rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b370518463f1035488f9969fdeff982f44fd7ce2aebca69af462af279fdd2bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:28-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:cd33e30b3873a9573c16b668c612e01a4b11a5b62878c71c94e98624676f0c62
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496180675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eacd7dd31f80b867b7f3a2a76dd5b3919cd281aec1f34e7209b7f4818542de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Mon, 19 May 2025 23:50:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 19 May 2025 23:50:54 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 19 May 2025 23:50:54 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:50:55 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Mon, 19 May 2025 23:51:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 19 May 2025 23:51:05 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 23:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Mon, 19 May 2025 23:51:06 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Mon, 19 May 2025 23:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 19 May 2025 23:51:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Mon, 19 May 2025 23:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Mon, 19 May 2025 23:51:25 GMT
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
	-	`sha256:6ad34cfe431afeba829bb483c800d938b62321c6a0c3e4466a46f62c06a53c4f`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ff3d258acf41f6e15e68503586fd127706a5267dbac3e98eeab9a5117a207`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 381.5 KB (381497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219802eddc8cdcf95e92bdd39a89edfccef429435c724dc21a2717d25e167011`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075e3e84399ca5931d2f68d5b60a52c0d159f11c1900832226cbd8ea29405eaa`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26c38545c68741a5efd8c7f144919505f98c4d08540a300cd2435e34838ab7`  
		Last Modified: Mon, 19 May 2025 23:54:55 GMT  
		Size: 20.5 MB (20474953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a53b09719e1c6ca93dc68f28f076971f6ffcb756479fd6fe5f0c5e1528380f2`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5796fb7a71f8fe87f9184a1cd28ec05b381f18961c7f17ed17996e2ca4bbc495`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84cc3c5e1ce75870c6fbbb37a47b6795a1a532454261812e58db2602f891ae4`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a492c29b63feedcd1a26796e55560bd9a8ad07eee05e63e401557803da288`  
		Last Modified: Mon, 19 May 2025 23:54:56 GMT  
		Size: 22.4 MB (22379291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49005344b8db08711374a5a2e52cdd68e558278daecbf01e44bc1ed60a4883d8`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6281c40f1074eca464b36919af1b64cba6051f0b469f28f9554e710bd8a2bc3d`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c08cbe257d7f4a0179e8f7538b140301ee93d26d637eb23e8437ba293b3f7e4`  
		Last Modified: Mon, 19 May 2025 23:54:51 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a2d425ccb7681aee1a40a9226c80bc8295f8a3ee377491641c190d18744377`  
		Last Modified: Mon, 19 May 2025 23:54:56 GMT  
		Size: 22.2 MB (22167270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
