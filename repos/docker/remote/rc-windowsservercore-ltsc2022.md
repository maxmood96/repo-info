## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:01042628d4b514cac8b8d1c8117ac7a18faa23367e02290c3e600f1e009a8c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:b5271d473302d7a60b7bcdc1da426cd17043ec110e57373c23e862f574025c0b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327017815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5ee6a12f647e408d5e4c46de9f0e068b783dffc165df892af2320c4313600f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Wed, 19 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Feb 2025 00:34:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 19 Feb 2025 00:34:18 GMT
ENV DOCKER_VERSION=28.0.0-rc.2
# Wed, 19 Feb 2025 00:34:18 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.2.zip
# Wed, 19 Feb 2025 00:34:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 19 Feb 2025 00:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 00:34:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Wed, 19 Feb 2025 00:34:30 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Wed, 19 Feb 2025 00:34:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 19 Feb 2025 00:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 00:34:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Wed, 19 Feb 2025 00:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Wed, 19 Feb 2025 00:34:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3f1069dea9bd0607a8fb7fc76c3665c467d55340416f0de69da6abf7022fc7`  
		Last Modified: Wed, 19 Feb 2025 00:36:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b67032867116448034b144a09546a02577b7f54514ceb787d6d848c8cf14a6b`  
		Last Modified: Wed, 19 Feb 2025 00:36:21 GMT  
		Size: 365.2 KB (365246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa536d1d0e3433d6bf9836507a1f7275c143e2dc6f027ca3f4540874122adee4`  
		Last Modified: Wed, 19 Feb 2025 00:36:17 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d002f25b9133133449ebb4e67884f65da6927ca8d0fe6a0b3391d8b9ea0e908`  
		Last Modified: Wed, 19 Feb 2025 00:36:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba24ad074a53eb987b17a8dfd9e9670c465f54b0a5328d728bef39226f4b0444`  
		Last Modified: Wed, 19 Feb 2025 00:36:19 GMT  
		Size: 19.8 MB (19808023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a376f438fff70b0a2fe7d0d7641f3619375038f5e558052d060408f623af8`  
		Last Modified: Wed, 19 Feb 2025 00:36:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983c32a42ca9792f52c7c1a089c1e86b01f4d4e80c7c458242a56b78d07085e2`  
		Last Modified: Wed, 19 Feb 2025 00:36:17 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81e134697e20e09d32b1aaefd4b479b9834af886932787af1051025c6f65c40`  
		Last Modified: Wed, 19 Feb 2025 00:36:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d430b4662df4493981ff15ed9cb9142d064a80a8255badc0be2e666db4b59e`  
		Last Modified: Wed, 19 Feb 2025 00:36:30 GMT  
		Size: 21.1 MB (21145150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8834ad22b740f07faac8a3aafb86ce738e7aaed2e74f6a4550ec6ffc0c5ecb71`  
		Last Modified: Wed, 19 Feb 2025 00:36:17 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5290097776324678360799c705fe819a4e746ce149a3327883a5f75100d45130`  
		Last Modified: Wed, 19 Feb 2025 00:36:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4543ed98779fa9eaef51f49cb3dedcd6f03f1b7dd7f6371717276488c09328`  
		Last Modified: Wed, 19 Feb 2025 00:36:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b401c67626ad5ab5168f23a5a28fbe4bdf1ed11c6c8b2f4fc47c754660b27`  
		Last Modified: Wed, 19 Feb 2025 00:36:19 GMT  
		Size: 21.8 MB (21829811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
