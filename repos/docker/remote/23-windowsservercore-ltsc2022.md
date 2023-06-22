## `docker:23-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:2498d2cd153632d567309aea059eb73fa152795fda13e1235b8cee90e94af518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `docker:23-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:430e21751f2891894ee1872e6ca49f6ab5d2505612f13a1376de45a9305afc57
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1442546115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8840fd63727ebde60fad3ef5df57965285407624184f1e90ec64b41181a4d9f2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 14 Jun 2023 17:38:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jun 2023 20:51:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Jun 2023 20:56:36 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 14 Jun 2023 20:56:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 14 Jun 2023 20:57:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 14 Jun 2023 20:57:07 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Wed, 14 Jun 2023 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.windows-amd64.exe
# Wed, 14 Jun 2023 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=e314569943a591a097fa9119bf786556a4eb5c710e8ddefa57e95cd95aa7cc7f
# Wed, 14 Jun 2023 20:57:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 22 Jun 2023 00:16:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.0
# Thu, 22 Jun 2023 00:16:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-windows-x86_64.exe
# Thu, 22 Jun 2023 00:16:36 GMT
ENV DOCKER_COMPOSE_SHA256=dc6bd9c2016bbf7564959249204af044edf57ea4ff40238c5ecb4541a9d41573
# Thu, 22 Jun 2023 00:17:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972ddd233121a2afd2cf1a3eaec49d595cfe6b3ebe19ef3dd492d99784c370f`  
		Last Modified: Wed, 14 Jun 2023 18:17:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91e748fba47776a59c90f030f85ac47a68b36e81bfb09e869a091a006a4d557`  
		Last Modified: Wed, 14 Jun 2023 21:00:45 GMT  
		Size: 315.6 KB (315648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e84efc64649b1c3f25ad20275a6bc9edd38b3a067efbeeb3dc0f8704ecaf55`  
		Last Modified: Wed, 14 Jun 2023 21:01:25 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f47d04b05a1358406847a6e06be2d1594972002278035927e2cc412e62ee35`  
		Last Modified: Wed, 14 Jun 2023 21:01:25 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d261f384eb08a19fdb376c1d2c49a09faab74994a266e6e00257a08e1e0ab4ec`  
		Last Modified: Wed, 14 Jun 2023 21:01:28 GMT  
		Size: 17.3 MB (17316698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f71f1cd4b0927673a23bea443c12fe27c37c30c3fd4fec16d108d827c7d52fa`  
		Last Modified: Wed, 14 Jun 2023 21:01:23 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7cdeaa40266ab867cdfccccd0cf5a59fa5ba15d42b4cf6858a7740b3418418`  
		Last Modified: Wed, 14 Jun 2023 21:01:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802d2851d7207e4cf840870136e73056234d780b231d8ed8a8f888f3a49956d8`  
		Last Modified: Wed, 14 Jun 2023 21:01:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec0860eff5042e8e4aab65a6a3094065decb5ffb26aa3887d8168d3d44dd3c`  
		Last Modified: Wed, 14 Jun 2023 21:01:26 GMT  
		Size: 17.9 MB (17859733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f3c9ef8a22ae79c0a98be7f5aa258b25e4f43bf7e4e6fd8d9ac7193c6801e9`  
		Last Modified: Thu, 22 Jun 2023 00:19:00 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afce411b81889d1e3c8e529ef5a495262fae7e61acb4cdf60ffe43b057ca5111`  
		Last Modified: Thu, 22 Jun 2023 00:19:00 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896bdb3dee3442f802f207e5a0346838350b39f19e40fe0b9158636999b932b`  
		Last Modified: Thu, 22 Jun 2023 00:19:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ab15afa1e1ad0557c0b9421a28beb308958a3775fdd989db94e79b8b5f0de4`  
		Last Modified: Thu, 22 Jun 2023 00:19:05 GMT  
		Size: 18.4 MB (18442988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
