## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:f03d1b32ca4d0d7415dab6f8ab0a7fc6a5f5e6807c93d98ce56871b7e6f3f770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:cdf6aa8c3435340c7c3c56d5714e66c23ea2e7f04c947565b6d8494d8ae361f2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125346611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29d46783289fa8034fbb9aab9ac2bcba053cffa70393bd7f55c8d9b01e2f322`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 18 Jan 2024 23:03:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jan 2024 23:06:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jan 2024 23:06:08 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Thu, 18 Jan 2024 23:06:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-rc.3.zip
# Thu, 18 Jan 2024 23:06:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:06:44 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 18 Jan 2024 23:06:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 18 Jan 2024 23:06:45 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 18 Jan 2024 23:07:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:07:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Thu, 18 Jan 2024 23:07:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-windows-x86_64.exe
# Thu, 18 Jan 2024 23:07:15 GMT
ENV DOCKER_COMPOSE_SHA256=6c94193c282d5fba71563c617fe8ddf8dce9355fb1d0ae93609221c590d06fcb
# Thu, 18 Jan 2024 23:07:38 GMT
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
	-	`sha256:63e334d5c04f2ddc57fd2b06104cc3c7f01ac08d98323dc444ca98aaa7bec135`  
		Last Modified: Thu, 18 Jan 2024 23:07:44 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffa19a9c81bb3db49595f54eb9462305a0f502077b5003947a70b0b8c454364`  
		Last Modified: Thu, 18 Jan 2024 23:07:44 GMT  
		Size: 493.6 KB (493614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e3a95827dbfd7e9ea56bdf475af99d101bba62cbf1879052df633f320fda0c`  
		Last Modified: Thu, 18 Jan 2024 23:07:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c270919c607ec4d553ef5830b727645ed292a41ca0be14f97812c9be3558c`  
		Last Modified: Thu, 18 Jan 2024 23:07:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a55c7fae2d7002fd706805844c1d02064ea7ba9416733ec64d49de452daf73`  
		Last Modified: Thu, 18 Jan 2024 23:07:45 GMT  
		Size: 18.1 MB (18071318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca05c6e38bebcc7676f92c2615916e8366f09517d3e4f9ceb7477ac967f660`  
		Last Modified: Thu, 18 Jan 2024 23:07:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c203a4d0024709f588d0eb307e0a9c36d0c1d8bfee310026a85e0caf4ec3d4`  
		Last Modified: Thu, 18 Jan 2024 23:07:42 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba8eb3d63a83f07907c942f087ad12ea83a0bed8eeec4a6c160824504632b3`  
		Last Modified: Thu, 18 Jan 2024 23:07:42 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc0680dbc565956fc2748cafade8d008f364edc6cc6dd10a3012c5a08313b9a`  
		Last Modified: Thu, 18 Jan 2024 23:07:43 GMT  
		Size: 18.0 MB (18020224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff6dd61c0c68c58fec532897f357dc746a39938bc842eb3d37585b43b5eb350`  
		Last Modified: Thu, 18 Jan 2024 23:07:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01d98e357060f1b82efb80bd5b2e8b99355656b064bb245f3cf09de7d10aba3`  
		Last Modified: Thu, 18 Jan 2024 23:07:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3dde7f901971e817a7c1f756e91e1f67742924499bb06b17755614c4254705`  
		Last Modified: Thu, 18 Jan 2024 23:07:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae4dddef97660a6bc1279d3ac2b0d3c03b62348d8b71633e40ca74f66fcafe`  
		Last Modified: Thu, 18 Jan 2024 23:07:43 GMT  
		Size: 19.0 MB (19027227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
