## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:061a40406076ff8843375da449424a3c19052bb114078bab3189d8cb3d4cc72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
