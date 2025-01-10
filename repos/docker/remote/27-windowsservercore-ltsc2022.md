## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:25bf8f6dc29b204e9017e3d31c80e96c68255a4ce33c11a8462e0160e4116ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:1da6c7e8b349109a2399aa1f4afe6cda30ada0905c49dfcc8341d5b675ee932a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312998479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791e0f9826828a09165ffea4987388ab83f2e0bb254733f1ec61d56c5888175`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 09 Jan 2025 23:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Jan 2025 23:11:20 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 09 Jan 2025 23:11:21 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 09 Jan 2025 23:11:22 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 09 Jan 2025 23:11:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 09 Jan 2025 23:11:43 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 09 Jan 2025 23:11:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 09 Jan 2025 23:11:44 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 09 Jan 2025 23:11:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 09 Jan 2025 23:11:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Thu, 09 Jan 2025 23:11:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-windows-x86_64.exe
# Thu, 09 Jan 2025 23:11:54 GMT
ENV DOCKER_COMPOSE_SHA256=f384ad29e5187745cad4c18a14ddafd5e7a748c68b5bd991599b1756e36d3bec
# Thu, 09 Jan 2025 23:12:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746b26a4cb7116e17132312a685032ffd7d82e43b97080d9a6668a52e6525990`  
		Last Modified: Thu, 09 Jan 2025 23:12:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b7416daf75b317c89da160f376430b2e71e61a6326cf5cd5de190863647dac`  
		Last Modified: Thu, 09 Jan 2025 23:12:07 GMT  
		Size: 366.2 KB (366179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b188a2d940569010f4e18ad5f8ee8033a1a3e2885ae83c5cc5bba49d224d03e0`  
		Last Modified: Thu, 09 Jan 2025 23:12:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3084c275f9515220e4b6002a2468b9d0be7a892cfdc0ea688e67bfbd78ca09`  
		Last Modified: Thu, 09 Jan 2025 23:12:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3659e66176301005d15b20f88f5a15ae13d9446e499e9f982bf37e2db9bdaf`  
		Last Modified: Thu, 09 Jan 2025 23:12:08 GMT  
		Size: 19.0 MB (18973896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed3f238e5809283b789b1b3b916173f607ad4f05a9673e0bd4c845a47d403c6`  
		Last Modified: Thu, 09 Jan 2025 23:12:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedce60013d3fc0b2989a0c3455bf2cef1325cdf0d8ad51f6426de401ec0cbff`  
		Last Modified: Thu, 09 Jan 2025 23:12:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f461394bc78451afaf1db6d61c8e8a8db8e7884540825ec9723b62152f2093`  
		Last Modified: Thu, 09 Jan 2025 23:12:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b6680d0e5dac8d4079ed658d15e2576544785586c727278c62b7402d68d3cc`  
		Last Modified: Thu, 09 Jan 2025 23:12:07 GMT  
		Size: 19.6 MB (19623947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdfbd8b7a5eddfcba726940d436363dce86e7ce4cb49adf690894db597d3ba3`  
		Last Modified: Thu, 09 Jan 2025 23:12:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd8cadbd7e8d33f80dcff7410787f703179eee0aaaab08a0aa8c31ecf617406`  
		Last Modified: Thu, 09 Jan 2025 23:12:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96969bbec2bc301c689777037b19459d4fbf0885fe68c6463567a5803b7f38ed`  
		Last Modified: Thu, 09 Jan 2025 23:12:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331501b0512b2e83330bc061ec0b4be1fb38b1fdeb1f7b2c0a72617e5776bc3`  
		Last Modified: Thu, 09 Jan 2025 23:12:07 GMT  
		Size: 20.1 MB (20149265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
