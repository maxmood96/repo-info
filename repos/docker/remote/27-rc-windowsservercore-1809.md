## `docker:27-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:ecf1c56a28b25d113ced2925d0667196fe2be9e345a9e4828b57c0dd62a79134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27-rc-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:02ea4c56f0dd0160161d7edf05c76419dcddcf2c0378350db82c67f826a13a8f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778599927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6cc28a3ad16b452e70dd173bf9bbc76de69b94aa1bc43b60efcc5851d0be3c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 18 Sep 2024 17:56:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Sep 2024 17:57:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 18 Sep 2024 17:57:51 GMT
ENV DOCKER_VERSION=27.3.0-rc.2
# Wed, 18 Sep 2024 17:57:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.3.0-rc.2.zip
# Wed, 18 Sep 2024 17:58:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 18 Sep 2024 17:58:19 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 18 Sep 2024 17:58:19 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Wed, 18 Sep 2024 17:58:20 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Wed, 18 Sep 2024 17:58:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 18 Sep 2024 17:58:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Wed, 18 Sep 2024 17:58:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-windows-x86_64.exe
# Wed, 18 Sep 2024 17:58:40 GMT
ENV DOCKER_COMPOSE_SHA256=4eda107dc1f83a57116c57595d39e6a0ff63e696a52230ea277bd7fa7977c8d7
# Wed, 18 Sep 2024 17:58:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1da1847143c1d9e5f51d480db26165d7eaba01f769ff84b196348221bfa1464`  
		Last Modified: Wed, 18 Sep 2024 17:59:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f45a030a0c274b2e4ea314e0bb2794a4499f24dc5e77efa8b331c23ab1adff2`  
		Last Modified: Wed, 18 Sep 2024 17:59:01 GMT  
		Size: 342.7 KB (342749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f953e1a3e211ea514d8281be0fe5ca7124025c48c542ce23650a597d77dac685`  
		Last Modified: Wed, 18 Sep 2024 17:59:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173b7f2d933999dd8de6f2375eaa7781d787e5a4dbc1704ef2ad7f2c106cf1c8`  
		Last Modified: Wed, 18 Sep 2024 17:58:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1a9909af92fa980d988eb47e5eb90be136e76e95df44ff7cb978755f0bd047`  
		Last Modified: Wed, 18 Sep 2024 17:59:01 GMT  
		Size: 18.9 MB (18853791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d74a87ac599172d9e666c90d3833a7fd6c32a6046f1d04d6102461a9cb8c3d`  
		Last Modified: Wed, 18 Sep 2024 17:58:58 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57389420f3d591544414a8c48f8703c2999dd4f948bdc990dc71728fb3cdea7`  
		Last Modified: Wed, 18 Sep 2024 17:58:58 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6410a8d99dce13a8282111e4d0c8a2c79c8c23f919680048fe1ecb29d448abe0`  
		Last Modified: Wed, 18 Sep 2024 17:58:58 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6c0f4a3b85058084c5ea586f312018b7ef6480458b394d773d22edc71e099`  
		Last Modified: Wed, 18 Sep 2024 17:59:00 GMT  
		Size: 19.2 MB (19248898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f969afe10f6e0b971032245387c3ed1f9d90e5f30240b5b9d9e98d016c5dd5`  
		Last Modified: Wed, 18 Sep 2024 17:58:57 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85590fe849e48e6a26213277c2a98a7820eb7da36a5c8f523cc3f7992fd531a8`  
		Last Modified: Wed, 18 Sep 2024 17:58:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b591cc45ce9674d8a796a0f7cc6ee73aa5bc0333d2f0b8d28ef5f891a0c89`  
		Last Modified: Wed, 18 Sep 2024 17:58:57 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b411a4c539318dcf3a1424a9e4daf3a74acb99441319e30d95c83a1d9cafe6`  
		Last Modified: Wed, 18 Sep 2024 17:59:00 GMT  
		Size: 19.9 MB (19874232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
