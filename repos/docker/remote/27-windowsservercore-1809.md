## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:7732849f741714b49715193e2805a13f7cd9b5d35e4c218afaa61b649a0cefbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:6946edfaae022712905f65b469faafe6a2d0e790a8a84ff3a05c1fc676d9ba52
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778733573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ab3a1df4eecf5ff650ab01ec8fe6566b713b30f40c196913bf4278504ea09e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Mon, 16 Sep 2024 19:03:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 19:03:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 16 Sep 2024 19:03:36 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 16 Sep 2024 19:03:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 16 Sep 2024 19:03:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 16 Sep 2024 19:03:55 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 19:03:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Mon, 16 Sep 2024 19:03:56 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Mon, 16 Sep 2024 19:04:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 16 Sep 2024 19:04:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 19:04:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-windows-x86_64.exe
# Mon, 16 Sep 2024 19:04:12 GMT
ENV DOCKER_COMPOSE_SHA256=ae793808ae7cb326b2a20a35b1ff66022bf05d9a80bb08822f4455bbb44ff2c8
# Mon, 16 Sep 2024 19:04:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02de109e9af36ca7c156d8b291f5d8d69217c543d908e2116754fd104ea61713`  
		Last Modified: Mon, 16 Sep 2024 19:04:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757e1f0c0a9d9001bf52f1cb1817c5907e26adc3ae28cbc7b712a3e30aecb644`  
		Last Modified: Mon, 16 Sep 2024 19:04:39 GMT  
		Size: 340.8 KB (340819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7941a6b133577615a9f883a1f8fca9b09a2a853752b90088e6c0ccf554cc9d9b`  
		Last Modified: Mon, 16 Sep 2024 19:04:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f630f96b83465e31c4d32cd13a2999709aeb19218a29cdaef45f4172ffdd469`  
		Last Modified: Mon, 16 Sep 2024 19:04:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c55bb0b6b96f7d02674806761fedb6720e5329e44f7b823be7b2e38f7cb006`  
		Last Modified: Mon, 16 Sep 2024 19:04:39 GMT  
		Size: 18.9 MB (18925462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86115c46ba155a5b906a701124b60c0f7974ca5e208fee84a9daef75258dfe06`  
		Last Modified: Mon, 16 Sep 2024 19:04:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592643264bc6068cd8ba5acf9a4342765bef000c4a9ad5e2583871cf9d73a8d5`  
		Last Modified: Mon, 16 Sep 2024 19:04:37 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac9f87d279f5f0c1e4b89564ec4f2d8bc0c778cb99cc977e921c3f690c18fa8`  
		Last Modified: Mon, 16 Sep 2024 19:04:37 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff086d7b27ac847c29e15430aba2a5678fd9e1275da5527cecb415a8674e0e6`  
		Last Modified: Mon, 16 Sep 2024 19:04:38 GMT  
		Size: 19.3 MB (19279730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374862512cf35a710e7b41df3964cce4cb6dd465047a194caed311c3846b53e`  
		Last Modified: Mon, 16 Sep 2024 19:04:36 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1757a8a7ceb19293c79d4a7eea9e5c69ba813a576eb58c81bf4f0643dcb8f7c`  
		Last Modified: Mon, 16 Sep 2024 19:04:36 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d771f23ab557bd64341e999cce3547c66ad42a1ee0f135d0abc3f2749e1f712`  
		Last Modified: Mon, 16 Sep 2024 19:04:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ed0f040ef35e33b9275a91b3f090b40e4e2a6d5da757bfb1901f66cfd78c9b`  
		Last Modified: Mon, 16 Sep 2024 19:04:38 GMT  
		Size: 19.9 MB (19907389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
