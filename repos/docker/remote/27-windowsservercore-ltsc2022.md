## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6550e15f54a41601f5bf6cc07cda68d35cf115561478d97cc87dfdca2b7e8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 22:06:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 23:23:34 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Wed, 15 Jan 2025 07:14:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Wed, 15 Jan 2025 07:02:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Wed, 15 Jan 2025 07:14:52 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 23:23:35 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
