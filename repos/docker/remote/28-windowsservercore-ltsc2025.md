## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c21bb41951b8d050423571b9ad3fbc7922dcae93a52eb4b139ce335ddccb307f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:51d29cbeeca1c20f7f40dcc31d1430f1b1a843f18af07e6db7bf8a4806af142c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565260785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d57a46de5021912d4caf6f61effcef07c11c29f826f224884a2f479533bfe7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 26 Feb 2025 23:30:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Feb 2025 23:30:59 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 26 Feb 2025 23:30:59 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 23:31:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 26 Feb 2025 23:31:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 26 Feb 2025 23:31:11 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Wed, 26 Feb 2025 23:31:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Wed, 26 Feb 2025 23:31:12 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Wed, 26 Feb 2025 23:31:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 26 Feb 2025 23:31:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 23:31:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 26 Feb 2025 23:31:22 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 26 Feb 2025 23:31:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb10126a1203d4c66c7f1bd2d046403435188de2b4e803e68a55bde02277feb`  
		Last Modified: Wed, 26 Feb 2025 23:31:42 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a541a4bfb1bd4af941cc499e1eab1f74600e4e3096f4284c464e7360ed2614df`  
		Last Modified: Wed, 26 Feb 2025 23:31:42 GMT  
		Size: 392.1 KB (392068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f723a543ec211b4c562734914e9b44919ffdb47434842671ecc6242f4de41f35`  
		Last Modified: Wed, 26 Feb 2025 23:31:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f3888010c943088f39af77d926cf458856617ee6c96966d7129b7a4d07f090`  
		Last Modified: Wed, 26 Feb 2025 23:31:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba20276db292dd4183615b293b4d07543ff04e36c43b0261b2799bc25256edc3`  
		Last Modified: Wed, 26 Feb 2025 23:31:42 GMT  
		Size: 19.9 MB (19860186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d693177623270a2df11e1e1f62a1aab5fb94cb8d287b3c31924b9f9bf6d23d6c`  
		Last Modified: Wed, 26 Feb 2025 23:31:38 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19620ce2dfb2af4a6904d70f22bf0f0553b1f9ed384a0f2716d3ad217bebe4c4`  
		Last Modified: Wed, 26 Feb 2025 23:31:38 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6a1370ad1c5fdb7bd63a0bdc971e83b16fbae5d819fe2cc2208fbb94236809`  
		Last Modified: Wed, 26 Feb 2025 23:31:38 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3436dd6e2b774d5af2f08bc4c349a64ab0e638bb82fd72eacc2910919f1a66dc`  
		Last Modified: Wed, 26 Feb 2025 23:31:39 GMT  
		Size: 22.8 MB (22787344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a936f233a90aa7e5f8df6771bae3bc8223b91eab646091dc40da8461ac32a888`  
		Last Modified: Wed, 26 Feb 2025 23:31:36 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b384e6f7aa2f98e11af8d9a8b27df36af6490fde29567477276bd59b9689b12`  
		Last Modified: Wed, 26 Feb 2025 23:31:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5997c4a1e633eaa29ad87617702743f93036c3faffcf29bab90d83743168e9a9`  
		Last Modified: Wed, 26 Feb 2025 23:31:36 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b9b40633e17bc09799a8faae77798a7476375a19ff2e8d5192f61566888c69`  
		Last Modified: Wed, 26 Feb 2025 23:31:39 GMT  
		Size: 21.9 MB (21931776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
