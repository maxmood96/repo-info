## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fccccf96f59c1b8f28e7403434c83676fd2918545b80fc004f6813a8b97e16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:4d51f373dd2a4426a1fe2dc4967a42e90a0a2c22216d9f68feffdc36302b2e1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2126278412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8971f266b87258d9fea7ed23e99b1644fc2244c0e02ad6d1188812c524886f54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 20 Apr 2026 23:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:03:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:03:10 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:03:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:19 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:03:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:03:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:03:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f4559ccd19990eeb3eb464a5c03f7c8bd4e42fc037cc850c7dc5d79bf1767`  
		Last Modified: Mon, 20 Apr 2026 23:03:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8680fed5217e07032ae763bb4814082de2b6871eea99f7bcf4be6fb17dfd79f4`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 502.1 KB (502095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542cbb5df10cc920a089a68af1d0f860484ef70c9d225a612dcf5ada2aaef390`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88dd0729e80918b82e555dffd716238e73e864506f572bbbd0a8d756ec675bf`  
		Last Modified: Mon, 20 Apr 2026 23:03:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7176f52dbf05c4190cc72cf02fbe31e6539e8dcb732de302e9ebfd1e551f86`  
		Last Modified: Mon, 20 Apr 2026 23:03:47 GMT  
		Size: 20.2 MB (20193395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30381a09bd7e612f87bec4de2b1d777841f1d46d5ba73d38f9cced6f9b8115e4`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210f368239bd3baeaccf30803eaeec62843562f847f4f963141670c760522e87`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806603dc9170bc3b136c2941f1e2a772ccfaa85ee9aef9c22b08a74e983edb3e`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ec0ed78a357c0c8f98fc6487d30563e9d8a03db4def9807966493cbf91e4ec`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 23.4 MB (23434006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3950ad53b54530338b85e919a0e803046bdb1e51c7437915640748a7a11e53`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab184fdff530ee113fb07a551306f51ac338c1ac6d707c5e5ada12e7f3a9c3`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0306647508616ca419bbaf30c1bc7c5cb266e7dacac4b59856274b4243e01`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d91cba3e753e1dc5b702a3c5be5695fcc7d24a8cd552f8c620fb10598c4cbb3`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 11.9 MB (11925928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
