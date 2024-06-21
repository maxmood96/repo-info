## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:13ab6619f28919ffae14410dfc46ef305ae340568c1f7b3d020c637382efdb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `docker:rc-windowsservercore` - windows version 10.0.20348.2527; amd64

```console
$ docker pull docker@sha256:d25ebcd07dbe2c342347188859e6b45cf45ed6df1bb000c6f565c5940f5302fc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2176466286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8b92f74ba484c5b1e6f1388c445d446d554e082b4a4c6b76f6a01a9bb36e3c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Fri, 21 Jun 2024 00:08:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jun 2024 00:08:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jun 2024 00:08:23 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Fri, 21 Jun 2024 00:08:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.0.0-rc.2.zip
# Fri, 21 Jun 2024 00:08:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 00:08:34 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 21 Jun 2024 00:08:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Fri, 21 Jun 2024 00:08:35 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Fri, 21 Jun 2024 00:08:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 00:08:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Fri, 21 Jun 2024 00:08:43 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-windows-x86_64.exe
# Fri, 21 Jun 2024 00:08:44 GMT
ENV DOCKER_COMPOSE_SHA256=b9878421deeff63bb4685a0ee502fc737429123f68ee40de326cdc9fab800c1d
# Fri, 21 Jun 2024 00:08:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a544feeb9bee08a7557e72afbc165682668147ff606cb97ccd3218eb14265b`  
		Last Modified: Fri, 21 Jun 2024 00:08:57 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805d2e01271d81df16e760dc29229f7c3746ab5bed1853fa6f37879f5ac39e7d`  
		Last Modified: Fri, 21 Jun 2024 00:08:57 GMT  
		Size: 357.1 KB (357079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9405370bbe25eb2eff9e2347e9740e9a6d436b63bea59a129104df3bb28e237b`  
		Last Modified: Fri, 21 Jun 2024 00:08:56 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff89ba88a1b8343ffc3b707c5fdfa0c785f0be69c4e913bb65d0d41c5b6fc90e`  
		Last Modified: Fri, 21 Jun 2024 00:08:56 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b79f569b154905432166013fabfac38b7397c780fc325a1a7d730019d784b9`  
		Last Modified: Fri, 21 Jun 2024 00:08:58 GMT  
		Size: 19.3 MB (19266375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3096853cfcd3c5d7e9545238ae49915973a4f568661868d30a6301e456075f35`  
		Last Modified: Fri, 21 Jun 2024 00:08:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e22ac3c863c11720a620a8c5507967af3aad3ce663c7ff563a0a034c9d81d9`  
		Last Modified: Fri, 21 Jun 2024 00:08:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0911d454863cd88bf44b381163171c4139b60d0ff618278a24ce7deaa4d2e882`  
		Last Modified: Fri, 21 Jun 2024 00:08:55 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88b950592d0fa051b214ddfb3737acc64b31685d1d2f3c0755a146dcbc16508`  
		Last Modified: Fri, 21 Jun 2024 00:08:56 GMT  
		Size: 19.0 MB (19021835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f701e6b8e9d3ce522ad56c0e0b5f91b2267edbb9fd43fb6a98e9ca2f095a86e`  
		Last Modified: Fri, 21 Jun 2024 00:08:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298d298f1f680c0c469cebf1938db15191ac05429d8065237d61ce97f2960e7d`  
		Last Modified: Fri, 21 Jun 2024 00:08:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3fc140f5b6363b4873e74b363daf7b44c1542ac1a20b728dcf4537626897f4`  
		Last Modified: Fri, 21 Jun 2024 00:08:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d60414e171ed680119c1b21c06b30e75de68ada0d128cb40d8bdda6b91b10`  
		Last Modified: Fri, 21 Jun 2024 00:08:57 GMT  
		Size: 19.6 MB (19630711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:5a7a9b38da7134184913c6e58682d6f3bb04104b360a146abd7c53566d4f4f04
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279122882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f85641609392e98e23901261ccd2fd530d8dc2e890a4b9c2d31eef9e418b8a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Fri, 21 Jun 2024 00:11:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jun 2024 00:12:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jun 2024 00:12:51 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Fri, 21 Jun 2024 00:12:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.0.0-rc.2.zip
# Fri, 21 Jun 2024 00:13:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 00:13:15 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 21 Jun 2024 00:13:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Fri, 21 Jun 2024 00:13:17 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Fri, 21 Jun 2024 00:13:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 00:13:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Fri, 21 Jun 2024 00:13:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-windows-x86_64.exe
# Fri, 21 Jun 2024 00:13:41 GMT
ENV DOCKER_COMPOSE_SHA256=b9878421deeff63bb4685a0ee502fc737429123f68ee40de326cdc9fab800c1d
# Fri, 21 Jun 2024 00:14:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d204cf1feed91b8d497a7dce52e38345f64c40476a87c78b8dae6058ed63899`  
		Last Modified: Fri, 21 Jun 2024 00:14:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947ffdf2ba0c4c5d27cbe870bc4e509f13bc72d5f22c5b2196b5c7fc95839f02`  
		Last Modified: Fri, 21 Jun 2024 00:14:06 GMT  
		Size: 494.4 KB (494421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324dfd02da86bcb5628b11086d5da0cc4f02f94b0b2119f2982024fc76875eba`  
		Last Modified: Fri, 21 Jun 2024 00:14:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22693b71e1228fe1e0a3b96b2d8d4b3427f5c8447ca70cea47b7a10b70768ec`  
		Last Modified: Fri, 21 Jun 2024 00:14:05 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c911b2b5a225ac5520ef58dae02cb3f575c931a7072b410574fa2b358740b`  
		Last Modified: Fri, 21 Jun 2024 00:14:06 GMT  
		Size: 19.3 MB (19273603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e647d949d12637734c3503038a4bd805001752e3074591f00004c165df8a5e`  
		Last Modified: Fri, 21 Jun 2024 00:14:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca60b55afde455d64c15a542474cdce6ed9b0c12b87b20ae3c3869e7ec2e8c5`  
		Last Modified: Fri, 21 Jun 2024 00:14:04 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6803b2314c285f9cb081cce4ea8a0782e0ff41c4ce8268d1afdfdea4ffe3bd2`  
		Last Modified: Fri, 21 Jun 2024 00:14:04 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a11b834e470fa5154d48b6e8c0e634de6a282fab7a610f22d117942e6a3bd9`  
		Last Modified: Fri, 21 Jun 2024 00:14:05 GMT  
		Size: 19.0 MB (19030204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4797c5a4b196bf9f107b718927490d5dbc8f458b3fc05bfbb6537e6bce202ad`  
		Last Modified: Fri, 21 Jun 2024 00:14:03 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59fd060482c1eb41e8f8ab1003d373397753f8b2455ba99124d8b9499a9ac9f`  
		Last Modified: Fri, 21 Jun 2024 00:14:03 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df8a2249fec2940cf8d52079033b9b544e12263384a314e9dc839db780951d8`  
		Last Modified: Fri, 21 Jun 2024 00:14:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7edebc0c5dddd2f52a90594e54fe6a60eec90a61bd8df01cc0f544e76a24e`  
		Last Modified: Fri, 21 Jun 2024 00:14:05 GMT  
		Size: 19.6 MB (19631752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
