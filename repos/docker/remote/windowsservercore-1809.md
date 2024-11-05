## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
