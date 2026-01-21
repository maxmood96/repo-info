## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:e5be8819c33c02450ae1cb0ffc732f43adce21efbf8bc516c2d83ad28ab7f609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:011b8de53ecb70fa60f226045aca2c69332bb6ee94d021bb9d3fcc085384a0d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1550967984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6dccad077a318174c56c30ebe3c491c307ecc1db3239e2cd5c399177b281ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 23:27:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 23:27:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Jan 2026 23:27:59 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:28:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Fri, 16 Jan 2026 23:28:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:10 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 16 Jan 2026 23:28:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Fri, 16 Jan 2026 23:28:21 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Fri, 16 Jan 2026 23:28:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf85b52279cbf5f434afc4ab079f83bda3ef50d3486fc74a30c20f552694d85f`  
		Last Modified: Fri, 16 Jan 2026 23:28:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93445caeafc2bddea797a95857da92e939124df4d54c185f80f39445e80c0b94`  
		Last Modified: Fri, 16 Jan 2026 23:34:04 GMT  
		Size: 377.1 KB (377114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e299452bcfd7aca11225e6700bf13ba1fb4bcb19e176b8a1a14f554377c7dd2`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053285375a511f9c5e62aad814a3035f4e232806d8993ce9390e35ea7c757b1`  
		Last Modified: Fri, 16 Jan 2026 23:34:04 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc97dec1a7c7fd01f0954f1b05bf600bd724c454ef5a252543bc69fd4fd00b`  
		Last Modified: Fri, 16 Jan 2026 23:34:05 GMT  
		Size: 19.4 MB (19432334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8f925ec92367d9f26dcaaf379beed54c2f51aa96dedc2c1426ee427cd71831`  
		Last Modified: Fri, 16 Jan 2026 23:34:04 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5376a23cd36fd59eb5251f2151e83a0e1a7a67013ba2b5899fba9a796e16092`  
		Last Modified: Fri, 16 Jan 2026 23:34:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c61331a4364799d750587d61e8cce8abf465f33de033951aefcaf07321e77d`  
		Last Modified: Fri, 16 Jan 2026 23:34:04 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b78cf75f88295cbd8090b41c814f0df5e0a6951e496caff112c42de8eac459`  
		Last Modified: Fri, 16 Jan 2026 23:34:07 GMT  
		Size: 23.9 MB (23929994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671ff8ed0c7f11b6caaf11da12b447a4a63e27b1711ecb4078f8007f675be90f`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48250282c43183796eda8334f28230b90a9fac97a683cc4c7b9a49373dcf154e`  
		Last Modified: Fri, 16 Jan 2026 23:34:04 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07517cc4d488302c8930b5fac70a5e65f24ec3cf9a28ead9ab5dff5b3d276f0`  
		Last Modified: Fri, 16 Jan 2026 23:34:04 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4401644c9320335d7ccbf201067db845ccd52bb0dd1091a086309a20504d55`  
		Last Modified: Fri, 16 Jan 2026 23:34:05 GMT  
		Size: 11.5 MB (11456516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:27574c8077e47eae8b561adeac8e2136d1c27bb97bfb370868963f775372c3ac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1890962783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fac75bb46939eff0674007ab202879fd5c512d38bc3477a4ce536005f69de5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Sat, 17 Jan 2026 00:31:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Jan 2026 00:31:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 17 Jan 2026 00:31:37 GMT
ENV DOCKER_VERSION=29.1.5
# Sat, 17 Jan 2026 00:31:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Sat, 17 Jan 2026 00:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:31:55 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Sat, 17 Jan 2026 00:31:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Sat, 17 Jan 2026 00:31:57 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Sat, 17 Jan 2026 00:32:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:32:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Sat, 17 Jan 2026 00:32:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Sat, 17 Jan 2026 00:32:15 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Sat, 17 Jan 2026 00:32:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c78b49395f890e706d473e38c35368e19c6b35bb262c64ca03e023a301e2a6`  
		Last Modified: Sat, 17 Jan 2026 00:42:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ca2adb184b097e41d61db1c4e93f50645315b61438a439b40c1900f125996`  
		Last Modified: Sat, 17 Jan 2026 00:42:53 GMT  
		Size: 501.7 KB (501717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24467fa2d0304efe337e545989ba3cd2e46d51af14ad0b64773f789d3afbeec7`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c5802fad231b2fb1a2c83745d11231a54367bf5f857c22dd7e6435fad68712`  
		Last Modified: Sat, 17 Jan 2026 00:42:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e8f5908d5455b3264f322cb1a1cc727a24fd8b6f17df307574c2561b3e0f90`  
		Last Modified: Sat, 17 Jan 2026 00:32:36 GMT  
		Size: 19.4 MB (19418332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356fa589200fb90532adf9bf598defe12f34d1730f728a493cc1f47019d2dc46`  
		Last Modified: Sat, 17 Jan 2026 00:42:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bca3e0930ba28041675051a18961927142d24d6613f43643112d084fe2ea54`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f85ec7305def0a28b34b0dc0d85d34383426f6ec7852bbb5f37a8505debe2c`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860fb2aeaaed18a9b4d34daff9ddd454eecfc15f6c9788e79c3012cfc58e11a0`  
		Last Modified: Sat, 17 Jan 2026 00:32:37 GMT  
		Size: 23.9 MB (23926291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123dcce148cf36dc3fef9dcac9bc0744e708d97e50efaac5ce4d19cd88c4643a`  
		Last Modified: Sat, 17 Jan 2026 00:42:53 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac82bd7e1e254f2f86462290e0b6f665a884852c8aa1955b982a51ba89d28a65`  
		Last Modified: Sat, 17 Jan 2026 00:42:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11280c48513ddcab1b722f8667f5032899f18af35a191af81071ac5cdb6914`  
		Last Modified: Sat, 17 Jan 2026 00:42:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3022a6d86f2499b629eedda0a7d2f272c52085b6ba6ea64307eb525200beeaa8`  
		Last Modified: Sat, 17 Jan 2026 00:42:54 GMT  
		Size: 11.4 MB (11445469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
