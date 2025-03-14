## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:10534064ac729673b33cbdca95321f226004604f7768fea4db27838ebe3d44ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:538f4999202c7e81b53d6b08e3c57970e153f2b39ac17a41fc1cfb146d960797
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335146546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eda11887160daecb3912a773a2f13fb72352ff56a0562ad2b2f014edb7fbef9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Fri, 14 Mar 2025 20:27:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Mar 2025 20:27:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Mar 2025 20:27:33 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 20:27:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Fri, 14 Mar 2025 20:27:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:27:46 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 20:27:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Fri, 14 Mar 2025 20:27:48 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Fri, 14 Mar 2025 20:27:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:27:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 20:27:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Fri, 14 Mar 2025 20:27:59 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Fri, 14 Mar 2025 20:28:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83bfd3cec0ebe5c646d5735b43ab392607ab6725811e4dd9c8101085c3ab3ef`  
		Last Modified: Fri, 14 Mar 2025 20:28:16 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d483288d5dd71b58e5d2e39986f24e3add8983efe6a4344f8d3da14fc305a`  
		Last Modified: Fri, 14 Mar 2025 20:28:15 GMT  
		Size: 353.8 KB (353804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4e6d225bb6e736cda1f7293493d8b94ae2f4dc09c518455eeccb70382e48e7`  
		Last Modified: Fri, 14 Mar 2025 20:28:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdc60933044b936dcdddb73f9182097bdaaa7972196c25e38b6bfd0f24e549b`  
		Last Modified: Fri, 14 Mar 2025 20:28:14 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c8f449256923700c12fda37d9616e2add2bbff61401ab259cbadaaeeb071e5`  
		Last Modified: Fri, 14 Mar 2025 20:28:15 GMT  
		Size: 19.8 MB (19812922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afc67b968ae48dc367b6f06cad02e565d1eabf6cc403c13b14282176ea39bd2`  
		Last Modified: Fri, 14 Mar 2025 20:28:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17820c7b2f6c9966d8cd748221a321b899635ea378b88301a074474b9fe2a999`  
		Last Modified: Fri, 14 Mar 2025 20:28:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71895d0e38c1b29c95f81698e598e9bfb8feff1aa772410ae1c01b13c308d79`  
		Last Modified: Fri, 14 Mar 2025 20:28:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101409f72d4da5d00ba9032cd3741626d13207f92fa60522af3ccd6041d5275a`  
		Last Modified: Fri, 14 Mar 2025 20:28:16 GMT  
		Size: 22.7 MB (22739166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e89052fe33793fbde299dcbc3130cb0545e9e71d748c173b94d70d04e1dc6`  
		Last Modified: Fri, 14 Mar 2025 20:28:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55431de88dc75aefa8f8aec17bc87c48ebd27a4e417c7ed2c978c16ccf50131f`  
		Last Modified: Fri, 14 Mar 2025 20:28:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b940fd21726a05c3c591d44f8610b4090fe6b744898edd72e85984bbf3d528b2`  
		Last Modified: Fri, 14 Mar 2025 20:28:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bea29af16c9bd9f321318cfbe88d357222fcda3630d99622848479e38ef89f`  
		Last Modified: Fri, 14 Mar 2025 20:28:16 GMT  
		Size: 22.3 MB (22287865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
