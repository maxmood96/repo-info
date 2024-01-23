## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:45324cfabe09afab42e505f3a8b01d13aa3c8d6cd5e9e3c331bdb384deac3854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

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
