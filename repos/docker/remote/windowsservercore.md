## `docker:windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
