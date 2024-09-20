## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d436ba51852b1b7153307c438211d920860c7c1f8afe56ff64e0c89ec8eb79c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
