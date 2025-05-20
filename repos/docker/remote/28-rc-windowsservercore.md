## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:6f4f5ac70c1a86eb4583be3e6a35a17262dc05ae85708be646b19800b107609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.4061; amd64

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
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad34cfe431afeba829bb483c800d938b62321c6a0c3e4466a46f62c06a53c4f`  
		Last Modified: Mon, 19 May 2025 23:51:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ff3d258acf41f6e15e68503586fd127706a5267dbac3e98eeab9a5117a207`  
		Last Modified: Mon, 19 May 2025 23:51:34 GMT  
		Size: 381.5 KB (381497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219802eddc8cdcf95e92bdd39a89edfccef429435c724dc21a2717d25e167011`  
		Last Modified: Mon, 19 May 2025 23:51:33 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075e3e84399ca5931d2f68d5b60a52c0d159f11c1900832226cbd8ea29405eaa`  
		Last Modified: Mon, 19 May 2025 23:51:33 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26c38545c68741a5efd8c7f144919505f98c4d08540a300cd2435e34838ab7`  
		Last Modified: Mon, 19 May 2025 23:51:35 GMT  
		Size: 20.5 MB (20474953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a53b09719e1c6ca93dc68f28f076971f6ffcb756479fd6fe5f0c5e1528380f2`  
		Last Modified: Mon, 19 May 2025 23:51:31 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5796fb7a71f8fe87f9184a1cd28ec05b381f18961c7f17ed17996e2ca4bbc495`  
		Last Modified: Mon, 19 May 2025 23:51:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84cc3c5e1ce75870c6fbbb37a47b6795a1a532454261812e58db2602f891ae4`  
		Last Modified: Mon, 19 May 2025 23:51:31 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a492c29b63feedcd1a26796e55560bd9a8ad07eee05e63e401557803da288`  
		Last Modified: Mon, 19 May 2025 23:51:32 GMT  
		Size: 22.4 MB (22379291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49005344b8db08711374a5a2e52cdd68e558278daecbf01e44bc1ed60a4883d8`  
		Last Modified: Mon, 19 May 2025 23:51:29 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6281c40f1074eca464b36919af1b64cba6051f0b469f28f9554e710bd8a2bc3d`  
		Last Modified: Mon, 19 May 2025 23:51:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c08cbe257d7f4a0179e8f7538b140301ee93d26d637eb23e8437ba293b3f7e4`  
		Last Modified: Mon, 19 May 2025 23:51:29 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a2d425ccb7681aee1a40a9226c80bc8295f8a3ee377491641c190d18744377`  
		Last Modified: Mon, 19 May 2025 23:51:32 GMT  
		Size: 22.2 MB (22167270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:4bec6e19fc8ced9209c4787014e59b79286eb1399b801eee6e32f5bd477fb886
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338944992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f975efa5de6fc4f423382e714b89170e0da6d5807e30a6a717308731044a6f96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Mon, 19 May 2025 23:49:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 19 May 2025 23:49:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 19 May 2025 23:49:43 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:49:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Mon, 19 May 2025 23:49:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 19 May 2025 23:49:55 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 23:49:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Mon, 19 May 2025 23:49:57 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Mon, 19 May 2025 23:50:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 19 May 2025 23:50:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:50:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Mon, 19 May 2025 23:50:08 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Mon, 19 May 2025 23:50:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e13f10d1bc5bce38f8d29a317627e76624ed708d291658aaafb4b3008f6577f`  
		Last Modified: Mon, 19 May 2025 23:50:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc2b28cd47f994d39c757070171f42db4e7b8a8f7d1a28bca70ba2cdfb63f50`  
		Last Modified: Mon, 19 May 2025 23:50:27 GMT  
		Size: 356.0 KB (355987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f790ef636043a241e24cc20421ba3308ef6fb80c4c6bdaec57aef0aef4a5b0`  
		Last Modified: Mon, 19 May 2025 23:50:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61034518f5b935894fdc3c8cfb10d90316e559e8baa292c73552c2000de2e59`  
		Last Modified: Mon, 19 May 2025 23:50:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c251f303a5dbed05cb9d898a6b1d6f5185c847eadc69716ccf50e591a5949c`  
		Last Modified: Mon, 19 May 2025 23:50:27 GMT  
		Size: 20.5 MB (20453324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aef13bcc10a6f5946db7fa39831d48d919977c79255d714b5b58d087282e547`  
		Last Modified: Mon, 19 May 2025 23:50:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a0102a3b4f773ee1e28f6a36d9569d6a591a8d5f22b80da986209a7cef8d45`  
		Last Modified: Mon, 19 May 2025 23:50:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f470482e68ba15c5a525188018b71f938ebcb4c1126eb2e80b71d739b95742`  
		Last Modified: Mon, 19 May 2025 23:50:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642b667613e3d09cc3b85d51f0dc19b8f993ad143ec15de5bd71d8253c571ee3`  
		Last Modified: Mon, 19 May 2025 23:50:24 GMT  
		Size: 22.4 MB (22357077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20276411efba2d75b6c201467983e19b426e3ce522f6c97409c1e13467758a1c`  
		Last Modified: Mon, 19 May 2025 23:50:21 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6695487d1b4c651d20fe4c2a0bd0cbd85bff3d4a4347fe6c8c7397ea437c23c`  
		Last Modified: Mon, 19 May 2025 23:50:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3279687a903c8bd78b0bd3845f58d32eec052cb8cdfcb0c664239dd01fc65477`  
		Last Modified: Mon, 19 May 2025 23:50:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3808e740776dc967f6024a15b7bac856c2106713e566225ce2022385b27bf2`  
		Last Modified: Mon, 19 May 2025 23:50:25 GMT  
		Size: 22.1 MB (22138827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:cb01a9fdf485e746b9a0cab13413f40768e458f7270ee6e860183e5d1cc3d2a2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2249067043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87628b403ed12f76e3fd4667b0520943af970f172d9c29ffe751fdb0ed200a34`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Mon, 19 May 2025 23:54:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 19 May 2025 23:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 19 May 2025 23:55:39 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:55:40 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Mon, 19 May 2025 23:55:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 19 May 2025 23:55:55 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 23:55:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Mon, 19 May 2025 23:55:56 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Mon, 19 May 2025 23:56:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 19 May 2025 23:56:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:56:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Mon, 19 May 2025 23:56:07 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Mon, 19 May 2025 23:56:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff23a7e5e5f84ca73044593c59dd47ba0355c67d0f0b12ef00ceaf39fa49d1`  
		Last Modified: Mon, 19 May 2025 23:56:21 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd11ad4e3a5099b0a7194d64026663b46417b2498ec50ec5e28ff11676973a5`  
		Last Modified: Mon, 19 May 2025 23:56:21 GMT  
		Size: 367.6 KB (367584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bb1dfba0185a4a3831d7fb4713f44887a11842117d9ef6b28b192152071b69`  
		Last Modified: Mon, 19 May 2025 23:56:20 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815c20b1c35c6d3693d13c6011ec422e76131255ee83c3403964fb98671a6f1`  
		Last Modified: Mon, 19 May 2025 23:56:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61225e2253998d1a256f78d623ee05042795c57981ab522665a59072e752c1b`  
		Last Modified: Mon, 19 May 2025 23:56:22 GMT  
		Size: 20.5 MB (20463126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d7a20829c7f32c2aace9edd79f669f0a37b95cd07fea541fa5a7e8bb983838`  
		Last Modified: Mon, 19 May 2025 23:56:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657e06d5db97b12ab43d33ae02c5454f9d7497dc2594c3e2ada479d9e551d7d3`  
		Last Modified: Mon, 19 May 2025 23:56:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707fab8d39197aa75386167ce2e6ede26efab6e8509b36612c38bc2505f99db4`  
		Last Modified: Mon, 19 May 2025 23:56:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99190d95c3d6cce2bbddabe8712ad103a96e24a52d295c473e5e90bfce8fe39e`  
		Last Modified: Mon, 19 May 2025 23:56:21 GMT  
		Size: 22.4 MB (22366012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf0c9e342aa488ac123b9823aa05f42e6f409088c4b615cbf31dea6e87b224`  
		Last Modified: Mon, 19 May 2025 23:56:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6ce7decceef3f5272a4ad3215d44247db1f1375f85c38384faa59f25e63c83`  
		Last Modified: Mon, 19 May 2025 23:56:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee89c8c456cee6f97a4fb7dc49151e8a36d2389ea374913607c024b43d9124a1`  
		Last Modified: Mon, 19 May 2025 23:56:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7813869919bbb298b581be3ad1989b2539a98b94d325094ba8abd3f997322a68`  
		Last Modified: Mon, 19 May 2025 23:56:21 GMT  
		Size: 22.1 MB (22141178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
