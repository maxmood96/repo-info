## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:8327bf634255e9194fe652fd088888acc89ead76e3a54d69e3f00f9869e9fe77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull docker@sha256:92484f739bd6ff5fc55ccb56ad11aa071a56298620d03bd9cb8d9ab02bfd2251
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1965791850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e253c0c4d496fe1d315df035da87380e558f28a1a3d3528846118771a66d393`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Fri, 16 Feb 2024 19:59:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Feb 2024 20:00:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Feb 2024 20:00:10 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 16 Feb 2024 20:00:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Fri, 16 Feb 2024 20:00:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:00:21 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 16 Feb 2024 20:00:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 16 Feb 2024 20:00:22 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 16 Feb 2024 20:00:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:00:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Fri, 16 Feb 2024 20:00:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-windows-x86_64.exe
# Fri, 16 Feb 2024 20:00:32 GMT
ENV DOCKER_COMPOSE_SHA256=7a25ec49a53320fbe218c59ac7aafb05440725894322d396d4b353ad198b9dff
# Fri, 16 Feb 2024 20:00:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f1d9b8108e7b21446783f2fe2e43f67b6cf0da6f19aae1fb401ae7ac33c95e`  
		Last Modified: Fri, 16 Feb 2024 20:00:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7cf809e4171818e5d454a237103349c59caa89177c170f5db2acf6015155a2`  
		Last Modified: Fri, 16 Feb 2024 20:00:46 GMT  
		Size: 501.0 KB (501048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639204ad8eaa39d45914b46a2f06e221364fa6e4268d7c1abc39f9aa56e0aed6`  
		Last Modified: Fri, 16 Feb 2024 20:00:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8405a7ca182adb17907795cf6f6a206e4ba57a1db2e3e8fb2edcb21767eb78b9`  
		Last Modified: Fri, 16 Feb 2024 20:00:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1a9ddc2e943e369aca6c3330341515e0b2251802502ff849d141edbe7a7844`  
		Last Modified: Fri, 16 Feb 2024 20:00:47 GMT  
		Size: 17.5 MB (17540939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df864e6ead0e235db87283ebeecff45291db6962026f16045164dd19611061a1`  
		Last Modified: Fri, 16 Feb 2024 20:00:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53f6e2d0ac91464ed9b5d72d673e8022c87b2dbc2e99632d4d413c816c9512d`  
		Last Modified: Fri, 16 Feb 2024 20:00:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9371b25c19626d7b4fc22c24a15da98bfda8a1e7dc07a960c4f5af27ab1a0d`  
		Last Modified: Fri, 16 Feb 2024 20:00:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b51db43017a32a3cc3792530ef815ed0852cef50a3299f99882e2bd26bc84f`  
		Last Modified: Fri, 16 Feb 2024 20:00:46 GMT  
		Size: 18.0 MB (18019530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b9567a257dae06703ad887c9c6e2d1d2328621011a7f14bef5d3fc298e7500`  
		Last Modified: Fri, 16 Feb 2024 20:00:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad75b2409b61a0e398ff3ada9a449eb75c109b19af402216f0614e39a540b613`  
		Last Modified: Fri, 16 Feb 2024 20:00:43 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c98fbd41f6c243a27e39b2b1f38331ac2244d4245fe72258c4f8c4cdaa67b`  
		Last Modified: Fri, 16 Feb 2024 20:00:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe5ec6cb98ba8840bb52b795e11da81481489678777cdb94335108e6a547c7a`  
		Last Modified: Fri, 16 Feb 2024 20:00:45 GMT  
		Size: 19.1 MB (19064606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull docker@sha256:8ff9de389af5e773516475dcd2583452f7e89f6a76ff899463210df31b8ff8c2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2135575857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a658ed1488dc4d59b45888f08862d6167fb176c9963d503091bf0ce1c158f906`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Fri, 16 Feb 2024 20:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Feb 2024 20:03:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Feb 2024 20:03:04 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 16 Feb 2024 20:03:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Fri, 16 Feb 2024 20:03:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:03:32 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 16 Feb 2024 20:03:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 16 Feb 2024 20:03:33 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 16 Feb 2024 20:03:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:03:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Fri, 16 Feb 2024 20:03:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-windows-x86_64.exe
# Fri, 16 Feb 2024 20:03:58 GMT
ENV DOCKER_COMPOSE_SHA256=7a25ec49a53320fbe218c59ac7aafb05440725894322d396d4b353ad198b9dff
# Fri, 16 Feb 2024 20:04:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a86a46b132f1ccb0e1450a2b9a6ffdaaf7949845204face802b39bef498becb`  
		Last Modified: Fri, 16 Feb 2024 20:04:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7576b792b0e34ac9d734d6dcef3e36add9a155db749867bf135f651cd4107`  
		Last Modified: Fri, 16 Feb 2024 20:04:31 GMT  
		Size: 494.2 KB (494231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d374025bd341f4730bd8e81462e2395707790cd2832eab455b55dbbcb1718b`  
		Last Modified: Fri, 16 Feb 2024 20:04:31 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d415158a2a5b4cf07c41332268bbf762d1350558f46b1267667c6750db8fb21`  
		Last Modified: Fri, 16 Feb 2024 20:04:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe1bb960a4e9c575f3a0133762244d9047956e214c2b7eac5fbe0fa5a7dae57`  
		Last Modified: Fri, 16 Feb 2024 20:04:32 GMT  
		Size: 17.5 MB (17540243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9fd09dd0372083d869cf984b8fe5cc869befcb24635f28af21eec4edcd54be`  
		Last Modified: Fri, 16 Feb 2024 20:04:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61a7f7fa7d6b5a8b68fe45c8bb15bb05facf811bfd4f0236f96c73b7803e8bf`  
		Last Modified: Fri, 16 Feb 2024 20:04:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d9137909dafa0d9e45b1ed987409eb3a2825b9dbef57e7ee6e86a5c1e92f57`  
		Last Modified: Fri, 16 Feb 2024 20:04:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a5f8e63201fdda90f0a5d97b3067c747b10cf13756606224317387591eaeaa`  
		Last Modified: Fri, 16 Feb 2024 20:04:29 GMT  
		Size: 18.0 MB (18020779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dd393936598226bc37c35eb538ea3da0e97216caf1e1661ab36944733b917d`  
		Last Modified: Fri, 16 Feb 2024 20:04:26 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64540f6053a72b4c74317d3c0b1489307e8e14b583407d491b3c61fb2036ac4c`  
		Last Modified: Fri, 16 Feb 2024 20:04:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebc28d895e982aa403379ddae71b07ad067aef53f4944b56d432654310c05c7`  
		Last Modified: Fri, 16 Feb 2024 20:04:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf481109469b101cb01f304d2aa0850d5f47a6ff71c6ed564c0cfe2153a77d6b`  
		Last Modified: Fri, 16 Feb 2024 20:04:29 GMT  
		Size: 19.1 MB (19060152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
