## `docker:27-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6468a193da4dcdd4849f0a85c259c52db8c99d573bc85e66ee14d0897612be6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `docker:27-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:67df468ed6b6daeab34babab11a8c4a69281962e8c0c3f0b7925cfa06f51042a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311501680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2740427e9956a06f1e79d0829725b0c9f9942aea15fe5b4aa072b94a035a991f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 05 Dec 2024 01:27:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Dec 2024 01:29:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Dec 2024 01:29:27 GMT
ENV DOCKER_VERSION=27.4.0-rc.4
# Thu, 05 Dec 2024 01:29:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.4.0-rc.4.zip
# Thu, 05 Dec 2024 01:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Dec 2024 01:29:48 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Thu, 05 Dec 2024 01:29:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Thu, 05 Dec 2024 01:29:49 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Thu, 05 Dec 2024 01:30:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Dec 2024 01:30:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Thu, 05 Dec 2024 01:30:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Thu, 05 Dec 2024 01:30:06 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Thu, 05 Dec 2024 01:30:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf6d46328e6b63d040dd4f64fbfa1704fd45e5970bb464e1fa4ad4c4c5802c4`  
		Last Modified: Thu, 05 Dec 2024 01:30:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb79793a79b421f305989f0bba34a058c29395210d473b5a8c650c3ef17c760`  
		Last Modified: Thu, 05 Dec 2024 01:30:21 GMT  
		Size: 373.5 KB (373508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca00e4f1260b580cc89c3da67e58bb446cb245f610a6a83cfac070273dc9fdfa`  
		Last Modified: Thu, 05 Dec 2024 01:30:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e9c0e472a2d743e5859c5fe41783d7b12a79333cfa3ce56026adce600317f4`  
		Last Modified: Thu, 05 Dec 2024 01:30:20 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e881f4c3c19de3ee63b03e3cccda008b444b31092af36e288b83ff1577f2a37`  
		Last Modified: Thu, 05 Dec 2024 01:30:22 GMT  
		Size: 19.0 MB (18975119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7727b67efcc8cc5e77dd75ea46a915c39a760d932d76444524dc58f937a26f67`  
		Last Modified: Thu, 05 Dec 2024 01:30:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c6a874ce2de5fb18841f20807171daac16a6a4d433c0bc4f20681182ae8c75`  
		Last Modified: Thu, 05 Dec 2024 01:30:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69122410894ac93f5efaf6e0deb3201d7112158c362754dc5d004366731ac04`  
		Last Modified: Thu, 05 Dec 2024 01:30:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d3c0bda81c4cba85bd8f5f7aad5a830832d2a59cd945042508f8e56ef69410`  
		Last Modified: Thu, 05 Dec 2024 01:30:20 GMT  
		Size: 19.6 MB (19622332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db8ccf328543d9f237b24949fcfb77ae3bf6b35d8bf43a76ded7cab11cd5480`  
		Last Modified: Thu, 05 Dec 2024 01:30:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279bc03a4f6f24d8eb1f0d5f5a8d7e9d05f6dc51929aa303dfae152284742705`  
		Last Modified: Thu, 05 Dec 2024 01:30:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646fcebd4fcde3e2bc914a4a8db63d2833798f8c69e3560e8eb2d9fcbe3c58fa`  
		Last Modified: Thu, 05 Dec 2024 01:30:18 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838807ae88c4fa54b900b08838d9cc195eab7f5a54314b69a406072a3e2855e9`  
		Last Modified: Thu, 05 Dec 2024 01:30:21 GMT  
		Size: 20.0 MB (20034930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
