## `docker:27-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:6375daa31720deeb2664df88c18a79ae88dd189d4f6c00ad908069d4c1a997e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `docker:27-rc-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:0838a923626774e658e06453930a294bb003ace9a4bb9a8549722dddd645fe48
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279030063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e206ec3a3366ba061c37e5e50297fec417138871e808d794f156e0c00ef794dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 22:12:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 22:14:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 22:14:25 GMT
ENV DOCKER_VERSION=27.0.0-rc.1
# Wed, 12 Jun 2024 22:14:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.0.0-rc.1.zip
# Wed, 12 Jun 2024 22:14:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 22:14:50 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 12 Jun 2024 22:14:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.windows-amd64.exe
# Wed, 12 Jun 2024 22:14:51 GMT
ENV DOCKER_BUILDX_SHA256=f9285890c7d0b68ed36a07d4db062bfdc8db2059fa59a812cdbef438cfa3f774
# Wed, 12 Jun 2024 22:15:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 22:15:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 12 Jun 2024 22:15:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 12 Jun 2024 22:15:12 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 12 Jun 2024 22:15:34 GMT
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
	-	`sha256:ba32b87a8b40c409628ccbe9d68324385a66fc65f48389b5745286d5c2c18252`  
		Last Modified: Wed, 12 Jun 2024 22:15:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb6e382caaf7e7793235289ed1cc0c6b4566488567c371d8fa5ef6d68ca67c5`  
		Last Modified: Wed, 12 Jun 2024 22:15:42 GMT  
		Size: 470.5 KB (470460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae6f5145c14b1a657130b4de51f25136427c1f8e9d964cee99f5aba1bbe26e7`  
		Last Modified: Wed, 12 Jun 2024 22:15:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b3c27bd96b24b37e91abce8a178103ef29952f845cf023725824693b4e8bf3`  
		Last Modified: Wed, 12 Jun 2024 22:15:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e4b80e25b79b5ea09ba762c6e4679bc74449437e9118223c6440ec0214c6bb`  
		Last Modified: Wed, 12 Jun 2024 22:15:43 GMT  
		Size: 19.2 MB (19247045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa16812160122498f6abb80dfdc53ef30e93718a15ef086def5c2b52ba2905e4`  
		Last Modified: Wed, 12 Jun 2024 22:15:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd35fe1fcfe4ec6cd32d869b42b79c8ff0ef737661a4402c72566a8bcdf25062`  
		Last Modified: Wed, 12 Jun 2024 22:15:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77800f653ca231a9991dbf47e1b3ba17644dc24f3d73afd1064975798bf73b5f`  
		Last Modified: Wed, 12 Jun 2024 22:15:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cccd26a6295ddb5faefb27525ca6835abb3d11fc950ab57790202142675a6ce`  
		Last Modified: Wed, 12 Jun 2024 22:15:42 GMT  
		Size: 19.0 MB (19006046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f93b440a6a563fc380fc134d2b9d60cdf823d287b8452a551e6a2546824e08`  
		Last Modified: Wed, 12 Jun 2024 22:15:39 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75499d49a5a41280f070608ee74059b5eb30adc0e8684637f0aa67140075cace`  
		Last Modified: Wed, 12 Jun 2024 22:15:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1051afd1bcca00b9cfa012d7be7f9e4f124db5a7b6299fee567c547baf5ac97e`  
		Last Modified: Wed, 12 Jun 2024 22:15:39 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd154e2a94576a5389f1727acc3575c6f56ccfa891e6327786943aa5c9d5506c`  
		Last Modified: Wed, 12 Jun 2024 22:15:42 GMT  
		Size: 19.6 MB (19613596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
