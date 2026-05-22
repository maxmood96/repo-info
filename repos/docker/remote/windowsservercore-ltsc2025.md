## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:38a6d8d2632ca78eb3229980b6b255413aa7fafcf1d3ad906265d8c05df98652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
