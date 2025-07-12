## `docker:windowsservercore`

```console
$ docker pull docker@sha256:8af71f9bf2d9299f329b29664b8b03bc103d1ccfa95b6aa17e9ac2cc813b3f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
