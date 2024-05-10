## `docker:windowsservercore`

```console
$ docker pull docker@sha256:f35712f120909a03f643fb0e623419340553911f071b1a1753fcb2f65eda15ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull docker@sha256:158e9911e0f722f538846fdf4d35e4e35f141e43f9395e6637ed764526532e82
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2057591766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d29cb950bb740732153a87606dd2fc41459216f499c0affe0eb5e8e3ad8778`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Thu, 09 May 2024 23:52:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 May 2024 23:53:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 09 May 2024 23:53:24 GMT
ENV DOCKER_VERSION=26.1.2
# Thu, 09 May 2024 23:53:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.2.zip
# Thu, 09 May 2024 23:53:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 09 May 2024 23:53:45 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Thu, 09 May 2024 23:53:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Thu, 09 May 2024 23:53:46 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Thu, 09 May 2024 23:53:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 09 May 2024 23:54:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Thu, 09 May 2024 23:54:00 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Thu, 09 May 2024 23:54:01 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Thu, 09 May 2024 23:54:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d1c96afe651885fd5c1ba5213fcc679e9cf649ff72a993510891cd181819c`  
		Last Modified: Thu, 09 May 2024 23:54:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa45a7d28f17b2ee2d4515f57150bccecbf3fd945a2f5c51c5be6c609511761`  
		Last Modified: Thu, 09 May 2024 23:54:16 GMT  
		Size: 500.5 KB (500520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3d050926b3da8a050c5fa00f391cfa1866633bd713995fa96b09fe7203d611`  
		Last Modified: Thu, 09 May 2024 23:54:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff167efc2054b8ac6d379b9d5d7a12a5cf8c64aab88f203002e938fbf3425fe`  
		Last Modified: Thu, 09 May 2024 23:54:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e9fe98ac61872bd5e55fbfe7cd47fa444cf40efa5d3d81ea9095ccfa77b433`  
		Last Modified: Thu, 09 May 2024 23:54:16 GMT  
		Size: 19.2 MB (19204663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac3e2688d91b3cc1193db57cc96ab70b0a835591dcb67f1ad4a44d7a3811215`  
		Last Modified: Thu, 09 May 2024 23:54:14 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55341319b320c9801097b0afcb21835b186b79cf5f11bfa642fa6d532c153573`  
		Last Modified: Thu, 09 May 2024 23:54:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b172ad310542cccec28a9a5b89538ca31d9fcd59743a263725df8d1e97f9de`  
		Last Modified: Thu, 09 May 2024 23:54:13 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d09a308f78ca35df2fdc9f9f85ef5df4f2981c8ae927397f715d61f05bd046`  
		Last Modified: Thu, 09 May 2024 23:54:15 GMT  
		Size: 18.9 MB (18895157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb92832b11f7234cfbe67b79a3310e74f45d860e87fbcf3354bb6472acf126ee`  
		Last Modified: Thu, 09 May 2024 23:54:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0324918e11a7fbd82a91b3b5baa96e54085b4e18efcd104ef566bdb6a518527`  
		Last Modified: Thu, 09 May 2024 23:54:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3f1d264023da4714bc360a07a108a6e2405b424ccb44adf02745c1cb2ae89f`  
		Last Modified: Thu, 09 May 2024 23:54:12 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce18fb9d48be00e96cf90eb9b28d1c92b9614aaabdd85736087b6bc03179888d`  
		Last Modified: Thu, 09 May 2024 23:54:15 GMT  
		Size: 19.6 MB (19606173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull docker@sha256:452596ac13dbd7d4f6c65605cf82f32a47b2cd6187d5a78ad42e4854d14339cf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2222725191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4bc48b67e8bd2c89e6f3691de391134cb0d023f725c6020e6d48f4729c7403`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Thu, 09 May 2024 23:52:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 May 2024 23:53:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 09 May 2024 23:53:53 GMT
ENV DOCKER_VERSION=26.1.2
# Thu, 09 May 2024 23:53:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.2.zip
# Thu, 09 May 2024 23:54:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 09 May 2024 23:54:26 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Thu, 09 May 2024 23:54:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Thu, 09 May 2024 23:54:27 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Thu, 09 May 2024 23:54:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 09 May 2024 23:54:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Thu, 09 May 2024 23:54:55 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Thu, 09 May 2024 23:54:55 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Thu, 09 May 2024 23:55:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ca6f089ab87bde1c77ca2d7956e39cff438ffa028eea066bca2cd4f76e872c`  
		Last Modified: Thu, 09 May 2024 23:55:31 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfde717a973c1730a0fcc7153725defe34b47ace7a249f76bf0e92089f4f3c0c`  
		Last Modified: Thu, 09 May 2024 23:55:31 GMT  
		Size: 495.5 KB (495523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d940bfa5d6e2647bd24272fbc58d8efacebc5667f49a05fcc2d9680e839957cb`  
		Last Modified: Thu, 09 May 2024 23:55:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595d788c38d3bc3d93f1f1a37e61152a4faa8acfdce08240f742eb6e0064698e`  
		Last Modified: Thu, 09 May 2024 23:55:30 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd09c798082ad658e6cd467b8aebc208fae76afc000bd0371f92e956a8d5f4a7`  
		Last Modified: Thu, 09 May 2024 23:55:32 GMT  
		Size: 19.2 MB (19236432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23f02870bfd29a22fc14b0cd742dfa3362afb90a15478450317ad482afe94ae`  
		Last Modified: Thu, 09 May 2024 23:55:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb5f4effd21f0064cb2e0e6647b22e680e741679ab583cb4aa88b286935fa0d`  
		Last Modified: Thu, 09 May 2024 23:55:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71553f9bbdee18037a99bf799e067693f19008dbc57a105433e23f6ac2042af`  
		Last Modified: Thu, 09 May 2024 23:55:28 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd3175a30d3365afe60d31ab6cd3db4945c7698446f061ec8d9c88eba93933c`  
		Last Modified: Thu, 09 May 2024 23:55:29 GMT  
		Size: 18.9 MB (18924701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9231ec6d189af93a493b67694f635f9e79a2bcd7207ac587dfdb2d9c123456`  
		Last Modified: Thu, 09 May 2024 23:55:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2577d113c2b3087c1ed71d43f31082c2bb562ad4fbe1aa7497d18e0cf2cec392`  
		Last Modified: Thu, 09 May 2024 23:55:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00447492ee145548d780941063294eeadd03e3b56063b2e488dda9a84135e12`  
		Last Modified: Thu, 09 May 2024 23:55:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce2d1b3938e06ce30dec331e8eb1d0d6446d449ea63cb48e2f272fcee2e42c4`  
		Last Modified: Thu, 09 May 2024 23:55:28 GMT  
		Size: 19.6 MB (19628916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
