## `docker:windowsservercore`

```console
$ docker pull docker@sha256:0869de84e82e8707faa2238d565cea70e111fd670a2699eb7ed746f424fac81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
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
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
