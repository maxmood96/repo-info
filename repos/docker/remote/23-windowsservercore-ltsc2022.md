## `docker:23-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ef4f467fc1f8e82a90e67d81aef8be7aa83aeb82d4873b2039031adf725bfebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `docker:23-windowsservercore-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull docker@sha256:e54be01f00ee3c6281696a9c5826cd017630dafb0014af82c8377b2bf936dd29
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1814778421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e603f37b4262bedcd47831e73f43aaad733567e49e478286c6cee2f0b46c13c1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Wed, 05 Apr 2023 00:38:27 GMT
RUN Install update 10.0.20348.1668
# Tue, 11 Apr 2023 23:37:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 03:16:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Apr 2023 00:15:02 GMT
ENV DOCKER_VERSION=23.0.4
# Tue, 18 Apr 2023 00:15:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.4.zip
# Tue, 18 Apr 2023 00:15:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Apr 2023 00:15:31 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 18 Apr 2023 00:15:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Tue, 18 Apr 2023 00:15:33 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Tue, 18 Apr 2023 00:15:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Apr 2023 22:16:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Thu, 20 Apr 2023 22:16:56 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Thu, 20 Apr 2023 22:16:56 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Thu, 20 Apr 2023 22:17:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ecfa9c953d28a9da9d422b57cd0361c57c44e1faaaed7e50a2537d1c29cee1`  
		Last Modified: Wed, 12 Apr 2023 00:50:33 GMT  
		Size: 376.6 MB (376573004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98474c9b39bb0e3a2d79dca81a90952011b65d1fa352021dacd30335d1bb69f4`  
		Last Modified: Wed, 12 Apr 2023 00:49:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9122c88a621359fadd2c1ab6702c4106dd74f6703813469a0911060138dfc8f4`  
		Last Modified: Wed, 12 Apr 2023 04:07:19 GMT  
		Size: 766.2 KB (766237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a219cf92a84309a1b8ad540a85b062c133a78360f6fb489de2a98d881807574e`  
		Last Modified: Tue, 18 Apr 2023 00:21:29 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2098843916f649e92bc7eba0a047034ab8559bbb93c4ea874de904281115ce1`  
		Last Modified: Tue, 18 Apr 2023 00:21:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5626af144bb4ab2dc0792415355afbdb61bb16afc36aec18babe98dda7eddf9f`  
		Last Modified: Tue, 18 Apr 2023 00:21:32 GMT  
		Size: 17.6 MB (17594003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428f24ed740b1f9578f359cc495eacf17ccf6883331b1c66f849c28d7d606b79`  
		Last Modified: Tue, 18 Apr 2023 00:21:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1da5249827f7669cc3d5d22670755356f4d539684de45ed97200c1d3d9c68b`  
		Last Modified: Tue, 18 Apr 2023 00:21:27 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd97497f9bc982f8afd78bd1b49e40239c5997cbe457eeada369ae2eac2be8d`  
		Last Modified: Tue, 18 Apr 2023 00:21:27 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca4248af8f5765b6c238796c780ee66d9c26eb6e88b2b8a54b28861ef35fb1d`  
		Last Modified: Tue, 18 Apr 2023 00:21:29 GMT  
		Size: 16.7 MB (16715647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dba72a49ee57276b748ee8b40ce3bd454bb0e349e51b3ac66632a0cec83760`  
		Last Modified: Thu, 20 Apr 2023 22:21:57 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391a2ce5f28c36540ad4942c22c827b4156c1369b19c56c74c668980304ffd8a`  
		Last Modified: Thu, 20 Apr 2023 22:21:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712faa569c7aaeb3bee863d5f14e20a1ffd049d60b4d3c708f2c9f11225196e`  
		Last Modified: Thu, 20 Apr 2023 22:21:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f7c11ec207a4edf82d2d60131dd99147190fe07fe3ce37ad85e6611e43f6c4`  
		Last Modified: Thu, 20 Apr 2023 22:22:00 GMT  
		Size: 17.1 MB (17087694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
