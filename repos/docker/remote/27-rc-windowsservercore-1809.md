## `docker:27-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:728f7eece15a911d9bb1bb4130d674068aff46fa6756aeaeba0b3b4029df122f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27-rc-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:f3996d50288e806836f5e59fd6ce881fb50fcf430708b71659a997e73b416892
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778638092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f34e6406a2db1c2f8bc167c8bb63a44e11a0bcf6f2e65110d934678472aa0d9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Mon, 16 Sep 2024 19:02:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 19:03:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 16 Sep 2024 19:03:00 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Mon, 16 Sep 2024 19:03:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.3.0-rc.1.zip
# Mon, 16 Sep 2024 19:03:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 16 Sep 2024 19:03:15 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 19:03:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Mon, 16 Sep 2024 19:03:16 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Mon, 16 Sep 2024 19:03:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 16 Sep 2024 19:03:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 19:03:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-windows-x86_64.exe
# Mon, 16 Sep 2024 19:03:37 GMT
ENV DOCKER_COMPOSE_SHA256=ae793808ae7cb326b2a20a35b1ff66022bf05d9a80bb08822f4455bbb44ff2c8
# Mon, 16 Sep 2024 19:03:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c376d22903b7070a5a4350354333125a5351d29a0db44600e6c7207a80fed68`  
		Last Modified: Mon, 16 Sep 2024 19:04:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb469f23853c16b1fa73b520e78bae0604139c53e75dabdb02049d29eb325abc`  
		Last Modified: Mon, 16 Sep 2024 19:04:06 GMT  
		Size: 325.9 KB (325922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0cabd486087bd1d2137289761a79120cd407d25d29b0781de346151cf0b70`  
		Last Modified: Mon, 16 Sep 2024 19:04:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a364502e8c1ffa6be358cda8b9ccbb216ccb1b7488e5601409046f5525ea857`  
		Last Modified: Mon, 16 Sep 2024 19:04:05 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e562170fb27dd9602ad25c125b24a5375ea6782297f22544591a12c76928680`  
		Last Modified: Mon, 16 Sep 2024 19:04:07 GMT  
		Size: 18.9 MB (18873531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce499e6ebf9e56648b7ce62e1827ea1026596c8bbe3dc79b18a7e0cfb095ca77`  
		Last Modified: Mon, 16 Sep 2024 19:04:03 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd2dedb1f2ad68a9f01218d08900508e08e6895ac187d2c617283db88d1576c`  
		Last Modified: Mon, 16 Sep 2024 19:04:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b533e14983108adab48d3434dd8c272f0f01d6bfcf0f4d853322acf2347eb2`  
		Last Modified: Mon, 16 Sep 2024 19:04:03 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a4bdfc6dabc27a797dd31ac28cd16c708145be4b20fe24f0fdc7d315d2479`  
		Last Modified: Mon, 16 Sep 2024 19:04:04 GMT  
		Size: 19.3 MB (19265182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07170660b5c05db5af1978e0831450c2605814a1326aa00eb4191b6c8eeb644d`  
		Last Modified: Mon, 16 Sep 2024 19:04:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05858e66b55dee918f91b132c1d3d5f30bdc1519c72337ebabd602d20c48012d`  
		Last Modified: Mon, 16 Sep 2024 19:04:01 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f23232b000b94e0c8ad0e2fbde69a179559dfef86476e88632584dcfb4266`  
		Last Modified: Mon, 16 Sep 2024 19:04:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd093089710627ff66e8965bfddb86b7e040c5797fcf10471f54af50c8f4bde`  
		Last Modified: Mon, 16 Sep 2024 19:04:04 GMT  
		Size: 19.9 MB (19893281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
