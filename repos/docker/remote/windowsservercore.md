## `docker:windowsservercore`

```console
$ docker pull docker@sha256:7c2aaa01e206e815db7d85984b9efd624f52384562eae39e4bb83adae293dfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:f3fe3baab48a4a189bdf59d8080e690502d69d660116c2d5f521c0917908ad35
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955737955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d0a13b9d5ba521cf92a598bc65eb9b719c18a2f59b39bc9a5d99bf68ebd701`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Mon, 22 Jan 2024 22:50:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jan 2024 22:51:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 22 Jan 2024 22:51:02 GMT
ENV DOCKER_VERSION=25.0.0
# Mon, 22 Jan 2024 22:51:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.0.zip
# Mon, 22 Jan 2024 22:51:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 22 Jan 2024 22:51:20 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Mon, 22 Jan 2024 22:51:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Mon, 22 Jan 2024 22:51:22 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Mon, 22 Jan 2024 22:51:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 22 Jan 2024 22:51:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Mon, 22 Jan 2024 22:51:31 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-windows-x86_64.exe
# Mon, 22 Jan 2024 22:51:32 GMT
ENV DOCKER_COMPOSE_SHA256=8402473653066beefdd602acb227f399cdae11a328ac3ca5feead826992c31b0
# Mon, 22 Jan 2024 22:51:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286583bf56fa50789056d8a02f3dc0dd67cd0def063b44e2c77564da06c3aef1`  
		Last Modified: Mon, 22 Jan 2024 22:51:48 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b18ffe1ffbe1b4e456e25e33a39bced048d8b9bc79fcb64d2db02c2cd6c1a60`  
		Last Modified: Mon, 22 Jan 2024 22:51:46 GMT  
		Size: 494.2 KB (494151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e609a1bdda12234f14169c249bf6ffa986d7a37824008382f934aeeb3ed6e1`  
		Last Modified: Mon, 22 Jan 2024 22:51:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc98855ab0781e25e5299ccd90e65627c0de1be786fd33c0974972786d39118b`  
		Last Modified: Mon, 22 Jan 2024 22:51:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7234434ccc234be8349a6c0719323cad1bd8d05025e1399688a4c9e847ee224`  
		Last Modified: Mon, 22 Jan 2024 22:51:49 GMT  
		Size: 18.0 MB (18034122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1016c688669888e366c0f76849a9423cbd3bb75ffa605250c867cfb963e6a6`  
		Last Modified: Mon, 22 Jan 2024 22:51:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454640a3dfc0137f4edf2f7b6aab5430d3a04b3fceda99d28f3d7e8857fe3903`  
		Last Modified: Mon, 22 Jan 2024 22:51:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9e3dd7abb7cd6390c50dddcd94edd62ec9552bfebfb94d31b67e6a09a617e`  
		Last Modified: Mon, 22 Jan 2024 22:51:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b036fcf586a75ff21f05ec169fc370877cc8783c70ca7ce45b1d6b7ad18a2e7`  
		Last Modified: Mon, 22 Jan 2024 22:51:46 GMT  
		Size: 18.0 MB (17985713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859f3989faf45d6435297b1eb310c5cfa48d98403975426b6246089a96701fd0`  
		Last Modified: Mon, 22 Jan 2024 22:51:43 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dd6fa2ffc7e3177b7e0f1a08acaff194a5ad365fae020448612952ef5ab006`  
		Last Modified: Mon, 22 Jan 2024 22:51:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985e94c8466f290505eb1ef487961c77536c08cece543f7266ae4e797242b5d1`  
		Last Modified: Mon, 22 Jan 2024 22:51:43 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724539e0a462212b06111308c4d7ac901dfe59114e006791d9b5964e0c19c39e`  
		Last Modified: Mon, 22 Jan 2024 22:51:46 GMT  
		Size: 19.0 MB (18999476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:ab4a97cd8380ae1cd9cc0c8ab993066d3e8e47777705204256cfbf3906e975fe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125353037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2d2c99eebf865ba28a71990f4982b28a0814647deb774ea379b52c98cd50c3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Mon, 22 Jan 2024 22:50:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jan 2024 22:52:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 22 Jan 2024 22:52:12 GMT
ENV DOCKER_VERSION=25.0.0
# Mon, 22 Jan 2024 22:52:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.0.zip
# Mon, 22 Jan 2024 22:52:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 22 Jan 2024 22:52:45 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Mon, 22 Jan 2024 22:52:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Mon, 22 Jan 2024 22:52:46 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Mon, 22 Jan 2024 22:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 22 Jan 2024 22:53:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Mon, 22 Jan 2024 22:53:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-windows-x86_64.exe
# Mon, 22 Jan 2024 22:53:15 GMT
ENV DOCKER_COMPOSE_SHA256=8402473653066beefdd602acb227f399cdae11a328ac3ca5feead826992c31b0
# Mon, 22 Jan 2024 22:53:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47363f71e543fb478a9482606c206f4e76cd7d28dbd116a06fb8e71339d2bf9`  
		Last Modified: Mon, 22 Jan 2024 22:53:46 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb2119bec5b851722d6b3c55fe17dc04fdf3507c456ac7a1150bd7ab1ff1a6d`  
		Last Modified: Mon, 22 Jan 2024 22:53:46 GMT  
		Size: 495.6 KB (495623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca6de571a58de9f6d3ac732a53e7d656e235a2bee772c28bb9b92f6604912e3`  
		Last Modified: Mon, 22 Jan 2024 22:53:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d815762b65020a0953a16725f012c70f95f1c81bdb37761449e7d0206d37a3`  
		Last Modified: Mon, 22 Jan 2024 22:53:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad8de3cf935d61b1300765d2c4a00e7cc69ba1e36dfb79c506319f763135686`  
		Last Modified: Mon, 22 Jan 2024 22:53:46 GMT  
		Size: 18.1 MB (18073396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3ac37b0b54f3a8ae7ddee759cf2597d3ebbb7a7363764d1f2118422adc1f03`  
		Last Modified: Mon, 22 Jan 2024 22:53:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3822c15a2c9fcbae2ff1830c21e31368ab1ba5785691ae3a269587f4d44f7d0d`  
		Last Modified: Mon, 22 Jan 2024 22:53:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b749f174c04f066fff7f5c0f8e9063b4493d209aac2704875d1ec61cfbbdef60`  
		Last Modified: Mon, 22 Jan 2024 22:53:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0353c9f5fa97580a34bf0568bfbcf94bad190cb59faf5ab36320d0760bd5951`  
		Last Modified: Mon, 22 Jan 2024 22:53:44 GMT  
		Size: 18.0 MB (18021145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca982914410b15f290e9c446d215e0798e75db03fa7b18491b2275ec6e0d0f8`  
		Last Modified: Mon, 22 Jan 2024 22:53:42 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700d3ff423bfe0ca3e9610620e32c02022d75fc43a19634b52c81e58930aed04`  
		Last Modified: Mon, 22 Jan 2024 22:53:42 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a923b41150d11a31159e82fb82c50545465797aee32367cff1e05f64acbfa7`  
		Last Modified: Mon, 22 Jan 2024 22:53:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9050a3f3798c7ec9b1995cb5b4c78fda2a1ba1a1fb5cab46c89758c967337005`  
		Last Modified: Mon, 22 Jan 2024 22:53:44 GMT  
		Size: 19.0 MB (19028703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
