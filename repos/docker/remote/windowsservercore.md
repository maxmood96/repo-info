## `docker:windowsservercore`

```console
$ docker pull docker@sha256:32d6e626f79e39b5cc83a10d4fcc2fd8f090cf2052298b7081c073d05d6788b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
