## `docker:28-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c30d9b2fd053abe728c7e5ed1893ef50a0b261dde2c0dfbc26f92de26baaaff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:dc9ab14190c5e91567df559d4de3d4aeab07a5cdb5ed0f2d9412b4e614c78189
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346182400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dd0493883bede5e4ecf7e70ad4d6fd9a79db9a1c8c83c6716a6da3e8734a91`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 24 Jun 2025 18:25:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Jun 2025 18:26:20 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Jun 2025 18:26:20 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Tue, 24 Jun 2025 18:26:21 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.3.0-rc.2.zip
# Tue, 24 Jun 2025 18:26:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 24 Jun 2025 18:26:43 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 24 Jun 2025 18:26:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Tue, 24 Jun 2025 18:26:45 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Tue, 24 Jun 2025 18:26:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 24 Jun 2025 18:26:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Tue, 24 Jun 2025 18:26:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Tue, 24 Jun 2025 18:26:58 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Tue, 24 Jun 2025 18:27:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981dc64ace0b854f8fbc81398d4ea7e103b36f76e2af608946e24312a9ede489`  
		Last Modified: Tue, 24 Jun 2025 18:38:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d16c1e72c3b7acb8b4c6d0edb6ae807f0d7702214a2eb83ff73d523695a7768`  
		Last Modified: Tue, 24 Jun 2025 18:38:24 GMT  
		Size: 357.2 KB (357180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be19cdc6cdb830573763518cd0a9e3e7d2edc901d2eb048cb0bdd11375a9390`  
		Last Modified: Tue, 24 Jun 2025 18:38:27 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e198a53497c9e1b68b699435be1d01f3ee43b13407be9adf17c25238882a0223`  
		Last Modified: Tue, 24 Jun 2025 18:38:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95b02034523cae3b3ab831bc32d54a87f48410bac8bb43bee36fdedbb5327ee`  
		Last Modified: Tue, 24 Jun 2025 20:08:33 GMT  
		Size: 20.8 MB (20794561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877ae5777eb31342d073618445a2a580f2aee1b8f667b2735bc35248daae5e84`  
		Last Modified: Tue, 24 Jun 2025 18:38:33 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d36ac2b2707157c3bb7d76edf21ae6309ffe0f92ce31a351f103c88b010f68d`  
		Last Modified: Tue, 24 Jun 2025 18:38:36 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba4156e09017e9afc801e554536f602ea04375e6eed7b7490b747b701d7126f`  
		Last Modified: Tue, 24 Jun 2025 18:38:38 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c52f925f36e649e73898a8840c164dafa57158084ada8f0382ded6de308be1`  
		Last Modified: Tue, 24 Jun 2025 20:08:34 GMT  
		Size: 22.6 MB (22618204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f0b93ec54d9451f1e8683d908acf2a103efc1a427e7c83d480971879d3a7f2`  
		Last Modified: Tue, 24 Jun 2025 18:38:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af96ded1dbb0f5418f349f5eecc6d5cc6c598f98a55b95516b1555c74a612f1`  
		Last Modified: Tue, 24 Jun 2025 18:38:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42072d2606136acb7d498211f3bbbc03731c388e768baa176be5e0fc30fafe2a`  
		Last Modified: Tue, 24 Jun 2025 18:38:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f36f236bc72d8dbe73aa4ee1f7261d1a8a054b6c1087e7c4a9e3b08794f3bf`  
		Last Modified: Tue, 24 Jun 2025 20:08:35 GMT  
		Size: 22.1 MB (22149342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
