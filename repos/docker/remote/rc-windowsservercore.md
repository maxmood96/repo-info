## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:eb93624c556f40fbb298db7087f3138071ebe3646a6f07ca763d7ffdf2bd801e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:rc-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:1f99cc5dff353b8e0ee4b058c8057425c6c9e75f2926c178713b67d9b13ac634
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542364466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098db58296dfc493a5cd39f2883c5a8cce6fd630e315ff5edfe40985c4052ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 24 Jun 2025 18:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Jun 2025 18:30:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Jun 2025 18:30:52 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Tue, 24 Jun 2025 18:30:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.3.0-rc.2.zip
# Tue, 24 Jun 2025 18:31:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 24 Jun 2025 18:31:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 24 Jun 2025 18:31:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Tue, 24 Jun 2025 18:31:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Tue, 24 Jun 2025 18:31:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 24 Jun 2025 18:31:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Tue, 24 Jun 2025 18:31:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Tue, 24 Jun 2025 18:31:20 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Tue, 24 Jun 2025 18:31:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca44f9504fbeca58404d55ef36d46b697bf986a5ecd29e620d0db450f177e4de`  
		Last Modified: Tue, 24 Jun 2025 20:08:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33699d8e7a66000b360b0ddef8df82f9bdb716fe38f85730e21731734d926c4`  
		Last Modified: Tue, 24 Jun 2025 20:08:30 GMT  
		Size: 400.9 KB (400869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27d4100c738c201e2792b6ac66733da4b5a91c374d012d6f4df0ff8f43e6c0f`  
		Last Modified: Tue, 24 Jun 2025 20:08:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284b1b40a97eeb52db7e63df2086fd7afa7b56c144289ad6ea71720d8182dcae`  
		Last Modified: Tue, 24 Jun 2025 20:08:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfe520baebf966058619e66723bfd894798267fb14f9cd7d6d381fbda434985`  
		Last Modified: Tue, 24 Jun 2025 20:08:32 GMT  
		Size: 20.9 MB (20864415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257de5096bbc2e08e4b577a12d4d1efa9a871a0c271151c82f46679a020d0c15`  
		Last Modified: Tue, 24 Jun 2025 20:08:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc9733c5c611859a38acde9c3f2bc6b7554bb9539a1df8ee3fe98758fe9c5a`  
		Last Modified: Tue, 24 Jun 2025 20:08:31 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335d77f42dc9d18299f118ec30c916cddc76787eb44d92d09f7493a8530c74f0`  
		Last Modified: Tue, 24 Jun 2025 20:08:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce32d211e5534921297b8253676be82a7928cdde4e689225e4da0b1e8870796`  
		Last Modified: Tue, 24 Jun 2025 20:08:33 GMT  
		Size: 22.7 MB (22686853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0455a4660737e8d962ad1e6f3dba8dac922f634e7fc6d021a69bf0a0367e8d`  
		Last Modified: Tue, 24 Jun 2025 20:08:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ad914d9af6aff3f162ab97cb81f43d017b75d38e7b9dd47723e1e587801772`  
		Last Modified: Tue, 24 Jun 2025 20:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca6867ea127d1d1884bbebdbd2decc39620aa54fc45812ea92f0ce5c84828bc`  
		Last Modified: Tue, 24 Jun 2025 20:08:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0057f1080cf587761cefc42b1d34b489e2e189d933a812a3a4dcef6717a85b`  
		Last Modified: Tue, 24 Jun 2025 20:08:34 GMT  
		Size: 22.2 MB (22226556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.20348.3807; amd64

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
