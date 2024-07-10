## `docker:25-windowsservercore`

```console
$ docker pull docker@sha256:4741c9428e7579ef19a31e64e42849a22bcaefe5b7316b51f3a6df43c76f9399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `docker:25-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:02b56e44bc5be5b485dcb428fa1adec821c3f1b1c503bc34dd82bf480e3c87cf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2196759748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af019b5eefecc9079376df2126b8ab8c213fbd9dbaf5c6382ec29df4d893c15`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 17:10:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:10:59 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Jul 2024 17:10:59 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 10 Jul 2024 17:11:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Wed, 10 Jul 2024 17:11:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:11:10 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 10 Jul 2024 17:11:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Wed, 10 Jul 2024 17:11:11 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Wed, 10 Jul 2024 17:11:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:11:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Wed, 10 Jul 2024 17:11:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Wed, 10 Jul 2024 17:11:20 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Wed, 10 Jul 2024 17:11:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b74f68c4938e7ff57f6604e0e030c3c28800b5e0ef9e081a466b4825bceb04`  
		Last Modified: Wed, 10 Jul 2024 17:11:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1644c48be4224d3dff2313824bc1eaa610fe24b342f7ff05788d19ce8024a2`  
		Last Modified: Wed, 10 Jul 2024 17:11:32 GMT  
		Size: 366.0 KB (366002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27110530f5b4f051e95bd1fc39e0e5eb4f33d77ecbc3fd3aa5b181ad67a400e`  
		Last Modified: Wed, 10 Jul 2024 17:11:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aa5c734bc33836cfa13e6f9f052773f2b929e5b212958a965c36eea6ad4bac`  
		Last Modified: Wed, 10 Jul 2024 17:11:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7786834cd4249b55f5994f4e534bce08c9b1fd39503acfe5ded65c1a678cb1b4`  
		Last Modified: Wed, 10 Jul 2024 17:11:32 GMT  
		Size: 18.1 MB (18081324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5ff667b4d8c7fca58e1648e22d58d09853918e24c33ced1e2a7db0ca7fad63`  
		Last Modified: Wed, 10 Jul 2024 17:11:30 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1099e6bd49626840a02e96dd68221957bb288fd70dc928b691c7836d25c3f6d6`  
		Last Modified: Wed, 10 Jul 2024 17:11:30 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89156bf3fb91988bfb3abb98a012739cd552b5d372a18cf12db5cca9c72d681`  
		Last Modified: Wed, 10 Jul 2024 17:11:30 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fc8f38452598d7e9f6cd14dfe954f6fc1cc456f25ad08be0bc35db210d9be7`  
		Last Modified: Wed, 10 Jul 2024 17:11:32 GMT  
		Size: 19.0 MB (19033191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fe4efa2a4983dab58d221f9cd007de1e68b620e5c0ce6fc908f16b6bb490e8`  
		Last Modified: Wed, 10 Jul 2024 17:11:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9991607cf91454884f0104af1f2dd4270b89eaf4bbec9bf07d21f74be38656`  
		Last Modified: Wed, 10 Jul 2024 17:11:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae2f63cea90617d6bee30f02be94cbaefff424098717a6912c4ec6e11614830`  
		Last Modified: Wed, 10 Jul 2024 17:11:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6ef700d84b18c701b905ab7136d5252b095d549c8de05d61dbd443623c2428`  
		Last Modified: Wed, 10 Jul 2024 17:11:31 GMT  
		Size: 19.7 MB (19667324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:7675d6f0057bfdae1ddc60d534479636005599aea7959fb655cd1271a625fd60
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295776383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e04e3f39bbbb315397aed3db4533392b74e0ceb860578a1ed509e790880f7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:26:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:28:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Jul 2024 17:28:31 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 10 Jul 2024 17:28:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Wed, 10 Jul 2024 17:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:29:01 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 10 Jul 2024 17:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Wed, 10 Jul 2024 17:29:02 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Wed, 10 Jul 2024 17:29:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:29:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Wed, 10 Jul 2024 17:29:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Wed, 10 Jul 2024 17:29:30 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Wed, 10 Jul 2024 17:29:54 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8f66fd22cdc8f3e3bfe3a847647973e79cc34369e8bee7c69523dbc0112dcf`  
		Last Modified: Wed, 10 Jul 2024 17:30:06 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c7fc8a462e2b6f38eb274fac3eb308131772dbc09518f7b79997167155edfe`  
		Last Modified: Wed, 10 Jul 2024 17:30:05 GMT  
		Size: 508.8 KB (508764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec2fdb374d819425578056e973ff63ab24fe14b6ba377fe8ed89a4d008a55d8`  
		Last Modified: Wed, 10 Jul 2024 17:30:04 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf25cdf1e191d05e385398bd7e9e19f56b39c7293e516eaee73fa978a2c924f1`  
		Last Modified: Wed, 10 Jul 2024 17:30:03 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fc2bef58f81a34b232d166796cb7e544780ddd2662007a6aa5ae3ce88f5db2`  
		Last Modified: Wed, 10 Jul 2024 17:30:05 GMT  
		Size: 18.1 MB (18097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f0114cf26515a1f57187b2ebe52512b79f55de515e792892e055d255832c9`  
		Last Modified: Wed, 10 Jul 2024 17:30:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dc6dbad2aae3ade89ad9b4fdaae1c4ff05ceb09a1f19fea0acaa3174efe76c`  
		Last Modified: Wed, 10 Jul 2024 17:30:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d6791a7062a05ffdb7cddfc00b3bc970a48cb197f03c1472e60e32953abb4`  
		Last Modified: Wed, 10 Jul 2024 17:30:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3d161e348ac0623b3f4ffa87675a6229b57e00e6212438de67e67ab3f72ba`  
		Last Modified: Wed, 10 Jul 2024 17:30:06 GMT  
		Size: 19.0 MB (19047543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4005b74d7caf94ce8aee5956ee03c53742e5c5c5c638c3db6708e183fd613277`  
		Last Modified: Wed, 10 Jul 2024 17:29:58 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012569641b4a166a91ca17d2b91f10305c188b72f2bac87f5f80014763ebc656`  
		Last Modified: Wed, 10 Jul 2024 17:29:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7d9dd27270c9a0acc020a8d8cb0e7f784a473b9052d6b4fbeb137b369b5af2`  
		Last Modified: Wed, 10 Jul 2024 17:29:59 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c625853f49d1b25c131e0faf0115aee786e9ebbeecb59806a5829c49cdcc363`  
		Last Modified: Wed, 10 Jul 2024 17:30:02 GMT  
		Size: 19.7 MB (19681065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
