## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:456f07f6a9e9737a0d47e0104821d7ad21903dcf0f9ecd3c47e7e627903f7701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `docker:rc-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:0c2c8feea0c45a1f9c150cfeeef10c85f169f45009ea5f5bfd184ff15757ccba
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955458380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f459f16ceabf1c3484c3e9ddb2402eeebe7a63d0357d762b55d3b4deab826fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:00:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:01:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 11 Jan 2024 00:01:09 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Thu, 11 Jan 2024 00:01:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-rc.1.zip
# Thu, 11 Jan 2024 00:01:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:01:19 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 11 Jan 2024 00:01:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Thu, 11 Jan 2024 00:01:21 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Thu, 11 Jan 2024 00:01:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:01:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 11 Jan 2024 00:01:31 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Thu, 11 Jan 2024 00:01:32 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Thu, 11 Jan 2024 00:01:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f880bd468928b00dd9f2f28b577ab09dfa8cfee0f9fb757ef43650ad05dfee74`  
		Last Modified: Thu, 11 Jan 2024 00:01:52 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c97174961abbfe9a13ef0cc098a3ed871e7fa10b7c98d1fe0d30760d6e33f6`  
		Last Modified: Thu, 11 Jan 2024 00:01:52 GMT  
		Size: 483.3 KB (483315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e222bb574e59bbabaad4e62a07f816863494fc98342788b81567b7e63c07e891`  
		Last Modified: Thu, 11 Jan 2024 00:01:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98154abe26284b80a1f191504b3e035fdff4d5ea82b06fe6fe3c995152954736`  
		Last Modified: Thu, 11 Jan 2024 00:01:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfb1db29c2c951315fc12e984408ebd5e4c50b56cd1327cb19d23152fd5b268`  
		Last Modified: Thu, 11 Jan 2024 00:01:52 GMT  
		Size: 18.1 MB (18050605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25053ff6c07d8696555b883f1bc0207c3d4f8aaf1635b924fa902c070aa4ffb`  
		Last Modified: Thu, 11 Jan 2024 00:01:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f61d8da6c8a8974f8f4d07a182d3d657a6516166843658d1e87117b706387`  
		Last Modified: Thu, 11 Jan 2024 00:01:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e780891d10e2bc5cd0ef98caf4b0511f9ec3b7b1163bf8415152a3071d3621`  
		Last Modified: Thu, 11 Jan 2024 00:01:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce42a36ba00257aa28a2c7ea0e6bd1ec26303de6337ababc5e7c5b550393064d`  
		Last Modified: Thu, 11 Jan 2024 00:01:49 GMT  
		Size: 18.0 MB (18007685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89d4a1b7901d18adf2682a7541f1ec6d13d06a52032bdcf4a404aa13f192050`  
		Last Modified: Thu, 11 Jan 2024 00:01:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618223c023a5a4d3deec2632a0dbdba59c59ef5c75c706ed441b95db1748fe82`  
		Last Modified: Thu, 11 Jan 2024 00:01:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66273205cfeda531fd49f260948e5dcadd8bc74a923b245197f897cb478efcb9`  
		Last Modified: Thu, 11 Jan 2024 00:01:46 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14df6ffaa10604785c7e5cde1149d205317ca696df3e21f84b0784edaef9c2d`  
		Last Modified: Thu, 11 Jan 2024 00:01:49 GMT  
		Size: 18.7 MB (18692370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:ad8c693a1f4f000226dabd24c013249a5bba8f6d80f73ab5fc5c50fed898183e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125004298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01568c6c90637e611908dc2e078ea781b15cf9e40920d0f90e41e0923fbefa6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:10:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:12:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 11 Jan 2024 00:12:15 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Thu, 11 Jan 2024 00:12:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-rc.1.zip
# Thu, 11 Jan 2024 00:12:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:12:44 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 11 Jan 2024 00:12:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Thu, 11 Jan 2024 00:12:46 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Thu, 11 Jan 2024 00:13:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:13:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 11 Jan 2024 00:13:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Thu, 11 Jan 2024 00:13:12 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Thu, 11 Jan 2024 00:13:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fedeaac156379923b249c926f48d3d82ddf940e19fef21c5cb25dcb1e9a4cd`  
		Last Modified: Thu, 11 Jan 2024 00:13:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f700c3ecff3905133f66e3cc1335b8ff003402818a1d5b22b28bfd9ceffb1e87`  
		Last Modified: Thu, 11 Jan 2024 00:13:48 GMT  
		Size: 485.2 KB (485172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7e56a04987c7363481f0fd0b60a5de0f44f13eb60f42fa5a3a2ed697e28ab`  
		Last Modified: Thu, 11 Jan 2024 00:13:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1779738a573d2f9c39e6bd713453741f7a4b90c7021b233b139e2afdd6e12098`  
		Last Modified: Thu, 11 Jan 2024 00:13:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fa1b0d967e65783df3db796927fbf3831dbb869cdf253f9f4bfd79b1c0bd26`  
		Last Modified: Thu, 11 Jan 2024 00:13:48 GMT  
		Size: 18.1 MB (18063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92691492950a59f6cf44c5a88ac67d1e16d49c175b14f72ca0aa422018ad2b6`  
		Last Modified: Thu, 11 Jan 2024 00:13:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af152c762760770894f12825c8f61865557b6369ecf575d5fcf6c89cf83896f1`  
		Last Modified: Thu, 11 Jan 2024 00:13:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99348a2debeda38b1f30d84de5ee1d3b25ab1737aff17b0125d18ff7cbd25a3a`  
		Last Modified: Thu, 11 Jan 2024 00:13:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c9aa82831b92856520bbad0673b6aef55c9d35632d3978d461ebedd627df62`  
		Last Modified: Thu, 11 Jan 2024 00:13:45 GMT  
		Size: 18.0 MB (18021101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c917f1bf41e242f6379fc841aa53b402d66a70bac170b6eae547512cc56ac7`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cd159f5c351560c90857b8329f0720f1e37df719630e97496830022be29c48`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5b70540d8dbc00afcf6cee2315a18070b9b23b95e63e6ddbe5b2eb2b43fb05`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fd34ca4b5354f44e250dd272c4cb23ae480cc309da8262f58bb57802f77d09`  
		Last Modified: Thu, 11 Jan 2024 00:13:46 GMT  
		Size: 18.7 MB (18699921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
