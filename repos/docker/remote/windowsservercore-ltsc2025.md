## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:0f458060178ee7b494def8a1c93a986c0822b94d655fead515c0f9fd6180196a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:ba777ce4ffefb7e1a583a0b952b175b2f37d9d93d3ecdc3325b334b36049a79f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262437168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88821562bde9244631c7e166f6acc156ddcf127956ef23332df624a7ce2a1d15`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 04 Jun 2026 18:05:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Jun 2026 18:06:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Jun 2026 18:06:37 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Thu, 04 Jun 2026 18:07:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Jun 2026 18:07:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 04 Jun 2026 18:07:06 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 04 Jun 2026 18:07:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Jun 2026 18:07:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 04 Jun 2026 18:07:30 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 04 Jun 2026 18:07:44 GMT
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
	-	`sha256:12e4c7b7fd97730db85cc8cb4e24f79703a02cc0f7f06635851629174bb44d30`  
		Last Modified: Thu, 04 Jun 2026 18:07:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc43a027f6b89b4d553ec7037bc17737a9eab9fa5380f0908825cbfb217a017`  
		Last Modified: Thu, 04 Jun 2026 18:07:54 GMT  
		Size: 406.6 KB (406649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ced300ab5391a7c38687e5b984ba803ec69b5c2d126d1a0c0d8047b12facb80`  
		Last Modified: Thu, 04 Jun 2026 18:07:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5864470dfe3d7bc2790e072a76be42ed74dd9371700e1f2797e5c16df5fc1ffe`  
		Last Modified: Thu, 04 Jun 2026 18:07:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d68dbbbfa1966dc74d4f6c5148b078e3d54784e374da07e5132546315fc5782`  
		Last Modified: Thu, 04 Jun 2026 18:07:55 GMT  
		Size: 20.0 MB (20022155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37ac582299df92d3af3260e7064260c6fdcc843b61d6e73145232cf175cd4bb`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd65284eb90d7f479096f37d4c60da09ad9bf562d7e971aba07a586e999a6eb`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31948ea43a781037597d869411c3f5a1e69fc5db903b69caa4dd5d859cbb6ae2`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7ef594c12ebe34495352de41cd28c8def8f4919e85538782e3b12b2de75948`  
		Last Modified: Thu, 04 Jun 2026 18:08:08 GMT  
		Size: 23.9 MB (23935081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a668513393fadfacaec2bcb4393cf4b7595ee0a605ddd8e1b64203e2480acc`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fb3b86ccca4649a4f99fe1251e441f7a5b67cae43dd70a7980bde1e485f0e1`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938085c6b5b637765dbd2003897afadb4afc9b7e6f63d291dd41c703b75eaaa5`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1431354d9ea3cf303ed27b340e79bd92000923d7c9e3496a5c9061dc5da0087b`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 12.1 MB (12119822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
