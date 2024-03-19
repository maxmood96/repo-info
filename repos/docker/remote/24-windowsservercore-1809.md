## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:ea868ecd5eb86e40bcf2ce105f1e50b79abf3843f88c286fff6d70fff1bdc58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:3257df4ab35e9b00cff355affe9afe0e7bdfb6624a9e7dbc698f57865239a8ee
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181041512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf878c9b9373ab48ffe5319355b2103b74ccfa90fef1b19019a85a19a8808617`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 18 Mar 2024 23:13:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Mar 2024 23:15:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Mar 2024 23:15:38 GMT
ENV DOCKER_VERSION=24.0.9
# Mon, 18 Mar 2024 23:15:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Mon, 18 Mar 2024 23:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 18 Mar 2024 23:16:11 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 18 Mar 2024 23:16:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 18 Mar 2024 23:16:13 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 18 Mar 2024 23:16:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 18 Mar 2024 23:16:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Mon, 18 Mar 2024 23:16:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-windows-x86_64.exe
# Mon, 18 Mar 2024 23:16:39 GMT
ENV DOCKER_COMPOSE_SHA256=27289c82fe3ee64eaa415ae47f028f7c6af6ab347f1af4fde0e0d7d2b4a84dbb
# Mon, 18 Mar 2024 23:17:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8434e714d0018ce0747589be4531ceefa11cd4f50982749d8895f9de1dae07a4`  
		Last Modified: Mon, 18 Mar 2024 23:17:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ed2e372af475f2dba095c5806b99e3158fc95353dfccb4706c7a4fedb5647`  
		Last Modified: Mon, 18 Mar 2024 23:17:14 GMT  
		Size: 486.2 KB (486208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5789c7f6f23629bd8e0214f48eab04415a4cb0f65f0cb6ec954564d24ebd66cc`  
		Last Modified: Mon, 18 Mar 2024 23:17:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a287b9d235b83213cd7316c70ba1cf6bdd7c4512f31effa7aba4613eadf4c`  
		Last Modified: Mon, 18 Mar 2024 23:17:13 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5672de2a6c6e2e991a9d8a1e186bec4382a7a81208d195b9342e74938c271e7b`  
		Last Modified: Mon, 18 Mar 2024 23:17:14 GMT  
		Size: 17.5 MB (17534659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e890838d2a23f5b543db8b56056d977831aa77bf45ea9a4415790f8ba3d7a884`  
		Last Modified: Mon, 18 Mar 2024 23:17:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1c74b3b924615c108c155a998de9355adce5a43c55ac189db8951c14238da5`  
		Last Modified: Mon, 18 Mar 2024 23:17:11 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71db82313fa17068355ae74062857119ef4b4a60f2f553ab1eac86a3ef87b9d`  
		Last Modified: Mon, 18 Mar 2024 23:17:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6724dd37f93f3481b5e16365a0f9b57e94de1db453b504500ef14b61d8bcfdd`  
		Last Modified: Mon, 18 Mar 2024 23:17:12 GMT  
		Size: 18.8 MB (18831659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16489c01600cdd3099c5000e3728546f26a6ad386e5abbaae6fadbea35bcd105`  
		Last Modified: Mon, 18 Mar 2024 23:17:09 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c7fee413751e8019adcffbd5fb3de1350fa2e93100edb15e2317ba11485c21`  
		Last Modified: Mon, 18 Mar 2024 23:17:09 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe7126d052b05a3e2113cf1cdbb2a0604891df06a493f4769bb270298d023f`  
		Last Modified: Mon, 18 Mar 2024 23:17:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccccd9dbdfa2e6449bcf7f68dda252a75b25938f74989bc953e99aaf05e2c30`  
		Last Modified: Mon, 18 Mar 2024 23:17:12 GMT  
		Size: 19.1 MB (19077397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
