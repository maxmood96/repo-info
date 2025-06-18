## `docker:28-rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:80edcdf0f6a7f47645a9133189ee479e3af19b20bbdaf7423a4adb581023afd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:0a2f145b6407d5d68782eaf6a32e182e2c11d39221e8b24fd97716a56d2980f3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542219022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d211d59e6327843275018159670da3328e90b7d1f9afa25d6e56c8a32d7e01ca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 18 Jun 2025 16:44:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Jun 2025 16:44:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 18 Jun 2025 16:44:13 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Wed, 18 Jun 2025 16:44:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.3.0-rc.1.zip
# Wed, 18 Jun 2025 16:44:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 18 Jun 2025 16:44:27 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 18 Jun 2025 16:44:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 18 Jun 2025 16:44:29 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 18 Jun 2025 16:44:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 18 Jun 2025 16:44:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Wed, 18 Jun 2025 16:44:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Wed, 18 Jun 2025 16:44:41 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Wed, 18 Jun 2025 16:44:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d328ad7cd67a157bfd48cfd259255a63c4bb60062d4338ac5bb390fe2e181b`  
		Last Modified: Wed, 18 Jun 2025 17:08:00 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49e97739c9ee7a597996286010d84627562b8be01d44083166eb2606ce487d`  
		Last Modified: Wed, 18 Jun 2025 17:08:00 GMT  
		Size: 401.7 KB (401657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef42592b2685f1ea780126a6db963a2813d242d6c6b93b7fe5e03bae121e76c`  
		Last Modified: Wed, 18 Jun 2025 17:08:00 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a8fad66e879ff5956222852f946dcd907af93389ee7edabd6a0f7e0f4ce5fa`  
		Last Modified: Wed, 18 Jun 2025 17:08:00 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77def14ebf28f410b2ef7538bf72dabd4a88cf7a96e0d83870b7db7ec79432c8`  
		Last Modified: Wed, 18 Jun 2025 17:08:02 GMT  
		Size: 20.9 MB (20864583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfee3f7fbe0f5239229a7b9104b265a39ef89d5c11c892ad64b97f418c3e572`  
		Last Modified: Wed, 18 Jun 2025 17:08:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2d8e18e5120c9205106520989d01bc80c18476924f5621f1f080b9a95fdf05`  
		Last Modified: Wed, 18 Jun 2025 17:08:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af26c9a3b38afec0aa41442763b69e7204b089167e0f8184a0590b3a7b9da9a9`  
		Last Modified: Wed, 18 Jun 2025 17:08:00 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b193fb8b7d7802247433d6bf70ab4d2574d214044f0cb5cbbe6c4e906b113f`  
		Last Modified: Wed, 18 Jun 2025 17:08:04 GMT  
		Size: 22.7 MB (22691620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d248999ed4f854bb3258d55bb89f647f13de5570a5277ed779edb535af319e2a`  
		Last Modified: Wed, 18 Jun 2025 17:08:02 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756003ccf2f28d43ea98e8d78e6f888fe636b8e8b9cc4feb806a04a1df800cbe`  
		Last Modified: Wed, 18 Jun 2025 17:08:01 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e191b559b05fae292f391875b437c1a0fda69aa62cbfbe5144a6596fa812d`  
		Last Modified: Wed, 18 Jun 2025 17:08:02 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e389232ff1ab235f6f6edebb56ce5171a0cfdfa58ce12698a286db6f27e5ca6`  
		Last Modified: Wed, 18 Jun 2025 17:08:04 GMT  
		Size: 22.1 MB (22075132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
