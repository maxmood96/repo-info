## `docker:24-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0a9107851c15d1ef089be6991e5ddd4d90021dd3602be79d1f95ea57f94f2a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `docker:24-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull docker@sha256:823579f2be785b9fd5508ca7f16af80cd25bf47460bcecbd84c74905c79fdd15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1814902095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d509df9afeb7d2fcb77a7bb30a5474e5d6a77a4cc984ccbeab49a412f6f87217`
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
# Sat, 15 Apr 2023 00:15:03 GMT
ENV DOCKER_VERSION=24.0.0-beta.2
# Sat, 15 Apr 2023 00:15:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-24.0.0-beta.2.zip
# Sat, 15 Apr 2023 00:15:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 15 Apr 2023 00:15:34 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Sat, 15 Apr 2023 00:15:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Sat, 15 Apr 2023 00:15:35 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Sat, 15 Apr 2023 00:16:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 15 Apr 2023 00:16:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Sat, 15 Apr 2023 00:16:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-windows-x86_64.exe
# Sat, 15 Apr 2023 00:16:05 GMT
ENV DOCKER_COMPOSE_SHA256=0869cfe9d799d511e4eaf87029ed08ea256e7000f312023c062d7ddcadc385db
# Sat, 15 Apr 2023 00:16:29 GMT
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
	-	`sha256:f2950c2247196d386b0386eba7b53990e94ef585d0724b255d338db4f996d273`  
		Last Modified: Sat, 15 Apr 2023 00:21:39 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8639a0341a1d57b29a459ebc0b860c5b791e5c4d0dc1c315bab0556ba4f070`  
		Last Modified: Sat, 15 Apr 2023 00:21:39 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f321866acd3d344655258f19754a838ce64a1992df2aa20c4c49ea5889d655`  
		Last Modified: Sat, 15 Apr 2023 00:21:42 GMT  
		Size: 17.7 MB (17714464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891863d5be0020937a4c67fcd2d822c104cdac69778fef5d4345d13de187f15d`  
		Last Modified: Sat, 15 Apr 2023 00:21:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a54324a5fe374131f9b366579a0fe019425e54124b18b9faf6df2fc64cefb7`  
		Last Modified: Sat, 15 Apr 2023 00:21:37 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e02c5d4380489f6ecb1555f5580beeea8c0145faca076721091a40fec4e101`  
		Last Modified: Sat, 15 Apr 2023 00:21:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5025fe9b9747aa85183abf016b368b22c5ccc73bbde7f5068f0ec50e6286b088`  
		Last Modified: Sat, 15 Apr 2023 00:21:40 GMT  
		Size: 16.7 MB (16717438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41138feca8a5df23271b7f859ec5660ffe017b67e68f86369cec9dee81518b1`  
		Last Modified: Sat, 15 Apr 2023 00:21:35 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63239fe3efd18ac5bbf2bf7eee519676431441371d1ebccc349f1062b641c0e4`  
		Last Modified: Sat, 15 Apr 2023 00:21:35 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bd51e3ada61e95a7c0862ce4ce1a1f71a5ec16fa5ff743acfd18aa62b6f994`  
		Last Modified: Sat, 15 Apr 2023 00:21:35 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df15e1156e0367310c1ebd5db08f6cbec74ae5db50e4905fb13014f4ddc752a7`  
		Last Modified: Sat, 15 Apr 2023 00:21:40 GMT  
		Size: 17.1 MB (17089159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
