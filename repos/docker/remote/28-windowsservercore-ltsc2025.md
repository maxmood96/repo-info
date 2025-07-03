## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:47e4025f5f5eb4bb57f9bc7b3c77d306050988fe620d7ee3e7af4720382fe323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:6fd3a0953d971332397c8e5f14fa538fc9feb8ee0df0761ef69cc664d2c15d5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542412535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7fb045a7559131f0319249930363ace2c34f3549f5254f962c31ec2b021974`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 03 Jul 2025 17:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:28:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:28:01 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:28:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:28:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:28:17 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:28:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:28:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:28:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:28:30 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:28:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8360bc4e45fd1207fbb8507f009f2fafe0c692dda8013b87da385b1687fdb93`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee70f98e67bab9d88bef6785da7dcb0243c6678f90f98f1819bb1d6f15bc400`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 401.7 KB (401674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79844d9fe7e509cc013db5713ac75c91fdef2469815feec90b5b5ccad0760d`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6417f363ada4659759175f87056dac7cb772357f80f942c6f12d9c3a511ae2`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754e9768d552528080346d5f1236df2b7fec0cc26703a72181ab5c56597d3874`  
		Last Modified: Thu, 03 Jul 2025 17:32:16 GMT  
		Size: 20.9 MB (20869952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773798f77aa5f53805ec80969f800c997234c80e3eeaeb70915df160d58698d7`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08de61fa1493600c5c1abb22fb424babbd40f76e25bc0cb27af06a1e6826699`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9638f01c3683753b6296eba7747c7453af7e93065c1727c6b1c271fe3a9ad03`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2aa5bce1514c94a539188e90cbf3433418f9aee7b02aa6196d1b252701f4a6`  
		Last Modified: Thu, 03 Jul 2025 17:32:17 GMT  
		Size: 22.7 MB (22693614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b469a4641279b25c6f4c69230acb7f20cf78488659ef25e4b936f65ad62f7f`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94637a4a498775806b5d83e9b9a5dc8b4630e91f61f2560420791e57745cf4ff`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b5885e19d477e90daf5b71748592e75e7b6b7ff7acedc236c6872db6a7e27`  
		Last Modified: Thu, 03 Jul 2025 17:32:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c38a51f4f1af8ed66ca040eb007a92422ee88d91d4dd660bd0f0f5214c46e7c`  
		Last Modified: Thu, 03 Jul 2025 17:32:14 GMT  
		Size: 22.3 MB (22261431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
