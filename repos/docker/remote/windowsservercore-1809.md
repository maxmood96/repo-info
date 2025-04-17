## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:f5e06cbcdb7db063f7dab01b77e2e1dcb06e7f3e436746d73a222ce321f61ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:bcd74492b1ee68fdde0f87b0a9b6814bbca42d32d967cb11004cbef60d035639
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227153334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84581e1a23e35c8de3113ff26fd88f62d0e602628c8cd58ee03a62fcdce18467`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Thu, 17 Apr 2025 18:31:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Apr 2025 18:31:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 17 Apr 2025 18:31:24 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 18:31:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Thu, 17 Apr 2025 18:31:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:31:36 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 18:31:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Thu, 17 Apr 2025 18:31:37 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Thu, 17 Apr 2025 18:31:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:31:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 18:31:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Thu, 17 Apr 2025 18:31:48 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Thu, 17 Apr 2025 18:31:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8cec22ad2de983d62030efd24464c141807b9f6915d0f0f5efc19aa3df277d`  
		Last Modified: Thu, 17 Apr 2025 18:32:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12d74cd4516ac985ae33ba8dc133b1a915729ae039411b910e6715ad648b93c`  
		Last Modified: Thu, 17 Apr 2025 18:32:08 GMT  
		Size: 341.1 KB (341132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b86cb3fe3d947bfa201407687c9bb3a9d16c136bdccfbd4b4eeeedf1ca4372`  
		Last Modified: Thu, 17 Apr 2025 18:32:06 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe0d90993ba40b9e47ad5d80df3ea46df28418a166ecfa7d82e0b54eec172f3`  
		Last Modified: Thu, 17 Apr 2025 18:32:06 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0807b17c9af7ec2cbf1985d0c7d2ebb7236dbf88d473cf6b7bb262767aaff932`  
		Last Modified: Thu, 17 Apr 2025 18:32:08 GMT  
		Size: 19.9 MB (19888760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a68aedb9a34383bbd109bba34dd250efd7e66479dd0a30d54ae4062c13621ce`  
		Last Modified: Thu, 17 Apr 2025 18:32:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4adeebc30daa59f684343fa4f7d21804987d2b8db3b36541228bc6498e5476`  
		Last Modified: Thu, 17 Apr 2025 18:32:04 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba68c46bdba8925c73b8c82b8186cc6d127a63b1fd51d6d973e22d73000b1523`  
		Last Modified: Thu, 17 Apr 2025 18:32:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bdf1948bacdde554adc9c3aeb38278ea4702cd4612d005692793de20ba9fa6`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 22.4 MB (22352511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3472b294423b0e0183b30f58ac079d5a6e7c4ea3c9a637e255056c4df0d7c7c9`  
		Last Modified: Thu, 17 Apr 2025 18:32:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd5db15b65cab065f4aa34f3336bcc535d28afca6bdb58a9735b5e23bd1e0b4`  
		Last Modified: Thu, 17 Apr 2025 18:32:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1aeafc6ea386121681e626599a0f5e77d802a162c1a453a8ddc2960c4f8b41`  
		Last Modified: Thu, 17 Apr 2025 18:32:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635a22ab2d08567f602e6329c17af8041ec90791331a2a4a31e816234ada1042`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 21.8 MB (21833454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
