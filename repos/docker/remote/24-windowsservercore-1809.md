## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:80972f2e9f37af176b0394fa7856dd201cc68562fb9904058a80853bd648079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull docker@sha256:8b40966d96acf7c407eea7143d6215404acf25145bc4c191ac9bdffc9dcf04ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1993904989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb477c5e5e3c6f58d4b9d98370a26b68164c194d797e614a4c20909cc5a99483`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Jul 2023 00:29:34 GMT
ENV DOCKER_VERSION=24.0.4
# Fri, 14 Jul 2023 00:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.4.zip
# Fri, 14 Jul 2023 00:30:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 19 Jul 2023 20:16:31 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Wed, 19 Jul 2023 20:16:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.windows-amd64.exe
# Wed, 19 Jul 2023 20:16:32 GMT
ENV DOCKER_BUILDX_SHA256=d9419c0838c8a08c2da28fcee585f48926c4dd64e5be1d96eb55da12fa3332d9
# Wed, 19 Jul 2023 20:17:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 19 Jul 2023 20:17:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.2
# Wed, 19 Jul 2023 20:17:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-windows-x86_64.exe
# Wed, 19 Jul 2023 20:17:43 GMT
ENV DOCKER_COMPOSE_SHA256=d381f0697ce5d469917ab343dd4e59ae404865af8a5cf43178005bf400f0113a
# Wed, 19 Jul 2023 20:18:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb4cf79c2f4d846a90b33b635df0502f42d01fd0ee86b04449dfcec7cef5db`  
		Last Modified: Fri, 14 Jul 2023 00:39:45 GMT  
		Size: 230.5 KB (230461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159731638bc90a9f0bd35aa147c7caf45cb7eedcb01bb292fb2fe9fe1c81df14`  
		Last Modified: Fri, 14 Jul 2023 00:39:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7933132035cf06cc7c507dfffcc6e08c422ba49068d439e68b4e3518a5f3e472`  
		Last Modified: Fri, 14 Jul 2023 00:39:43 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585570eecc23b6ccbefc5f252f9d21997cbc9c44063bed0822982b1430286a6`  
		Last Modified: Fri, 14 Jul 2023 00:39:46 GMT  
		Size: 17.6 MB (17620781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e81f6ad5ec77ec0d9f18479eecb1a1c6469a4ba4b4e41b4035d38691f7f067`  
		Last Modified: Wed, 19 Jul 2023 20:23:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ffffac37caaf7c72b6a9814bd773fa3d1eae8c49fba76aa1540da04bb0854f`  
		Last Modified: Wed, 19 Jul 2023 20:23:13 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fd0057eaa6356cc9a03fa2a582ce95ebe6db89bfaaa652471820934ec03e91`  
		Last Modified: Wed, 19 Jul 2023 20:23:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66006628cda2503d61769a962545ff3299b46e898eeb6d3098acffbd47e54d34`  
		Last Modified: Wed, 19 Jul 2023 20:23:16 GMT  
		Size: 17.9 MB (17902193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ac4ab4710c7d5a362ad4f78503260ea6aa5a33974b5b1a65ea458396d28eb`  
		Last Modified: Wed, 19 Jul 2023 20:23:11 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0ad3237ba114aaecb3549b2770ecd4c387ddd0ee2a8824221179be6c99e4a7`  
		Last Modified: Wed, 19 Jul 2023 20:23:11 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0507f893c8475505c4290226ca55659b8c7cf484ca66d96d3def78f50d0bac9a`  
		Last Modified: Wed, 19 Jul 2023 20:23:11 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468aa5ac71dd86e54323e6fc5ff2896d60b3c96ffb881268bde2e219ecbfd62b`  
		Last Modified: Wed, 19 Jul 2023 20:23:16 GMT  
		Size: 18.5 MB (18450473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
