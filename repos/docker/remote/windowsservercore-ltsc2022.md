## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:db0bfd3a516588b0264a2e917d8ffc5747a8fd92f7071c31936950dc134bffdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:386223997bcd45bc3900c73f723f972d9acd82d397dd32439c9d9b8779b01bd0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2176463119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33eae8894e487ca61eb33dccf81effb91f53113f0d82c7030c2a7444c6231659`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Tue, 02 Jul 2024 00:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:57:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jul 2024 00:57:15 GMT
ENV DOCKER_VERSION=27.0.3
# Tue, 02 Jul 2024 00:57:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Tue, 02 Jul 2024 00:57:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Jul 2024 00:57:26 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Tue, 02 Jul 2024 00:57:27 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Tue, 02 Jul 2024 00:57:27 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Tue, 02 Jul 2024 00:57:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Jul 2024 00:57:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Tue, 02 Jul 2024 00:57:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Tue, 02 Jul 2024 00:57:37 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Tue, 02 Jul 2024 00:57:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb72fa6f17dfe9cd6454fb6dccdf6ca8fd19c212ede13b12c0ae062eff682f00`  
		Last Modified: Tue, 02 Jul 2024 00:57:55 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591b238929736a7300bb23fc793f3422ca4db1c36d13aec6bd23679968f5f7a4`  
		Last Modified: Tue, 02 Jul 2024 00:57:55 GMT  
		Size: 345.9 KB (345918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16014478e439a58518a38275671775c8a4954d9760b3a9bbebcdd57b8e2bdde0`  
		Last Modified: Tue, 02 Jul 2024 00:57:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3dc8c45fe3b5babaaaecec22050ef89d5373c83c39a7ba825a6c1c45f65b75`  
		Last Modified: Tue, 02 Jul 2024 00:57:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ebcdce69c445046638fd14aebf746d380ac04ce47f12a75d2fe4497d68b2d8`  
		Last Modified: Tue, 02 Jul 2024 00:57:55 GMT  
		Size: 19.3 MB (19255478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d58621a7b6be7445776140df24b5f8ada14acd0c9a3829d5ed64a68e864b03d`  
		Last Modified: Tue, 02 Jul 2024 00:57:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a615bbba8193c315e67683a98737824112f08d79977d516cd10865815a41ec`  
		Last Modified: Tue, 02 Jul 2024 00:57:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d7c351bb144e09dec014c82f8fe44e6ac8230a962c1981f24bd89f990dbd1`  
		Last Modified: Tue, 02 Jul 2024 00:57:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282a2ce5d6e772e4d9c63b5e6e779005176aa6526c5db9eda06c98461676007`  
		Last Modified: Tue, 02 Jul 2024 00:57:52 GMT  
		Size: 19.0 MB (19012372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732dfbb736368c7fe17a9c9de6828f6df1c38b274b3b7bed07da9bee6e949989`  
		Last Modified: Tue, 02 Jul 2024 00:57:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be92b0ac83eff3339d03e5ad0058911360ae9d21d17d0b233211c01715df53a`  
		Last Modified: Tue, 02 Jul 2024 00:57:50 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeb8fb03ab79ed8c37fb237ee93477a3ff05e8175bf768431d4ddb5058a2086`  
		Last Modified: Tue, 02 Jul 2024 00:57:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b25ec1f39df1d91b09b4fd2766030fdef0f29911749b781eff8de43d032a333`  
		Last Modified: Tue, 02 Jul 2024 00:57:52 GMT  
		Size: 19.6 MB (19647506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
