## `docker:windowsservercore`

```console
$ docker pull docker@sha256:528a394441b948ca8fa2ccce01b95f52233729ab27342fb1aa0339e63eac858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8aa47cd924b443e6ed4f2293a2350df34e37e3840d7f2d10fa31ee848767b822
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459291937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554c35c4d3f914e6695b9b090d2e9d3f4038ed0707cc2979c1a8536f166c3b58`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 22:05:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:05:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:05:42 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:05:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:06:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:06:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:06:31 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:06:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:06:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:07:24 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:04 GMT
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
	-	`sha256:8ff803ad22e0ab64f102a722831537db638cc47772e62fa4f66ffc6a1de17bea`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650f48f4339554104a9b685c62ece86c0131ae6c202350e5f1a52e3a37ce006`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 405.2 KB (405161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc49ea6a08f7cb24b63b58139a6dd7d541e4be2c493b13edb6baeadc60ec9d`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d558fa4719a5fac8b7e21cdb0c03d7fb86edd8d43dc1def3abb70c02fcb75805`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148fc3d5ca192103ee3ae1835ce8a09f63c602ef431fcd5e749aa31c35237cdc`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 19.9 MB (19909526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71983d7eafa2374ca5c49782e81dfe35e5039870e7cd99abd2974726f1abdda7`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f2a4a7cef42383900d86e61ce89a2cc511ce078fbd6ef543452b57decc48f6`  
		Last Modified: Tue, 15 Apr 2025 22:08:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb3b7cf9449e0a48b9b27cc9b0f6deece3b5fbe51dd4f277c9570e360b2184f`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb088745c9e5fe660fc7a745b3a9a54607c55d7bae09a18c30a152001e325528`  
		Last Modified: Tue, 15 Apr 2025 22:08:13 GMT  
		Size: 22.4 MB (22401686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90041ef92672e9384ec94e0d96df6bb0002534b8aeefcfb5a4d714743ef3706f`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70fc9c300e4e7129f577f4f0812ba764164930ed15018563351f6be609e05d5`  
		Last Modified: Tue, 15 Apr 2025 22:08:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa5c78927c877cdbd1b451ae71d849f427bfdc3c04a356a4c4bb65152dc2d4`  
		Last Modified: Tue, 15 Apr 2025 22:08:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c4122ecb346154069beaab3457ca61e4629a9de2c32cbeb64f92387e9c96a2`  
		Last Modified: Tue, 15 Apr 2025 22:08:12 GMT  
		Size: 21.9 MB (21884365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:68e38ab953a87c61b66914217106b383daee357c4c05b1647ab3a95bfe7d79ce
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335455807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbf36de339df80f34209544c9b63f8b7d83ca23f9337314dfe2eaf417fd644b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:07:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:07:48 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:07:49 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:07:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:07:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:08:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:08:01 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:08:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:08:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:08:10 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:08:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30151e3643fba377542afac5a171a0527fd990206b8e89128562f09c6b6f761f`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4725ce2acf24e3219acaaa964606e83f8b4a7f2ff49c13f3261a641951a8b1db`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 365.7 KB (365726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9b91c0fe3a715c4879fa6fff556bfc191f884bdcdf19bbdbac4be05eab6fd`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919b934268d7cf70b58919f0e50f2a45315bff20b5f9b7e83faca5460b955586`  
		Last Modified: Tue, 15 Apr 2025 22:08:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737480d00e37347bf879f9271d4ebf5445bd23e5631768e209d02fabc332cf5`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 19.9 MB (19871309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbdcff4db952a6d899885eb2d490f38cc558e145ddd9895b34fdd6d7f8e7c87`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c7b3a352e7efdbbbb5c2e6eeea9ed5deb2f375780a083421b2a6d863238125`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45f0f2eb53c4197068fb31b358a34a63517e22eef46f899066d3417c1f86c05`  
		Last Modified: Tue, 15 Apr 2025 22:08:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07362729c8326851ce50b1c80ca2976934c0ccdee6a27216870ecc812ea693de`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 22.4 MB (22364101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c09098cac7c45c8f6f1cf5d8e638a25be610c8efd36fe246f0cf0097b1bfde1`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceaf713f2cf3069d80077b0c0dce7dd6b385d96f318a7fd5b600daf6953008d`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef372443d99cb8ae017ed4b09096ce301d468ff7d48f33711ffa40177c21a85`  
		Last Modified: Tue, 15 Apr 2025 22:08:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc61b0ba2c5210eb8100bc7189348241ae40e963445358cf48edf32774055787`  
		Last Modified: Tue, 15 Apr 2025 22:08:24 GMT  
		Size: 21.8 MB (21847429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:9eea48e8624f5a89b632b349df9a9ef60250b1c5ffa205d3d91cf43c32846ccd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227127342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785c3dec269da97ebda3793c1818235279080fd52a121be171f0b57b16ddba27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 22:12:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:13:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:13:23 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:13:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:13:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:39 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:13:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:13:41 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:13:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:14:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75559a6ab4985605769e9345e4dff1b1dcce036c5e3f010989bc5d815bcf22db`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc5225e1556802cd30f8fd34e34314e3d8b61a8646572689a40d59b303a269`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 341.5 KB (341494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5c9f84290e2fafec5927a5d6d17a3a064c93078c593270106ea74ad23ec29a`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcf429ac4797944cc945ce64dc94e477c8d14341b6fecaf29b9ccc44180cb2`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44bd61aef7b941f7614c31fb50b8660886b2740bbb23a09d281aef1f08832b`  
		Last Modified: Tue, 15 Apr 2025 22:14:11 GMT  
		Size: 19.9 MB (19860556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d18acc9d9a4944f4b68e2eb3b2056dc918d4f3155a9de9469b804883c9a870`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9fb93169fb4009bfe58fef0cb707780bf6d1452c6b71e4add92e8c230fd923`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d2981dd79b2395c71b1f2abf10aa7e31aafcd81b94c306767eb6394e5caf23`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a04a74dc2f144ff9e196e62a1c06e6277d5004443ce5b7de37e0d4aaa59a13b`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 22.4 MB (22354530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d80f4121c811468ee950acee266056e1e05a0e7ed4750dba28b1290f9444c9`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86e7151feda14da9b65f7fa4811a3d9f596a3f632eee42ca1a9173930178878`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62c931e923807455c87709bcd05a0d7067b18b8f1033c6fc5bb4f1d77c0d98b`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a55036ef8e12942d5bc9f5782020380597b798bdec106fbd29daa958030524`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 21.8 MB (21833195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
