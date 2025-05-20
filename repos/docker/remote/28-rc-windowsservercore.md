## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:b1fbdd7649be32f64f12788fcd4d26bd4fd71b76cf9cb707eb76b01c39cb3347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:f9f79b35f18b56395b8b360bf83addbac5b1da496de46fa7f2b765074c42bef8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459346774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2014fd10b36c39ef11c3bbf5020eac8fac30dd7c36688daef0dbf5287493fbab`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 22:03:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:04:04 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:04:05 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Tue, 15 Apr 2025 22:04:06 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Tue, 15 Apr 2025 22:04:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:04:20 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:04:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:04:23 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:04:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:04:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:04:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:04:37 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:04:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Thu, 08 May 2025 17:36:24 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91183b2a88e148dca95fdc63ddf9242f11339ce9038bd05fd528a47f77ebcbb5`  
		Last Modified: Fri, 09 May 2025 06:20:21 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b08db622f6ed809d3398f0012786f8331a4c270647bee3ea71256cd06ec4415`  
		Last Modified: Fri, 09 May 2025 06:20:21 GMT  
		Size: 414.6 KB (414611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf28ff6d5ae985d808794c1797af3a827c47a9e541a73ea5195300032674e57f`  
		Last Modified: Fri, 09 May 2025 06:20:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd680cf57a45b235b43b6e47acfe000305cf88ca6337b8b766182d1fd93473da`  
		Last Modified: Fri, 09 May 2025 06:20:21 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca77b3effd4271362131982258dca41b2b7f7210ad86ff87e091bdd69bfbc31`  
		Last Modified: Fri, 16 May 2025 17:11:47 GMT  
		Size: 19.9 MB (19936516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc439e7b5dcd89838451a4fb16687f89932c9772da7dc822339859ae6c63bad`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee2c50089d08c3e89bd35fb8dc35a8a6b3f02a800ffb840228f03cc8b50e8ec`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23738aa6b5ed990f136e101c0049f0d75505f0877824c4cbb24d45494428eedf`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea7c93aa52117155d66f23e00e3fde9fe191d2f42972ca04f132f95f5206f50`  
		Last Modified: Fri, 16 May 2025 17:10:17 GMT  
		Size: 22.4 MB (22411622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0980586e177a08e20fc55ad3763a03121f648b8838c1763921f2283558243a04`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16bdc99cc42be98ae3e10f4a6b0b00f86f4017a0a4b6c6fe0e7b2137fe06ca9`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81ec503ae82985d6d43e418959a3196432a5439666828b5016b0cb8f1903fba`  
		Last Modified: Fri, 09 May 2025 06:20:22 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3fdef74f545d913c5819a1c9d01e8984a5b6a690b2c6e00c6773ea0e9d6cfc`  
		Last Modified: Fri, 16 May 2025 17:09:20 GMT  
		Size: 21.9 MB (21892647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:cbf9aeedaa940966bf2c5d1279dd1ba17bf848057ea3f282fdc22c1a17a21a22
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335440589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043ab734526d38e95b2e5c0b8d93734e5fbad3b304de716cb04084773b28ac32`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:05:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:06:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:06:03 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Tue, 15 Apr 2025 22:06:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Tue, 15 Apr 2025 22:06:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:06:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:06:17 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:06:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:06:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:06:27 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:06:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Thu, 08 May 2025 17:42:00 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb3c025d2865ce2d123ec98f46206d2a933b3de82189e720ac48bc8b42b60cb`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe7a17a6756b1156737fe7f201e0edd070fb50c7601af7e97bce2857c63a1ed`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 357.5 KB (357545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdde8583ba6c60e269770471113b2b235035599a89575b3735fabc72879177f`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a005b9f4e652ab8fa95aa0c9de090a43d26e97a86ee112bb89092e7a0370682`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18b25f236ecff8c233e3934d4eb849762c271c96f56fb91f9ad71d45c49d6b8`  
		Last Modified: Sat, 17 May 2025 09:35:37 GMT  
		Size: 19.9 MB (19880907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef52b76f20ebb7b07ad3a9b3396a1a23da0dd461d9a5489c5f2d67f6f207014`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e63f58a6b984f79761d84a865ae4c68b818883563b32d023c065de22b661949`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c840cecb3432a989f56bde5f5a3ee6c178c6e1f246e8446137571dc58f5e0676`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abd7cbcac2f656d16b886daf951211d98f50625d3e612b539ec89a4f9fa0a8b`  
		Last Modified: Sat, 17 May 2025 09:34:53 GMT  
		Size: 22.4 MB (22356375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717e7e72676e5d6bb62171449ca9a27313b6318dcfee79f32559a336d50033b3`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9820fe7c914314f249ac852de5bf2bb391160306e44e807104b8ce23fa360a`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e793b2fa7e6bbd811bc01c2a0c5444d6233d050f024cb455428d9b09ab47451`  
		Last Modified: Fri, 09 May 2025 12:39:19 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33deb3ae0749f96eaa6b7c90c5dc5787d4bdbc0763109300856dab8a19ee9142`  
		Last Modified: Sat, 17 May 2025 09:34:48 GMT  
		Size: 21.8 MB (21838550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:bbffb36fa13075d2a3778e2c679ce508a97d6282cc1048ccd9ff4c48bab06ae4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227136808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a9db8b010b661f3c759f63553819fb6ffabc14f077c712f7dc019645b34174`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 22:11:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:12:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:12:12 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Tue, 15 Apr 2025 22:12:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Tue, 15 Apr 2025 22:12:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:12:29 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:12:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:12:30 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:12:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:12:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:12:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:12:40 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:12:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Thu, 08 May 2025 17:41:33 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde229438835005c2995f8c6db35d55e3fe9154c302859fa977d57ce806ca5e`  
		Last Modified: Fri, 09 May 2025 08:19:02 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb2dd4167f46e5fd076b143811a9fb42a1ea606c1861f26e02309b269b925b`  
		Last Modified: Fri, 09 May 2025 08:19:02 GMT  
		Size: 340.3 KB (340323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f251cc62ae47fd0b192119ea1a2b13a2ca3027f5fbb5ae04cd066527356ad36`  
		Last Modified: Fri, 09 May 2025 08:19:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a511fd76e9ff785979b8f68bfb3521a2afb4bf9c75c21e2c761e8769e79b47a`  
		Last Modified: Fri, 09 May 2025 08:19:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca811736907d13d62432f1e0e17a00a734b61c2b20aa5829b01c037f70659a6e`  
		Last Modified: Tue, 15 Apr 2025 22:12:56 GMT  
		Size: 19.9 MB (19876171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23488f03eeeb3500f6e0c827006d3a6fe5c09db2b44f75f38491ee5e2972aaf3`  
		Last Modified: Fri, 09 May 2025 08:19:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad22b4d39fd8a9e29be066f8b01ac046219480675e6c4635edb18902e6f6ef3`  
		Last Modified: Fri, 09 May 2025 08:19:03 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0324b8947acabb01fa642dc7b013f9f1e8f7002f61aee0ac8d7aeac6aae030bb`  
		Last Modified: Fri, 09 May 2025 08:19:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed777abd70ec165306761f3cb7418fc39c524ca85bedd471479bbd92dd8fd0f`  
		Last Modified: Tue, 15 Apr 2025 22:12:54 GMT  
		Size: 22.4 MB (22352317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a0986850a5fd2327ff215d019f928fa1797a322e9cf6c675562965f23ea646`  
		Last Modified: Fri, 09 May 2025 08:19:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a1783a6102e422db72aec5bf8e5e61d73150d583ba8e746528971fdd51f6d3`  
		Last Modified: Fri, 09 May 2025 08:19:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4baa68c43f583dfbe10350cd9adb413ac89db04cb81d458b55fbf6089265df0`  
		Last Modified: Fri, 09 May 2025 08:19:03 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b7c2514da4ca93aef236e17d224224b7f35526b0b51ccefe157703b0260202`  
		Last Modified: Tue, 15 Apr 2025 22:12:54 GMT  
		Size: 21.8 MB (21830504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
