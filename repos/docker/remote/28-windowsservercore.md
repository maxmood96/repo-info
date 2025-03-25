## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:fdbf04adec3070897345d1e057af86328464a4e11f3f7426fc7b27e94e2eb517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
