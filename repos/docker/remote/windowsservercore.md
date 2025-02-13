## `docker:windowsservercore`

```console
$ docker pull docker@sha256:b6f8b0d57df4a2696419a5762e577d335b8045344e3955e8f4dbe161e18af19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Mon, 27 Jan 2025 00:02:38 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Mon, 27 Jan 2025 00:02:37 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Mon, 27 Jan 2025 00:02:50 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Mon, 27 Jan 2025 00:02:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Mon, 27 Jan 2025 00:02:47 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Mon, 27 Jan 2025 00:02:50 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Mon, 27 Jan 2025 00:03:03 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Mon, 27 Jan 2025 00:02:59 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Mon, 27 Jan 2025 00:02:55 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Mon, 27 Jan 2025 00:02:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Mon, 27 Jan 2025 00:03:04 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 21:54:27 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Mon, 27 Jan 2025 00:02:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Mon, 27 Jan 2025 00:02:38 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Mon, 27 Jan 2025 00:02:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Mon, 27 Jan 2025 00:02:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Mon, 27 Jan 2025 00:02:42 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Mon, 27 Jan 2025 00:02:45 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Mon, 27 Jan 2025 00:02:44 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Mon, 27 Jan 2025 00:02:44 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Mon, 27 Jan 2025 00:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Mon, 27 Jan 2025 00:02:51 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 20:54:32 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Mon, 27 Jan 2025 00:02:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Mon, 27 Jan 2025 00:02:37 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Mon, 27 Jan 2025 00:02:38 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Mon, 27 Jan 2025 00:02:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Mon, 27 Jan 2025 00:02:42 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Mon, 27 Jan 2025 00:02:40 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Mon, 27 Jan 2025 00:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Mon, 27 Jan 2025 00:02:45 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Mon, 27 Jan 2025 00:02:43 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Mon, 27 Jan 2025 00:02:44 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Mon, 27 Jan 2025 00:02:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Mon, 27 Jan 2025 00:02:50 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
