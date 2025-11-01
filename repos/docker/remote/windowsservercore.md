## `docker:windowsservercore`

```console
$ docker pull docker@sha256:f101911679ef62fe42bc64562750f964510d11e0eda014e22d94fb40030a7921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `docker:windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:871e69554bf56df735f248121de1e93ebd817d84b0aac1a8be0b35cc0f4ed889
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3287397357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0debdf3c164797188654d94b3b856fe4f5ffccf4697d46b66b8165325b45b5dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 31 Oct 2025 23:59:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Oct 2025 23:59:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 31 Oct 2025 23:59:43 GMT
ENV DOCKER_VERSION=28.5.1
# Fri, 31 Oct 2025 23:59:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Fri, 31 Oct 2025 23:59:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 31 Oct 2025 23:59:58 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Fri, 31 Oct 2025 23:59:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Fri, 31 Oct 2025 23:59:59 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Sat, 01 Nov 2025 00:00:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 01 Nov 2025 00:00:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Sat, 01 Nov 2025 00:00:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Sat, 01 Nov 2025 00:00:11 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Sat, 01 Nov 2025 00:00:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc526edf0002209c81ff3c5d6fb622cc6e858c2254f238c4972d2b726b00754b`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe04abbe3ef736ccb6492d759b61d4bcb045526d66ecc60c6bb655bff2c247c8`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 385.8 KB (385836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676d5ebdb28b29ee20caa6ce4769980bea6e67f4c707371a4a9cd2e88daf4f4`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e860b3de84cb81ca7ec484c9e36ff7cfaf3530ed5a8ab762fec932cfaeed30`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d511b2cd6a7b4283ce10b94aa5e7411a6c14ea531e6df2f23bf24cba302d9f04`  
		Last Modified: Sat, 01 Nov 2025 00:18:05 GMT  
		Size: 20.8 MB (20792620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423cfb084830ceda4d96169fefcfb945fb9f135a19646f53ea4bafacd2534ae`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6dd50c2a2a14e253157e4b93785f9b08504f2668e272f6d67211d424141c3d`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec07de3a2084c08d6dad88c7ae76475ee8c79d4f0452c594cc54b9b63e5a692`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d2367a664de75a0a0e8661070ec6df6d1fb9904d6c0cca4a5482907a4648c2`  
		Last Modified: Sat, 01 Nov 2025 00:18:07 GMT  
		Size: 23.2 MB (23173729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a748831fa362f544d5abbdd503de87258aba945cd6ddcc65cea9cba5af3abf3a`  
		Last Modified: Sat, 01 Nov 2025 00:18:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce27bde16d8f4317b3f45906510eaa53273b6efd4cac1c2c00d5ab292817177`  
		Last Modified: Sat, 01 Nov 2025 00:18:05 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40efd1f5e8a6b41239066da4d8dd2e89ba6ca367d9dd39a11500091df5af0d4a`  
		Last Modified: Sat, 01 Nov 2025 00:18:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d54da9134adf84111849d3e96556e0f6462fdf1aa1d7211382280d93ff5909`  
		Last Modified: Sat, 01 Nov 2025 00:18:08 GMT  
		Size: 22.7 MB (22686372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:e43c890001f2d513b7371d576fbad3171a42b38faa0662fec0e461ef90c54819
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1644338394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee163f65b7eacd1f969349f4b32835a6d8395e33fe5b3360e9fa839ea7bc853`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Sat, 01 Nov 2025 00:00:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 01 Nov 2025 00:01:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 01 Nov 2025 00:01:06 GMT
ENV DOCKER_VERSION=28.5.1
# Sat, 01 Nov 2025 00:01:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Sat, 01 Nov 2025 00:01:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 01 Nov 2025 00:01:31 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Sat, 01 Nov 2025 00:01:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Sat, 01 Nov 2025 00:01:34 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Sat, 01 Nov 2025 00:02:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 01 Nov 2025 00:02:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Sat, 01 Nov 2025 00:02:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Sat, 01 Nov 2025 00:02:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Sat, 01 Nov 2025 00:02:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cc5eeeb72e129272dfca31d07a512cf901707d7446bd1b292b96b040ab8787`  
		Last Modified: Sat, 01 Nov 2025 00:14:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770c2fb5bce2e932f2ec5e30b01a7aa868f231b36adbf17738f7dce086dfed46`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 510.8 KB (510820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b08fc4b24b5fe13129b528a695dbdd1b3971c4e1a77cbbc7c57662dd69e85c`  
		Last Modified: Sat, 01 Nov 2025 00:14:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7643434ca98bf15b6e614fde9b54bb983600450013015882463d7b8622865f42`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0230600e13e81127a504d8af9bea02f38319bfc6d68d16189615cbeaea34aa`  
		Last Modified: Sat, 01 Nov 2025 00:14:29 GMT  
		Size: 20.8 MB (20781165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a30a2d0f710ad87b5149bf3b271a776e1ff8ef3201a3316f1fcc96da287f261`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5b01c38ec1e3ba1915da51be0552f7ca4cf4f84e2803ba2e154b68171fb764`  
		Last Modified: Sat, 01 Nov 2025 00:14:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4404a557f2c4156b01f700e90cb97be9a6f0e926ae399ecaf9ff0a001562ca`  
		Last Modified: Sat, 01 Nov 2025 00:14:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ddc0df34aaf874a200bff0d905a909ede57d03c682d8ca08da019952373645`  
		Last Modified: Sat, 01 Nov 2025 00:14:28 GMT  
		Size: 23.2 MB (23163655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4267760ce787b841a05c316b35f91e95bd9e69994373a1dbb323743246cc690a`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2c1a000e617ff07bb472c8870dee371438daa6ad5fe7e29060aacd83abd5e4`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327f32ebe61d0026b8eb1e20d9257e92c4575b500afc147b3f18cbcff8404715`  
		Last Modified: Sat, 01 Nov 2025 00:14:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05169ad8cbc026633c054f283872cc71d9224e4af266ebbf6535a9fe766a7436`  
		Last Modified: Sat, 01 Nov 2025 00:14:29 GMT  
		Size: 22.7 MB (22677991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
