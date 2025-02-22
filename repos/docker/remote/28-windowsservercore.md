## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:8cbb71e3463881e43b4e46000916a151f195288cba0ad77f0eabef966bc5d438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
