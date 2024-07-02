## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:7e5b86108008d2277460f0b97a6c50c2ec7cf3e3c4b3915186f031346fb391da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:de583fca5903824418764496f4b3d23a32743447c812574b7c2187b6e597943d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279270318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8d17fe0e905412571b8c991d350d8ec207e6fbcc357137d647eeb975bcb810`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Tue, 02 Jul 2024 00:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:57:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jul 2024 00:57:58 GMT
ENV DOCKER_VERSION=27.0.3
# Tue, 02 Jul 2024 00:57:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Tue, 02 Jul 2024 00:58:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Jul 2024 00:58:26 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Tue, 02 Jul 2024 00:58:27 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Tue, 02 Jul 2024 00:58:27 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Tue, 02 Jul 2024 00:58:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Jul 2024 00:58:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Tue, 02 Jul 2024 00:58:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Tue, 02 Jul 2024 00:58:55 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Tue, 02 Jul 2024 00:59:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648e6774bf46a9570bbba378b813fe331d77e66794c67902533f033b386728e`  
		Last Modified: Tue, 02 Jul 2024 00:59:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3fcc6425991dc3ce2445421b81212fb560bf82676f44aff7da17c49d47334`  
		Last Modified: Tue, 02 Jul 2024 00:59:30 GMT  
		Size: 520.2 KB (520190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f3c0de4a441d13b67c7760d3d5964ae2a802a783ea1c33abe17ae803f105ae`  
		Last Modified: Tue, 02 Jul 2024 00:59:29 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec26b725989766448acd89453f905f1de1518029bf71abdf4803f36cd84643d`  
		Last Modified: Tue, 02 Jul 2024 00:59:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7e003b86bfd7f0b7560ef36ecbfc36ff7e261ec42b881dd2c77b342a47d95f`  
		Last Modified: Tue, 02 Jul 2024 00:59:30 GMT  
		Size: 19.3 MB (19306268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d273972d44fcdaf4a62d5ba6f75b7dfb129b6a5634e795d5e53dd4af1e8d50`  
		Last Modified: Tue, 02 Jul 2024 00:59:27 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23fbd9e8a5b8f3c5aaca6c9f4fe9898ad5c65969c8fd927159155c77b48bf`  
		Last Modified: Tue, 02 Jul 2024 00:59:27 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a33926f7fa4801cf9081a1007897725e622157b1eb31f11d623afceeade55a5`  
		Last Modified: Tue, 02 Jul 2024 00:59:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a822a40a60c40e379ab50a488875bc36d4586634087977a5816e69a5a422a50b`  
		Last Modified: Tue, 02 Jul 2024 00:59:27 GMT  
		Size: 19.1 MB (19058739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1fb193ed6f352bda7f667cdff053767018b6df0cd23bc0029741f6b64e41db`  
		Last Modified: Tue, 02 Jul 2024 00:59:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2d5334344610097bb8a4357b1d726019275b762d0f99b3062984d32c01ef48`  
		Last Modified: Tue, 02 Jul 2024 00:59:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1475a6c6bc70b770326361808bfc373c55fe283aa59fed6344fd458549085a58`  
		Last Modified: Tue, 02 Jul 2024 00:59:25 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe81dc3136381a8ec2c380d5e1c828c7fcba447c55c88de44ebd93b07a1cf5`  
		Last Modified: Tue, 02 Jul 2024 00:59:28 GMT  
		Size: 19.7 MB (19692275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
