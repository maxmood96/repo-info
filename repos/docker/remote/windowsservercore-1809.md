## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:88ee39cef259d3e5bae90a671a5f6187d0d1957b402a1d1536cb5e3b7ae162ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:b5dd4750d144f430411b5a053e3c7f4be958611c8fe8094584f9a8baaa39792d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2182148188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78587486f4896fc7829107252583ef85216072fd6b786fa83978197dc05887d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 25 Mar 2024 19:12:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Mar 2024 19:13:29 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 25 Mar 2024 19:13:30 GMT
ENV DOCKER_VERSION=26.0.0
# Mon, 25 Mar 2024 19:13:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.0.0.zip
# Mon, 25 Mar 2024 19:14:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 25 Mar 2024 19:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 25 Mar 2024 19:14:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 25 Mar 2024 19:14:03 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 25 Mar 2024 19:14:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 25 Mar 2024 19:14:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Mon, 25 Mar 2024 19:14:33 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-windows-x86_64.exe
# Mon, 25 Mar 2024 19:14:34 GMT
ENV DOCKER_COMPOSE_SHA256=0a9a63442f50b494e8c5b6b1af9da138d9dbbeab094e3076747a709a470bb9e9
# Mon, 25 Mar 2024 19:15:02 GMT
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
	-	`sha256:f659cda6b20f17f2c9e9847234b3d452e48fd8b0895d536c3c6b8182b2400dc4`  
		Last Modified: Mon, 25 Mar 2024 19:15:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa04adc232b5fd074a6eed6b9bbd08a1b177ab6e18e8205f61f55c5b4e19d046`  
		Last Modified: Mon, 25 Mar 2024 19:15:12 GMT  
		Size: 497.9 KB (497925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dcd7c950c87e6b0e157342369ad610c2c067d46d100db79d8ca2c60f5558e1`  
		Last Modified: Mon, 25 Mar 2024 19:15:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e96e7825a5b7d1ad9c64f422ee99e03d076c83784e177d10ffa630f6caf3a28`  
		Last Modified: Mon, 25 Mar 2024 19:15:11 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eedaae00513e8a55ac4bed441b831f7fa308cc74dbb8dd13fc0ee84968cb04`  
		Last Modified: Mon, 25 Mar 2024 19:15:13 GMT  
		Size: 18.2 MB (18166343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561214cff7099aed7bb88af0e44598d2762afc0136fc279d053c611872982491`  
		Last Modified: Mon, 25 Mar 2024 19:15:09 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1d8b797b19ee8c6b3d1d7b39603038a30bd834471c9af47a081fc10b8d95f2`  
		Last Modified: Mon, 25 Mar 2024 19:15:09 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8f000caa33a6328e4cbc681e908773d970d42177fa8a4fce4202a1813d5f1c`  
		Last Modified: Mon, 25 Mar 2024 19:15:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e0d7206c28583c769cbc6faa0c2ec15966036600271af114772d5984e130cd`  
		Last Modified: Mon, 25 Mar 2024 19:15:10 GMT  
		Size: 18.8 MB (18834011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff7b062ff9771931bc9d891be3958df2c39c5f2ad5c9111b0814c405889204c`  
		Last Modified: Mon, 25 Mar 2024 19:15:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95958bb684818083c113a35e2dbb0230a10cc3e4ee84a38ce321748560a1f90b`  
		Last Modified: Mon, 25 Mar 2024 19:15:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5903af2299127c1c3e900a998e524b6067d418f9bf191fd7b940dc532640bc27`  
		Last Modified: Mon, 25 Mar 2024 19:15:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf702861990f3ce1f4b8ca407b0603d92519b2318b1d26294e6658f493017c9`  
		Last Modified: Mon, 25 Mar 2024 19:15:10 GMT  
		Size: 19.5 MB (19538319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
