## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a729e92ce46488a613985944b915ad333231980c8321d66631e06f0a3b33dab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:39d173c2db9c15f71f5b50faef55819f9c55e044530ccccbebd440829fb8f1b9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638051869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f3aaea22cce41f3d02ed4eec95516369dd7732afdd0c4d4cb27eefb112f327`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:47:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:47:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Sep 2025 21:47:48 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 10 Sep 2025 21:47:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Wed, 10 Sep 2025 21:48:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:48:01 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 10 Sep 2025 21:48:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Wed, 10 Sep 2025 21:48:02 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Wed, 10 Sep 2025 21:48:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:48:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 10 Sep 2025 21:48:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Wed, 10 Sep 2025 21:48:11 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Wed, 10 Sep 2025 21:48:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee5668bf3ba1627541264428f67a2ab55326377dac447bebf1d4c10460b655`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d2b2de66d66d454ae12d0115615260ed18f394cf82b517cf78e83bc2afe7b`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 347.5 KB (347515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1aa8fa086b8b592be67349daba24adedc56f12e010176aff0943dc8c2c30c4`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f982327a77ccdd1f25e5644d989b11e7e1c2b9fea77c7770468aa38e27508a8d`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e577c683d4de2733464b92a27ccd02ea6c1bcc8a33bb57eea5dea54d094ce1e`  
		Last Modified: Wed, 10 Sep 2025 21:57:06 GMT  
		Size: 20.8 MB (20771445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5177245276d6a5f9726b0d81215b0fc4064f7fdb07a22075313ecf00e2748bc`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab34a9829e7cd7ec4f650ab1b9eb787261e99c74258307dc6cf025ed03a299fd`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d409b6063c630b2905be96e713d1d37335ad9c271761ff4599e3828832f06161`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4814286d72315ff3c413d6681bbf8379b3446f3178e3c262fc2e9782312b9e`  
		Last Modified: Wed, 10 Sep 2025 21:57:07 GMT  
		Size: 23.1 MB (23113497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d8eb00e24d9a4f16c7653a50a342c3173aed863b4e0a041847ada36d70b31`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faffc5fd7e6a639ab8983514b426e6d7f02380f4ad4d5a09e5aeb6b6cc1f4fda`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4251d3208997562f3376efe6f5474e146d7ad0ea310112bbfc359d4a998d3a`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9070d4e88bf02e5eba8c5561dd3c4f9ed5996ce9b57f675c22bd2935b18557b`  
		Last Modified: Wed, 10 Sep 2025 21:57:07 GMT  
		Size: 22.4 MB (22367853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
