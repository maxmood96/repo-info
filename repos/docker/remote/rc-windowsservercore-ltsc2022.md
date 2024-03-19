## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:410a66149772966c111d7939f68436f7318b5c62a30a7c9e1ed4ccbd986088e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:a52326256add27f50acf0878191a332ce2c963d527ed2f73c1256cafe0dc0346
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013969716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c722f31f137abd0feb486e38ecc25add0c22613e722a3e52d277113a5f8cde`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 18 Mar 2024 23:01:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Mar 2024 23:02:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Mar 2024 23:02:18 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Mon, 18 Mar 2024 23:02:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Mon, 18 Mar 2024 23:02:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 18 Mar 2024 23:02:30 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 18 Mar 2024 23:02:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 18 Mar 2024 23:02:31 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 18 Mar 2024 23:02:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 18 Mar 2024 23:02:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Mon, 18 Mar 2024 23:02:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-windows-x86_64.exe
# Mon, 18 Mar 2024 23:02:41 GMT
ENV DOCKER_COMPOSE_SHA256=27289c82fe3ee64eaa415ae47f028f7c6af6ab347f1af4fde0e0d7d2b4a84dbb
# Mon, 18 Mar 2024 23:02:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce082ec15db8a37b08198cb2e2b11de8aa6507cd17d613e5aafb329e489a766`  
		Last Modified: Mon, 18 Mar 2024 23:02:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af88e66e912d9be54e01c7b5b6d3dcf9a9f8c98386d2f421c59048cb5dc97a3`  
		Last Modified: Mon, 18 Mar 2024 23:02:54 GMT  
		Size: 492.0 KB (491978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b0ab83631ac33bf9b16d5f4b17ed364cc9b465a8b296abc27a624b16746d62`  
		Last Modified: Mon, 18 Mar 2024 23:02:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89d4e83d71d3bcf465d9396e24da783cc9137141fd215402266620b038fe338`  
		Last Modified: Mon, 18 Mar 2024 23:02:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df3cbeb7b5daf5754fb0d4b4cda3de9ab609be6f6df3eed0eeba740919fc2d4`  
		Last Modified: Mon, 18 Mar 2024 23:02:54 GMT  
		Size: 18.1 MB (18095760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754dfc16c010d6e854a6de5f35490c485be79be5f9ce13c809c82c71719ebe94`  
		Last Modified: Mon, 18 Mar 2024 23:02:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67ba15b76915320cc226b1eb71896ff3f56498c940547e424154330fe2a0d39`  
		Last Modified: Mon, 18 Mar 2024 23:02:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c07287f1045e346b3e2c9001e0a48882cbaefc801eee29ef9d6ec4691567485`  
		Last Modified: Mon, 18 Mar 2024 23:02:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db99b09a610be719ae378cac22039f2bad8f614cbae051af722e8375642d686`  
		Last Modified: Mon, 18 Mar 2024 23:02:53 GMT  
		Size: 18.8 MB (18829746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cc02c46f7345dafcd977c32d5d29a84f20b6b9b5b22e9f36df496ee4282ab2`  
		Last Modified: Mon, 18 Mar 2024 23:02:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8aa62041abcea24aa3e7debb6039ea123492a109de1da1169ff3acf5ea69e15`  
		Last Modified: Mon, 18 Mar 2024 23:02:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854cbe4c769ab7777c5883d6de0364ee7b75a5ceba57e7d21818e3088523297a`  
		Last Modified: Mon, 18 Mar 2024 23:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15ee89a1e80a116be9df4842d98f4ad40887ca9d4a8d52455904e5198e4363e`  
		Last Modified: Mon, 18 Mar 2024 23:02:54 GMT  
		Size: 19.1 MB (19081590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
