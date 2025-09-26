## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:41c600675f9ee0095671172e777d4cfb7b5dc56e1b37c723737024519484353c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:1d87cc42df550146b215cf76e8a02971828a50e53cc3d3ae9aaf7f5e30912181
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349062288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80109658e4ff01843b61e69230f1e740512424d9807390a0deb257a771d46b6a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Thu, 25 Sep 2025 20:54:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 25 Sep 2025 20:55:48 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 25 Sep 2025 20:55:49 GMT
ENV DOCKER_VERSION=28.5.0-rc.1
# Thu, 25 Sep 2025 20:55:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.5.0-rc.1.zip
# Thu, 25 Sep 2025 20:56:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 25 Sep 2025 20:56:06 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 25 Sep 2025 20:56:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 25 Sep 2025 20:56:07 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 25 Sep 2025 20:56:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 25 Sep 2025 20:56:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 25 Sep 2025 20:56:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Thu, 25 Sep 2025 20:56:29 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Thu, 25 Sep 2025 20:56:49 GMT
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
	-	`sha256:167a2d268e39075fdaa689e7a2734bdfefa65241235c320ebba11fdad31e6bc6`  
		Last Modified: Thu, 25 Sep 2025 21:09:47 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa846c8518e2620378fdd2e75ed36a9e8fc65340bd20683ab419dc34c430290`  
		Last Modified: Thu, 25 Sep 2025 21:09:48 GMT  
		Size: 377.5 KB (377461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6dbca6f5ba0aac820649ea42a2ec71d31966f437dce49de56042fc377a8b43`  
		Last Modified: Thu, 25 Sep 2025 21:09:49 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344e641b2a2df15d4f4d14444da4a9e2904d3350b8ef184ff68a76de1dfc489`  
		Last Modified: Thu, 25 Sep 2025 21:09:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98ad3bc23ac8d66a2091c94975afef03665c03ab10ff87a616487c99270768f`  
		Last Modified: Thu, 25 Sep 2025 21:09:52 GMT  
		Size: 20.8 MB (20789390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd46e4f8979644eed1cb4f94a92e6119053ceae28ea6f4824179d0ee9a69585`  
		Last Modified: Thu, 25 Sep 2025 21:09:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a8e6fd8e8393cde38ecac13f9a8005790645a8c5d4936f399c6e6e56b48dcb`  
		Last Modified: Thu, 25 Sep 2025 21:09:53 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1794372cc5ec289b2d233cd5be061bf4bfd68318d1e797f86a6d8de3d54de47a`  
		Last Modified: Thu, 25 Sep 2025 21:09:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e4b8ab7e9a3e395756ed60fb4574b6420624f58070902a3f35c0f78dfda482`  
		Last Modified: Thu, 25 Sep 2025 21:09:57 GMT  
		Size: 23.1 MB (23144486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195ff2b8302e7844680c746a4a7329b92b78670d77753a6e5e64712a202bd811`  
		Last Modified: Thu, 25 Sep 2025 21:09:57 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6484998374c6e1ecc52176c23dab3c3a6369b7c69dde79cd5189787aae413905`  
		Last Modified: Thu, 25 Sep 2025 21:08:57 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0093e801c4c63bdce68bfa181d7d6bfe0594ebb64ad86ceec58aab6268cb929`  
		Last Modified: Thu, 25 Sep 2025 21:08:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e3e382d28a0c2bea9dbf1454ba0bd8a9dbed70c8d00ca1c9b9f88ee6efa636`  
		Last Modified: Thu, 25 Sep 2025 21:08:59 GMT  
		Size: 22.6 MB (22594242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
