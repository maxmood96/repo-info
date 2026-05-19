## `docker:windowsservercore`

```console
$ docker pull docker@sha256:caf096228175be53e5de66be0b3c3741fd45d9590a48519ebbe00843e9368680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:be11aca37fdf81f358f489b889b6ddd2ea11bd5ce032a72b9f72680a6a1fd6d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262577085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e9377aa0b725654fa410b6130c2c116687a27d5ebe5da0488091158a93e46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 19 May 2026 18:55:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 19 May 2026 18:56:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 19 May 2026 18:57:00 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:57:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.1.zip
# Tue, 19 May 2026 18:57:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 19 May 2026 18:57:18 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:57:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Tue, 19 May 2026 18:57:19 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Tue, 19 May 2026 18:57:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 19 May 2026 18:57:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:57:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Tue, 19 May 2026 18:57:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Tue, 19 May 2026 18:57:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67053e4dd0e3a27b79130356abcb6c5767ac9647ec10e8da1e81a43c7bd386a0`  
		Last Modified: Tue, 19 May 2026 18:57:48 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868cc8b1b439e4243b2e362b753b428d24a3526435d03fff1d97140877c04bfe`  
		Last Modified: Tue, 19 May 2026 18:57:47 GMT  
		Size: 418.9 KB (418908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1751190dd829301ec9c16837be3e854f9c19cff1435de89c0efc31d3b4e400`  
		Last Modified: Tue, 19 May 2026 18:57:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc83b2cc3c3f19cddbda5d2e1926195ff5af81eb61baa3481b8753b0d3ab990`  
		Last Modified: Tue, 19 May 2026 18:57:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea1ee7ca2fd72a1ef9ebd87d6d2eee611bd28863e1485f25efde358a09411`  
		Last Modified: Tue, 19 May 2026 18:57:48 GMT  
		Size: 20.3 MB (20284341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22a2c71b9130d15368c70a86eba06ebe75c3ae4480c0613f8dfbca9c80af62`  
		Last Modified: Tue, 19 May 2026 18:57:44 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfdeefbb0201639f3ef8edf77f4719e916f88d340d08d1fbfd2823a94f5b509`  
		Last Modified: Tue, 19 May 2026 18:57:44 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ec7aaf8755086af8fbad8304de44e1f81ef0e99a2d5e3317c37f282577a842`  
		Last Modified: Tue, 19 May 2026 18:57:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ee45fe318973bbb0e9f1b5dfaa29c637dd6f2d1ee8734915499d669c1322c0`  
		Last Modified: Tue, 19 May 2026 18:57:57 GMT  
		Size: 23.9 MB (23944841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b075e22b56d94945e9cd50c5631526ab35dd4bd2ef059a9cf9d952d83d923d7`  
		Last Modified: Tue, 19 May 2026 18:57:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fe6a75dc1caac7193ae6620fb301150dd195536b90a112c32231c54a1c152f`  
		Last Modified: Tue, 19 May 2026 18:57:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0085ee98be20d577820db9e6b0996ac7f7d02642e06ca0179ad9f6a89c5551c9`  
		Last Modified: Tue, 19 May 2026 18:57:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b083b70d3a54f524b5472eac0cb4ed62473642910d48a06775dc27137a767`  
		Last Modified: Tue, 19 May 2026 18:57:45 GMT  
		Size: 12.0 MB (11975521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:4ea76917dba7138fac2e0b2ef09e0316a1bd2d562e4f36102d87c13a3bef9f7e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178895575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5bea371f8111250e2abf1a580b3e00c1eef2b83f1376e701f47f0af7136a20`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 19 May 2026 18:52:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 19 May 2026 18:53:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 19 May 2026 18:53:30 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:53:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.1.zip
# Tue, 19 May 2026 18:53:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 19 May 2026 18:53:46 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:53:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Tue, 19 May 2026 18:53:47 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Tue, 19 May 2026 18:53:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 19 May 2026 18:53:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:54:00 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Tue, 19 May 2026 18:54:00 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Tue, 19 May 2026 18:54:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34d34a8127c5dbd0a114dd8ded3dffef884e75731e3899fc7e1f51b27872866`  
		Last Modified: Tue, 19 May 2026 18:54:21 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fab4b84264ea907ed96f8b70fe5a7df639db304ef6d6e5daa0be444f1e30411`  
		Last Modified: Tue, 19 May 2026 18:54:21 GMT  
		Size: 507.0 KB (506980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d7eec9abcc30752f14779dbb9c5ac60cf7b538479c18f4873a57d85eaa32cd`  
		Last Modified: Tue, 19 May 2026 18:54:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3628a9173b5588fad96395f95f72477fff566ac88a6acb578abba4e87e9c7f`  
		Last Modified: Tue, 19 May 2026 18:54:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f984ee40b0ebdcb0d264a201dfba71e3bf2007146feb38e7bd9cb40555d6d`  
		Last Modified: Tue, 19 May 2026 18:54:22 GMT  
		Size: 20.2 MB (20196999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440f748d7c5a810c62afcd392416b44d674c6801f7f3a56fba65a558a0c100fe`  
		Last Modified: Tue, 19 May 2026 18:54:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35c67f5426b37891f43d856fc39442637cc85e2ce390514ae511bc9410b9f05`  
		Last Modified: Tue, 19 May 2026 18:54:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd29f8fe9bac33d0087c1a1cf352d2206674926c2b26301fd0d9632a7ad565a6`  
		Last Modified: Tue, 19 May 2026 18:54:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768c98afab8e11c075744c17c6d40635ebb85d0fec37b9c468abf315173e2531`  
		Last Modified: Tue, 19 May 2026 18:54:20 GMT  
		Size: 23.9 MB (23867361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1136567d8b1dbb646acd711a9efcc4fc2e198bd25d985fe37ae68386411d5b3d`  
		Last Modified: Tue, 19 May 2026 18:54:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdbea8e3be1a9c4cf613ee25b1312aec54d19c5eb65d2a11dab67d989e3efe5`  
		Last Modified: Tue, 19 May 2026 18:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857e714df2d63c709315e2a57bac7299c7b55f2f5a68a2fec8359e0da8e5d2d0`  
		Last Modified: Tue, 19 May 2026 18:54:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adf4bbd47bc4e8be450f0a17cd55ee24878c168724a2df4ffc3b4165fb89727`  
		Last Modified: Tue, 19 May 2026 18:54:18 GMT  
		Size: 11.9 MB (11891869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
