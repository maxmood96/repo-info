## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:570b2a0cb54cc1e4fb3c9c360c9fbf31c58a67160ffac2f851d5320b2220ee3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:a105d81267b506d283738c2eab0c3e5f2339533f55a3f4e578543f31a10c0559
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136248524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d491b6f638ed8098ef9803e3c78743401083c443ad9969e0c8c97b4a5061c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Fri, 03 Apr 2026 16:48:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:27 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:48 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:07 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be287d655249644e43f567922c8ace0ebd34d2029a63b5f7aff779c7f0ea81f`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bacc8dcf99a4b510435fd53e918e3bd0d6f4fdf27dcb309c4534ce03060f4e4`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 370.7 KB (370685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75b1a0e09957eca68ed1d9ce466b166f611394669ffd7e2ef3cb280d2e86086`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cd9630a95f491844d8e8a681bc533e92b0e16ccf40b4842c76d47b05c88b82`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea0afb7d1d92072a6f67dc1f20ac520593a6d5b6e34fd654db0236504072e6b`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19592556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851c661eadabfff21636e396053a6ef65d7806e441da086e892a0570aa37b52`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eeafb0e1065fbf8e495e596ab0979a2351aff4f33b4e1dc7d6c99f871eae97`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a24fd78eaaa140c5da70cb45d1a53de3c80317b8541f80a1d05bd6e4560022c`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe15c09ff0502ba71e3b975f0220d421f288c20d8c5d5f64c098496b4d84efdc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 23.4 MB (23432034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39061e0c2bb20d115f630e4eb90cda590eae044db260d399ae125e5b4328ff96`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb55d0d2e05e9f25e431de1cb3fea9bd5a99ce82e687614b9e3d5ac2bfbfaafd`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c676b321d5f609545214e994c74729fcfa063fb1814060367301f2b68aca4`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194caab5fefbe0467dced96b2a1e8533cd36bc07325c3061cff834433fab53d5`  
		Last Modified: Fri, 03 Apr 2026 16:50:25 GMT  
		Size: 11.6 MB (11645348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
