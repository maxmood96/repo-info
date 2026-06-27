## `docker:windowsservercore`

```console
$ docker pull docker@sha256:b17cd5aabf4729820527b6cb3a03aadcb67f50f3928a58d47da5380d1115c9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:9085800e73a7f69e3cf7879c3f20529b424e27dfd7e97bf056fbf93df5b97746
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335638438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4594b1030757f6ae95518073886ca762bfe183e5e9fcc92e298a386aa981c8e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 26 Jun 2026 23:45:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jun 2026 23:46:15 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 26 Jun 2026 23:46:16 GMT
ENV DOCKER_VERSION=29.6.1
# Fri, 26 Jun 2026 23:46:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.1.zip
# Fri, 26 Jun 2026 23:46:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 26 Jun 2026 23:46:33 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 26 Jun 2026 23:46:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 26 Jun 2026 23:46:34 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 26 Jun 2026 23:46:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 26 Jun 2026 23:46:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.2.0
# Fri, 26 Jun 2026 23:46:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-windows-x86_64.exe
# Fri, 26 Jun 2026 23:46:45 GMT
ENV DOCKER_COMPOSE_SHA256=90c81af6cd12227d84665b01e14a89b07920c42d6d04e8f6f391a415f7a8d6a4
# Fri, 26 Jun 2026 23:46:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6b5903c4b4a3a0205f3676e6c632b83872f2644f8eb5491fa2d95c5cecb5e4`  
		Last Modified: Fri, 26 Jun 2026 23:47:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68eae4cb37d4985f9327898154b7ffd4383eb2aa15c51de4f3855e4cd90518a7`  
		Last Modified: Fri, 26 Jun 2026 23:47:01 GMT  
		Size: 383.3 KB (383253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f77bf39d614818de9d5dc763348af9ac518045925ba988ce6a273f7562fc04a`  
		Last Modified: Fri, 26 Jun 2026 23:47:01 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0198fad1e60ebba9d64a06f8f780470706f2ad18cc074af5bef3a15a2400ea`  
		Last Modified: Fri, 26 Jun 2026 23:47:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14ef2cfc2477aa7d09939cf14f8e3c3544e8703c5116ba47c5834e45e37ca44`  
		Last Modified: Fri, 26 Jun 2026 23:47:03 GMT  
		Size: 20.1 MB (20141247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8be55e5959ab541412df71eff77b27b1aac2ed29c44d060fc7201d58bd00cb3`  
		Last Modified: Fri, 26 Jun 2026 23:46:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0afff28c8b7f5180c2fd27b824ab614cd91a221fc81a7418c39a2dd651f8714`  
		Last Modified: Fri, 26 Jun 2026 23:46:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57dedc378d4e25af8b0b8f68ce158d40dfafb1010851dbb6c5662e5737a0d4`  
		Last Modified: Fri, 26 Jun 2026 23:46:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023e1a4c527bc482017b351e49ff4c8d187a992a2d1c16bbf0e0a2d2136418c0`  
		Last Modified: Fri, 26 Jun 2026 23:47:01 GMT  
		Size: 24.0 MB (23954077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cb616ec6d06d1385988342e4dccd48e55c9b95058ca44b2d5c368db4f55be4`  
		Last Modified: Fri, 26 Jun 2026 23:46:57 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ced32e16a3333b95b101a1ead02c06b7eba747038493699e15d26cc5f5d1917`  
		Last Modified: Fri, 26 Jun 2026 23:46:57 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a4f16fd6baf1510fdcea9a5b866f0e2c0f29b1b521ce5fb82829404bbcf09b`  
		Last Modified: Fri, 26 Jun 2026 23:46:57 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873f2ad92d80f094c7382b48f0031fa9cfbdee8d7bbe3dc107f50ff4de5fb2`  
		Last Modified: Fri, 26 Jun 2026 23:46:59 GMT  
		Size: 12.0 MB (12005268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:4ad6a595363e7073ec00678cb8c08e8ece70ff44f6b9275a4a4856a74d3112ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188675542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb7aeb4e95dce664e25ad9144763419e48774952b585c30390cf756f8092a5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Sat, 27 Jun 2026 00:12:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 27 Jun 2026 00:13:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 27 Jun 2026 00:13:18 GMT
ENV DOCKER_VERSION=29.6.1
# Sat, 27 Jun 2026 00:13:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.1.zip
# Sat, 27 Jun 2026 00:13:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 27 Jun 2026 00:13:44 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Sat, 27 Jun 2026 00:13:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Sat, 27 Jun 2026 00:13:46 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Sat, 27 Jun 2026 00:14:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 27 Jun 2026 00:14:12 GMT
ENV DOCKER_COMPOSE_VERSION=5.2.0
# Sat, 27 Jun 2026 00:14:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-windows-x86_64.exe
# Sat, 27 Jun 2026 00:14:13 GMT
ENV DOCKER_COMPOSE_SHA256=90c81af6cd12227d84665b01e14a89b07920c42d6d04e8f6f391a415f7a8d6a4
# Sat, 27 Jun 2026 00:14:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9458cacd40a444e5887d754b7ee315f8f9a5e05962891a731e37b151bc24bf`  
		Last Modified: Sat, 27 Jun 2026 00:14:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b16d020f489a6f63ae248efd4bc6f3787bb5376721770e93738f4c5cfd4b439`  
		Last Modified: Sat, 27 Jun 2026 00:14:30 GMT  
		Size: 500.5 KB (500512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0005d1f8940e4f28ce2bcacb85ec59275e97f23b9f72bb5404726fce1afaa7ba`  
		Last Modified: Sat, 27 Jun 2026 00:14:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af25efad2c9fbe3a72add1584aecc59a1d0a09ade8ae48b649c334a2dde56c0b`  
		Last Modified: Sat, 27 Jun 2026 00:14:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b8f796b8efb2b043f7a8ef10d6990905592aa1d10c1e5b3edbbd98dc6158a6`  
		Last Modified: Sat, 27 Jun 2026 00:14:32 GMT  
		Size: 20.1 MB (20116806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6db0cf4b52aa2a1d58e0bb6bfb2ed87263efb90ca40c091ae17b2d6d22e789`  
		Last Modified: Sat, 27 Jun 2026 00:14:28 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce51af1e460c2432fc80f82413c1431d0706b15fb6dd0be1916d46088ee06bd5`  
		Last Modified: Sat, 27 Jun 2026 00:14:28 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b0a69ca356528fdd1bee8611913e40cd7dc72c6e0d091c0435bc54d41968f1`  
		Last Modified: Sat, 27 Jun 2026 00:14:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7165b8ec1b4d37840933a9aafb84e381cb91e7a3033ebac76fa705980072f8`  
		Last Modified: Sat, 27 Jun 2026 00:14:33 GMT  
		Size: 23.9 MB (23938178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e2abb337f910a51016d12f6501e8c4517c96029f32f9a776dd93c11c65a99a`  
		Last Modified: Sat, 27 Jun 2026 00:14:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40a57737c81a4570db699fa2d227e62a2195847de223f49f44565787ac11597`  
		Last Modified: Sat, 27 Jun 2026 00:14:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66ad9b1abeffb2bdc211ff137be083e913425030d1098b96a5ac7478708f381`  
		Last Modified: Sat, 27 Jun 2026 00:14:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726c6620e58061f13800c414651277c2266c9d482c84a268b0dc0beeff6b7d6c`  
		Last Modified: Sat, 27 Jun 2026 00:14:28 GMT  
		Size: 12.0 MB (11982845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
