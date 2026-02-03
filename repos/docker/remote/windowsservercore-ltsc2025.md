## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
