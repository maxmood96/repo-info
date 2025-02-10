## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:957ee0c924540df728ffa3c180f608a369fae89039bb987e0ffa199259fe780c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:7714ffae44851ceadb7ce05df46c8f31fc058e90cb050c80d69ddb2b58d2bd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183634877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565224969ab6d580f99a1d91d01207c6aa873aa5aa14aa8e7a87179704d34b8f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Mon, 10 Feb 2025 19:27:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Feb 2025 19:28:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 10 Feb 2025 19:28:23 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Mon, 10 Feb 2025 19:28:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Mon, 10 Feb 2025 19:28:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:28:39 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Mon, 10 Feb 2025 19:28:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Mon, 10 Feb 2025 19:28:41 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Mon, 10 Feb 2025 19:28:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:28:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 10 Feb 2025 19:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Mon, 10 Feb 2025 19:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Mon, 10 Feb 2025 19:29:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad421ac7b9b1a4c9fccb5d9be1b4c39a7980c94365636f8cd8d8c9c3371e79a3`  
		Last Modified: Mon, 10 Feb 2025 19:29:16 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c117c3ead9914a0a5d20416354afb307216b046e784751991e2c39637ae2ab3b`  
		Last Modified: Mon, 10 Feb 2025 19:29:17 GMT  
		Size: 340.1 KB (340071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a6cff2c2e1714567784de34d844b4f7e5d016fc009d0419de7ec6e96b5dd46`  
		Last Modified: Mon, 10 Feb 2025 19:29:15 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef5d05858ed84a3e18ad3414a6dcc2e8721d6a10f1221ebf196a064eb30a6c9`  
		Last Modified: Mon, 10 Feb 2025 19:29:15 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd23188b85bae2a5c99b1be179068cefe1a4efb06026a6f5d18661d5b463dcf8`  
		Last Modified: Mon, 10 Feb 2025 19:29:17 GMT  
		Size: 19.8 MB (19775687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2e0087b99ecccee549815cabbea01dd00cb39b844aebabb31cc9f4efb8c630`  
		Last Modified: Mon, 10 Feb 2025 19:29:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5c61405a12a15018a09f70a6c3449e6a4a1e7bd5e4271e7e12dbe9517622e`  
		Last Modified: Mon, 10 Feb 2025 19:29:13 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b843f8f863211e43a7aa438bdda92df683b2c04ba30a66702eb1ee7dd9f7a3`  
		Last Modified: Mon, 10 Feb 2025 19:29:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1fe62c994507df2ffeaa49907c8ae1de2966cc42c640de512908a86d74cd96`  
		Last Modified: Mon, 10 Feb 2025 19:29:14 GMT  
		Size: 21.1 MB (21131375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d619581d802e88f96c89aaca9f1b2ebc8879f0628091808d6114f0c9f33f3476`  
		Last Modified: Mon, 10 Feb 2025 19:29:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579795127c5544d3f700ecc76bba61de71d65567d4d6fc88970be3ced0948eb9`  
		Last Modified: Mon, 10 Feb 2025 19:29:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e7d8e3689a1094d7a8b9f1c5a772c8653297b5969a7bd81773b92395639dba`  
		Last Modified: Mon, 10 Feb 2025 19:29:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8786e98794ffc685ace3c69ece60579421998ca3a2da340ed005087278b0f3ce`  
		Last Modified: Mon, 10 Feb 2025 19:29:14 GMT  
		Size: 20.2 MB (20163836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
