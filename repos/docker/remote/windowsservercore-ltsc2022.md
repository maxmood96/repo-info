## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6bf82563a92527086103fa207c44adcac510de21b9d7ce4234565118a1010364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:83a06bbcb87bde57bf89aad73c8f350a09a1310d69ff4fa30464c56d83912118
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2176449391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efedf6e6257f1f89bdddb0ef0fed0ee30ebde2875c74ac12d71aaa48b8a1d75d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Mon, 24 Jun 2024 23:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jun 2024 23:01:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 24 Jun 2024 23:01:56 GMT
ENV DOCKER_VERSION=26.1.4
# Mon, 24 Jun 2024 23:01:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Mon, 24 Jun 2024 23:02:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 24 Jun 2024 23:02:06 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 24 Jun 2024 23:02:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Mon, 24 Jun 2024 23:02:08 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Mon, 24 Jun 2024 23:02:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 24 Jun 2024 23:02:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 24 Jun 2024 23:02:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Mon, 24 Jun 2024 23:02:16 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Mon, 24 Jun 2024 23:02:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246e482b6e23771fa41b6a97ddf58d6b8e2c45211e1524cfb7eccfa0fd9ce1d4`  
		Last Modified: Mon, 24 Jun 2024 23:02:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da0fca8cfb8c4aeedf6a91d0e065be220a4ce837dfa4d404f9f4f5e540c7e4`  
		Last Modified: Mon, 24 Jun 2024 23:02:28 GMT  
		Size: 345.9 KB (345885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068d6a51b1a127e2fd7469da3666cdd3c1affe6d4e2f69a80bab48d114954cae`  
		Last Modified: Mon, 24 Jun 2024 23:02:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6768c61d278aef37aa33785426450619cc28d80ccd049018f0785c299db14e`  
		Last Modified: Mon, 24 Jun 2024 23:02:27 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2617e1912221cf413d04d7299580b0daea3c0825fee7b5d9fad6a9a44f1a5454`  
		Last Modified: Mon, 24 Jun 2024 23:02:29 GMT  
		Size: 19.2 MB (19241807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d31372f6eb1e0c4455e4bad9bc6a40935b8576f56647573811f728f66716b29`  
		Last Modified: Mon, 24 Jun 2024 23:02:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27164582d8240a6b1c5b712d95806fdb59df86cf8a1bb194e96fb5e1f3a1676c`  
		Last Modified: Mon, 24 Jun 2024 23:02:26 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619a32541eaeb8b9af553b64aae13f0a963563ba072449138c4b112a2300eaf0`  
		Last Modified: Mon, 24 Jun 2024 23:02:26 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a67541314ab9c624da2df20937b0861ab7987c9b9d59af61e9ee17921078e13`  
		Last Modified: Mon, 24 Jun 2024 23:02:28 GMT  
		Size: 19.0 MB (19012054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303765272afa63b6e978553f603ccc8143fedc46a75c558e0fc2083d5d17d334`  
		Last Modified: Mon, 24 Jun 2024 23:02:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d6e97d4bbb0d07c480be5888d63631d5e2be9ad351c44720e781473cddd384`  
		Last Modified: Mon, 24 Jun 2024 23:02:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983542ae2a8cf1dd1fe4c7e09db1444d8ede7e730e2eab3e7c92f12f3d135a71`  
		Last Modified: Mon, 24 Jun 2024 23:02:25 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1690f9793edbd076b9cfb65e446be51744ed4e88575f5212285d2665e5276985`  
		Last Modified: Mon, 24 Jun 2024 23:02:28 GMT  
		Size: 19.6 MB (19647600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
