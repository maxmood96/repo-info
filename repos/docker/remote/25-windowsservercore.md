## `docker:25-windowsservercore`

```console
$ docker pull docker@sha256:8427f6a2143715ceb9f71cfd19cf4eda1f81119f015953b67ab90b8206d59815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `docker:25-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:3406e198b0747bd2f12027b5a893f874f040f45fee43c78cb54e06d35b2eaf3d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2196995321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb9f27a4ddaa3c0f44ae251b9c6f2957ee0cee582a07f20c3317a2605fbd9ed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 12 Jul 2024 01:12:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 01:12:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Jul 2024 01:12:46 GMT
ENV DOCKER_VERSION=25.0.5
# Fri, 12 Jul 2024 01:12:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Fri, 12 Jul 2024 01:12:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:12:59 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Fri, 12 Jul 2024 01:12:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Fri, 12 Jul 2024 01:13:00 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Fri, 12 Jul 2024 01:13:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:13:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Fri, 12 Jul 2024 01:13:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Fri, 12 Jul 2024 01:13:10 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Fri, 12 Jul 2024 01:13:19 GMT
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
	-	`sha256:f5a667083bf6f2448e39c9c063f6d9e6b3b8fd6e52d87e1e377ad4e1a54f933c`  
		Last Modified: Fri, 12 Jul 2024 01:13:24 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96f7f36533e1b9816c310cfa048335bc1d7172bea4d8a70d79930a041d195cb`  
		Last Modified: Fri, 12 Jul 2024 01:13:24 GMT  
		Size: 367.2 KB (367172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27caf5819cd6702bdb0ac5481d212e97ec1839579e17d6f4baf7d4368bd2e4c`  
		Last Modified: Fri, 12 Jul 2024 01:13:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8195c1ccc64776651675dfb8efbce45a6fc7f0126b1cd3f3f2189c8dab86b066`  
		Last Modified: Fri, 12 Jul 2024 01:13:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3a5e355126b85d430910117482a87edff85852e9ca02b817a03fb7d6e10ade`  
		Last Modified: Fri, 12 Jul 2024 01:13:25 GMT  
		Size: 18.1 MB (18081696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0289532f6b8803f22d451a28de39cb4a23b5981f3e6d768c21087eaa572b686f`  
		Last Modified: Fri, 12 Jul 2024 01:13:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1339197f3770346891e7e4bfe5301f7ada696fc3625a292fa540e8524c76039`  
		Last Modified: Fri, 12 Jul 2024 01:13:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60737d950c0e65ba6109a99f4a6550706d48ea056fc8aa7065d5c27e4fa5fea8`  
		Last Modified: Fri, 12 Jul 2024 01:13:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8436ea21a1406c86146c86cc8aa2d03d4038ad355a5bf663f200dc93488b52d1`  
		Last Modified: Fri, 12 Jul 2024 01:13:24 GMT  
		Size: 19.3 MB (19266180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca696084a9beafb9b522c39275e7752969bda490e5151aed7315f28ce39628e0`  
		Last Modified: Fri, 12 Jul 2024 01:13:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a934027c02dc7bc570635ce922f76a77026e86f3d5c90e544b4a2e645045595`  
		Last Modified: Fri, 12 Jul 2024 01:13:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7963dd93b3d16a901063da13675ce65d62327ef147233875000b018d0fffd9`  
		Last Modified: Fri, 12 Jul 2024 01:13:21 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304326ee82c224be661d085b574e00ea5495d65f995535dde34c9a0768760c25`  
		Last Modified: Fri, 12 Jul 2024 01:13:24 GMT  
		Size: 19.7 MB (19668320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:9c581ea97dcc7e5ace903011cc724cd0b71b3d1d0fb366cba18e3a99c47addcd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295965443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc044ba31f5999f1a8965e87d717e5df9f52ab6030e83abda79503aca18bb77b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 12 Jul 2024 00:59:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 01:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Jul 2024 01:00:12 GMT
ENV DOCKER_VERSION=25.0.5
# Fri, 12 Jul 2024 01:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Fri, 12 Jul 2024 01:00:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:00:38 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Fri, 12 Jul 2024 01:00:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Fri, 12 Jul 2024 01:00:40 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Fri, 12 Jul 2024 01:01:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:01:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Fri, 12 Jul 2024 01:01:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Fri, 12 Jul 2024 01:01:06 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Fri, 12 Jul 2024 01:01:30 GMT
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
	-	`sha256:77e721b5a8b0c838983c9383c0fbf02b28498e6fa70cb554530acda331e6a030`  
		Last Modified: Fri, 12 Jul 2024 01:01:40 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30fc7349f023d1703cda4efa150185164e262d5cb08ed8b9cd66fa29d696fd16`  
		Last Modified: Fri, 12 Jul 2024 01:01:40 GMT  
		Size: 497.8 KB (497765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681580dd61f0b705fff88fc6bc8b1437d055dffaf1817f94d0011944a1cf6127`  
		Last Modified: Fri, 12 Jul 2024 01:01:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0caad0c6f874e44b773491b4fb1db7ca2ae0ebcfeee05121e555597c34812`  
		Last Modified: Fri, 12 Jul 2024 01:01:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c4bc688d8f086b2f1d1fd2b0662895b0d373862dba580006f17cd0d8057f8a`  
		Last Modified: Fri, 12 Jul 2024 01:01:40 GMT  
		Size: 18.1 MB (18087344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7942b118b4baaca5b2f5f1ab3f8a540faa45f5ee5e7ce236142c1f2c149d3868`  
		Last Modified: Fri, 12 Jul 2024 01:01:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529051f8750e97f44e0aa518ec0884f0bcdccb729b5bfabfc4392c04a4737b87`  
		Last Modified: Fri, 12 Jul 2024 01:01:36 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3f713ba9f686012af956e315672874ded0c87c4ea9fbc6861dacc6c3c8bf77`  
		Last Modified: Fri, 12 Jul 2024 01:01:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3497f846ac15318f926d01da84a44b846ca13edec2a57743aad2c07e0f946856`  
		Last Modified: Fri, 12 Jul 2024 01:01:38 GMT  
		Size: 19.3 MB (19269018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a55fb36cfd5e2ef7405fed7655ac7bf2ab5dde7fa49c89af045df2425f05b7`  
		Last Modified: Fri, 12 Jul 2024 01:01:35 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ddb4637f247667f247ff052a6673f3050100bd0532af7d0469468301942edb`  
		Last Modified: Fri, 12 Jul 2024 01:01:35 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3918c7fa7d01e12b6bc5acac8c8cd54a114e8379e6e312cf10a6a822bec97ca3`  
		Last Modified: Fri, 12 Jul 2024 01:01:35 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df163b94d09ec2f26e1a4e9e920ee06a3f3f29550d032dfee8d005f6b208136`  
		Last Modified: Fri, 12 Jul 2024 01:01:38 GMT  
		Size: 19.7 MB (19670213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
