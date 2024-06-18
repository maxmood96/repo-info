## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:35b98d90725a2c3b749c0e95173f730e4768fd2b86ea442046dd327a67df1b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:de1af6b7e17f8bdb679049124d02e59f856ba105744c988e39a55c68c5ac708a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279123662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ed39ff16099cf638ef4043768b197d95bdb10c8a2bab4b89cc74b80ade29cf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Tue, 18 Jun 2024 00:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Jun 2024 00:05:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Jun 2024 00:05:44 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Tue, 18 Jun 2024 00:05:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.0.0-rc.2.zip
# Tue, 18 Jun 2024 00:06:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Jun 2024 00:06:08 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Tue, 18 Jun 2024 00:06:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.windows-amd64.exe
# Tue, 18 Jun 2024 00:06:09 GMT
ENV DOCKER_BUILDX_SHA256=f9285890c7d0b68ed36a07d4db062bfdc8db2059fa59a812cdbef438cfa3f774
# Tue, 18 Jun 2024 00:06:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Jun 2024 00:06:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Tue, 18 Jun 2024 00:06:31 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Tue, 18 Jun 2024 00:06:31 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Tue, 18 Jun 2024 00:06:52 GMT
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
	-	`sha256:57db80eabe1ed1b6b3f727d46a674dbed1b38d98fc310f43378265a210b75bd8`  
		Last Modified: Tue, 18 Jun 2024 00:07:01 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e08a280c9bccb71544ec49c6280074a829af6e2db07ed494b622f93107beca`  
		Last Modified: Tue, 18 Jun 2024 00:07:01 GMT  
		Size: 493.5 KB (493521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153cf6ddd0bf4c08ee5b07fcd8ee448fc96c23355bffc8ab051e7de9d084c962`  
		Last Modified: Tue, 18 Jun 2024 00:07:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cab7929b77bf40bfd727a53da6e30f8dff041615226c8f297f7f35fde68bb0b`  
		Last Modified: Tue, 18 Jun 2024 00:07:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e710f5ccdce38d4ac9e3004365799cbe67f4c63f7ec002d62dd6e126dc0336`  
		Last Modified: Tue, 18 Jun 2024 00:07:02 GMT  
		Size: 19.3 MB (19272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b147aa6ac8a6bb676c93eb2eb18b0450dd4d52b05b3f55fae491d7ea6e85f136`  
		Last Modified: Tue, 18 Jun 2024 00:06:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfbbc4a05a79af54442cc9c4cb1df238ba431fa36d8bc07775fe2c362f4505b`  
		Last Modified: Tue, 18 Jun 2024 00:06:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088a3e90683af7bb664b69130eca820166303766042604713c01362e6ce4d366`  
		Last Modified: Tue, 18 Jun 2024 00:06:58 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb6a389707b79dfef07658d45334afdac6c83eff343dd01951fe14b078b25bc`  
		Last Modified: Tue, 18 Jun 2024 00:06:59 GMT  
		Size: 19.0 MB (19028434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24262655f60205a98da6d433fb26a802b6f9f6974db94c81e2195650b4b32194`  
		Last Modified: Tue, 18 Jun 2024 00:06:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4db36a742079bab5d2257aeed5db8907f6b0b6c533a08ac990ed195c32b7bc6`  
		Last Modified: Tue, 18 Jun 2024 00:06:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9501af9d4edc8ff4b71a6bdd00c1202506e1c649ece58af123e1c12f46ca2e3`  
		Last Modified: Tue, 18 Jun 2024 00:06:56 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c34126905a4befc15d6b9c18ca9581e4302ddaa1b2dcbbcba0ebca44a7b445`  
		Last Modified: Tue, 18 Jun 2024 00:06:59 GMT  
		Size: 19.6 MB (19635956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
