## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:51cd4d88a987b70d83a6b0c7232740ab955c77d0abd8625f40daa49ff35f7f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:03fb3a913dc4f1465332f09a30d64bd2d1593c087d8076f192958cc0e78ead73
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565629198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dba4f80b10e0ffc054202c373d41b17ed08299798d42223f423c37a30983daa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 01 Sep 2025 22:39:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Sep 2025 22:39:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 01 Sep 2025 22:39:25 GMT
ENV DOCKER_VERSION=28.3.3
# Mon, 01 Sep 2025 22:39:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Mon, 01 Sep 2025 22:39:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 01 Sep 2025 22:39:36 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Mon, 01 Sep 2025 22:39:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.windows-amd64.exe
# Mon, 01 Sep 2025 22:39:37 GMT
ENV DOCKER_BUILDX_SHA256=1e89de288c9897990220d2ee695b50956d42a3a0792c0b070e9fee7711b9f896
# Mon, 01 Sep 2025 22:39:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 01 Sep 2025 22:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Mon, 01 Sep 2025 22:39:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Mon, 01 Sep 2025 22:39:49 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Mon, 01 Sep 2025 22:39:58 GMT
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
	-	`sha256:ce467fb2ca593283d716259d94188ee1c7db07b5d251b522ff0e1919dbc8adaa`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8e7b9b4c09027a9f9e7099ee679070906a44e8c98327b16f182a19fade0c24`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 380.9 KB (380911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6bdb99e4ffa1186246d1ec272e9a12b7338929a91e887b763d282dd9c24f8`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941f54a3ed76421817cc8c0063d31aca441f926224430a6f74520e0995ee143f`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0a0098b0bbdaad6162f85f0a2e9adf14fe89aed4714c18dc36e9beeddad9f`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 20.9 MB (20859849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c35ede22d20d1da237e03fbf6806721d65c33eb0681dbccc1965c7c1917d4e`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9032419640af747a06d5d26fbd513025681aac754eff8dce56025265729020da`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2995d785b536a0e21ee15143622b4d651abc8f74e8f14d78228c004232b022de`  
		Last Modified: Mon, 01 Sep 2025 22:43:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab515808fb28c0db212d7836f2d2ceb248a67c98f56df6ec462a00af9ae1772`  
		Last Modified: Mon, 01 Sep 2025 22:43:45 GMT  
		Size: 23.1 MB (23130307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46559d189a20d0a0caef1c4fbe4282a81a22a684a9b3f020a0c8c495a98711b`  
		Last Modified: Mon, 01 Sep 2025 22:43:37 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff97af7cbfef4ee2f69bf6f5b414fa5f316fb7ee9b9d08eb5676f596a9424ac`  
		Last Modified: Mon, 01 Sep 2025 22:43:37 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9eebf1fc56984a1d0592fd38a8a7edae56836d5e88a23c3eb04f945470762`  
		Last Modified: Mon, 01 Sep 2025 22:43:37 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019f501dd43a6c2ca290b616ef72b9cc599efb4623a276a5752300ae5588d2a2`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 22.4 MB (22415690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
