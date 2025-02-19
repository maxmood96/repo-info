## `docker:28-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:6c125d6f090b22b786e24c64ac598279a3e9ea5eadb091564c0cb228d85a4d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:28-rc-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:5cc91e936f3a13dd694df971332018d2ccc469ba629010ca7da92b56fb53e58e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200052100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8704bd867cfc67a7d43bb170fa7fe4b7706ece2cb57eec4345ea41b09066067b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Wed, 19 Feb 2025 01:13:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Feb 2025 01:13:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 19 Feb 2025 01:13:46 GMT
ENV DOCKER_VERSION=28.0.0-rc.2
# Wed, 19 Feb 2025 01:13:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.2.zip
# Wed, 19 Feb 2025 01:13:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 19 Feb 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 01:14:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Wed, 19 Feb 2025 01:14:01 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Wed, 19 Feb 2025 01:14:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 19 Feb 2025 01:14:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 01:14:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Wed, 19 Feb 2025 01:14:12 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Wed, 19 Feb 2025 01:14:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044271d4218f928b9c314cbb988a85c92771ffb8be6bc8f6dc5d0690dcbfdacc`  
		Last Modified: Wed, 19 Feb 2025 01:15:16 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b9c4df5e64b2a6853c0f641ac8ed47dba1144c4dd5f21b91ef5af1f78b193`  
		Last Modified: Wed, 19 Feb 2025 01:15:19 GMT  
		Size: 349.7 KB (349701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037e658326392444793a99e278e43b461ff88cde42eaf645d4a8c79136f97710`  
		Last Modified: Wed, 19 Feb 2025 01:15:15 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d6b615b9779dd0ccc3d1b92ff0884590f2d51e37b854809a415b16a36b66a4`  
		Last Modified: Wed, 19 Feb 2025 01:15:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f2553939c59e9d864c8deed955c82d1c1b0c1513febb2ec21e565a674dcbf2`  
		Last Modified: Wed, 19 Feb 2025 01:15:30 GMT  
		Size: 19.8 MB (19810421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4197cc1b392ceb3437e8368c3593449315e5c161dd08697a3341ffa1415994`  
		Last Modified: Wed, 19 Feb 2025 01:15:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2389c2be07cd42f93f170166d6d5c601d38eae3ca50fc03de83273634a49f3c8`  
		Last Modified: Wed, 19 Feb 2025 01:15:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d714ca1613ba445a542d20d1eb268c55fa2b0d4dd35ff6067d2509f18196bd2`  
		Last Modified: Wed, 19 Feb 2025 01:15:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b767934ffcd2b365a3de3862a1532c6434bcedd89d8fd1e6560475255ae882a`  
		Last Modified: Wed, 19 Feb 2025 01:15:21 GMT  
		Size: 21.1 MB (21147143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9a8381a114aec70f0a53c2214233a8a3a63972791818c43e35c60e55ce338f`  
		Last Modified: Wed, 19 Feb 2025 01:15:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a248cfad50d573a1fa9818971c82eb12d5be8615cee01a8f2f91e310674f24ff`  
		Last Modified: Wed, 19 Feb 2025 01:15:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817ec5cb47eecee84b312d330954fd1f5265f7d8d8af796f99f043b67973d253`  
		Last Modified: Wed, 19 Feb 2025 01:15:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035b9c2b8f395cb10a7b84c797dffd5c5acebf84583c0894806d5e14da6f777c`  
		Last Modified: Wed, 19 Feb 2025 01:15:22 GMT  
		Size: 21.8 MB (21824262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
