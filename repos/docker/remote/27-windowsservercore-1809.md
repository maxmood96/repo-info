## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:33d0cfb22fdeb687dad2ee7a0569fa8661a7cfca017305d3492645a09e7bf275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:f43aeed0b833824092a1af517b89d7bb5d127ef431608fa9f142571b6014b75b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297193945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638b1ff933a76cb4525771d0cc3efe5066ddc6dfb28565cf7dc2336853a11c11`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 22 Jul 2024 22:09:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 22:11:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 22 Jul 2024 22:11:38 GMT
ENV DOCKER_VERSION=27.1.0
# Mon, 22 Jul 2024 22:11:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.0.zip
# Mon, 22 Jul 2024 22:12:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 22 Jul 2024 22:12:15 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Mon, 22 Jul 2024 22:12:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Mon, 22 Jul 2024 22:12:16 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Mon, 22 Jul 2024 22:12:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 22 Jul 2024 22:12:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Mon, 22 Jul 2024 22:12:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Mon, 22 Jul 2024 22:12:47 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Mon, 22 Jul 2024 22:13:11 GMT
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
	-	`sha256:e5722a6c35de79a6ba62c6f68555d3481bd612715692293e21808e1f3148412f`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36560dd96f298e266280aacc94078aaee1e8d8167d18f9910770b1ba1fa1024`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 499.1 KB (499139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67090d7cb650319db1275b3b8b2e377a12f6b4876a173184e54c489ce122007`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f92a0d4b5623be14a097e19ed36f87102a1aec0c7c086240f6e6726df07fde9`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1369c743c87d51b33710f4358be843e8a8592c4b8ab6bd04e302377cea26d789`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 19.3 MB (19300711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacd740cfd17bea9b1171bcc7bb502de977ca868f301234f2caf148620f1738`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1530315a56480b3029f0b2d2acc6fae6a2a87b8cc85460ab3396b4db56cca63`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c5014d117bb4af14a6676b9822b483c0d0643008f0371361ed0703f767fd94`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc4af703a00526f8269f0b3308f611a47d5709ee81dc2eb0a8585701cd828d9`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 MB (19263046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcd49d916b7b24dcdd711dcd96febf9fe1e16f2286c48d4c9b3c12466ae3f2`  
		Last Modified: Mon, 22 Jul 2024 22:13:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e7c28afcada5cd019b7d8bb817e97b0ea072d9b08b3d3bdd52699c80278428`  
		Last Modified: Mon, 22 Jul 2024 22:13:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45af29a214167ee1cd5f285be348e2221011159a2e7bd445a854fd7a7947cc56`  
		Last Modified: Mon, 22 Jul 2024 22:13:14 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44388ba4e9aa4ff1589586a71b75b4e7a2f68224162e58e0dc3c62e8ef1157c4`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.7 MB (19689947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
