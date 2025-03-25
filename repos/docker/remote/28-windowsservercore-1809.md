## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:c8052ef5f90cd2fa3c44394fec8378a887db5d87c66f6d5af683b3082f4f3658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
