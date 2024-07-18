## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:48473bddf1edd525f24133d9c71986b8940d5d9bbbe101c451498f28a56ed416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:6064f7085c089349c2af19c686c4a990a34fe03c189ea6aeffe67e3e31274244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2196455646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1863276ed98e0af2f4e7bf6d63a55fdaea3e84991740dc05bdc013c767251cd0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Thu, 18 Jul 2024 18:55:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jul 2024 18:56:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jul 2024 18:56:39 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 18 Jul 2024 18:56:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Thu, 18 Jul 2024 18:56:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 18:56:55 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Thu, 18 Jul 2024 18:56:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Thu, 18 Jul 2024 18:56:56 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Thu, 18 Jul 2024 18:57:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 18:57:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 18:57:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Thu, 18 Jul 2024 18:57:06 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Thu, 18 Jul 2024 18:57:16 GMT
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
	-	`sha256:d9252b4b4e34d24e40bb4793dc004f6a6003b03c640b80ce9ef50e242d2566f4`  
		Last Modified: Thu, 18 Jul 2024 18:57:24 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96ee9a1bcc3c2bcdcafb434ad0ba004105b9d034d98ffb1959a81bc2345f45e`  
		Last Modified: Thu, 18 Jul 2024 18:57:24 GMT  
		Size: 359.0 KB (358968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a372927cc71b90ea1ff18880f3acf30f80155319fed263c2e5df5f1be33f791`  
		Last Modified: Thu, 18 Jul 2024 18:57:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db5d5f971e08668b99f0434df7944f9d530e29927867f137406a0b7eb42ec4c`  
		Last Modified: Thu, 18 Jul 2024 18:57:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777b75dc21a168e57cb8805801fd9a85b81d0b58e5d9b99a00363c21f1b154e9`  
		Last Modified: Thu, 18 Jul 2024 18:57:24 GMT  
		Size: 17.5 MB (17533994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e56be3e352de37f4ce36a492bed020bce8acf91961845b5487bf2386bbf442`  
		Last Modified: Thu, 18 Jul 2024 18:57:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c940ba767fba22b40b3c442b2acdf78c00e44f4b76ad7e10f0be2da6f833c4f`  
		Last Modified: Thu, 18 Jul 2024 18:57:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda09f2cbe602900ed5c061de75bf5170e2968efe29df7e794a7646cf98f2c49`  
		Last Modified: Thu, 18 Jul 2024 18:57:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e59c716e65019cf6c647667a741228802a4737fd72d929e765370144125728`  
		Last Modified: Thu, 18 Jul 2024 18:57:22 GMT  
		Size: 19.3 MB (19258167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673efc4650af30018daaf6782ace2db4cf235e037176b4656e8f04a1f76e6150`  
		Last Modified: Thu, 18 Jul 2024 18:57:19 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864d9afa9cd0a350c89757ba784d86e7a8053739a6541f4597ff7371fff61987`  
		Last Modified: Thu, 18 Jul 2024 18:57:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3ad2d9c12151f5ad4fe212cc25a8c18949607c8887add01625d824dbd1362a`  
		Last Modified: Thu, 18 Jul 2024 18:57:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33b4656b3781708b4c3fa2b4c680f799aa0b2374797e22230e15182938c8768`  
		Last Modified: Thu, 18 Jul 2024 18:57:22 GMT  
		Size: 19.7 MB (19692711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
