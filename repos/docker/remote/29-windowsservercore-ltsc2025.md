## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:e70dd93fb31ea4f9f717b82d89f543124c83d9ffeaf27a6cd4648611d83988dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:c9375e23c219a58d22de86c5365ad4a3df9cc597a6dafea5e821c9e4e50f1f61
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2025361096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86a12d887bab67a2db5d0b41d4bd78ae92498b3b7797b95a0aaf53c8761514d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:51:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:51:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 22:51:46 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 10 Feb 2026 22:51:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 10 Feb 2026 22:51:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 22:51:57 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 10 Feb 2026 22:51:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 10 Feb 2026 22:51:57 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 10 Feb 2026 22:52:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 22:52:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 10 Feb 2026 22:52:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 10 Feb 2026 22:52:07 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 10 Feb 2026 22:52:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f3641b48551abf691e707ba76f8b07a225d509249237749ad0c13cbcab89a6`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93109682ef3912c071c715e24f0d1b167c77a36b603db4e4b4ba87b0e41fb44`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 341.1 KB (341113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fed3cb55905ff4b923956923962134f6b56682edd3f49f72f73c7f991caf78`  
		Last Modified: Tue, 10 Feb 2026 22:52:22 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d52847d7a99dc3712781780484ed2e658cb2d6a9eef03cc2c03c084705832fb`  
		Last Modified: Tue, 10 Feb 2026 22:52:22 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b422d01a05845e46e72c0b6bdc60ab10afbed6f2686c298c152ef1a352f8bcb`  
		Last Modified: Tue, 10 Feb 2026 22:52:24 GMT  
		Size: 19.4 MB (19419123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d5839b3c533adebc5f128e1dc97b36a0ea748ed0c55f4a668d441f83379d7`  
		Last Modified: Tue, 10 Feb 2026 22:52:20 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee097239df91c424e239b0de48100e7fef995ec5513016d4a9cac0053eb1e5c`  
		Last Modified: Tue, 10 Feb 2026 22:52:20 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6544e451a45a70a8d1cdebcc90125e88eeee39840ea196ce78adf289c85ceab`  
		Last Modified: Tue, 10 Feb 2026 22:52:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46382a7a13c77b8fe6a92f8bb021ceb39e2115352c7f70d7efe8663bb07ba3dc`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 29.4 MB (29395150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa16f67b883942ca441126845d8596234a08d46d79b6f9b197d750f05f33ef4`  
		Last Modified: Tue, 10 Feb 2026 22:52:19 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dd787c124803a1db43ba48aafdd861693d324b06337b3575e36c1bfd8b98e4`  
		Last Modified: Tue, 10 Feb 2026 22:52:19 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6dc08f0810d450a6f7c42c18c61f6870cb7a748b544039c9794514d7facc7e8`  
		Last Modified: Tue, 10 Feb 2026 22:52:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ff00b2c954ee8f88bb7d63f0ef83627a6efbff11e870d0b5a9f9e8d60fdb7`  
		Last Modified: Tue, 10 Feb 2026 22:52:21 GMT  
		Size: 11.4 MB (11433950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
