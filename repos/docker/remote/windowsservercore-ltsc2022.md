## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1c7ad5b5ef3c89a3bdc56e2574cbfe03b7327d744f4266d72447109f574789c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:08c5da38b0e30b8a83bf89e16eff7a1292d6948010a051f9310d6e9511e6423f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178998545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2de39d58f5e39341f81d00642352c6b050887b387821ad49ffd590b688ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 22:15:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:58 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:17:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:17:09 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5961f3afdef68ce25fa592066416467d81416df4b1af2537087f1c9150afb728`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae47499b6a77bf67c8fc4c6163dd490f816d5ea9168dfad57664888a82963cd`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 506.6 KB (506623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a50c6ae3a4766042c073c45ffd8a1c5d67595c9c560f65c76492d18a12fd50`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756530867ead10020116e1f2f106664f6fed6cae2160122fc6ec372b43fd678b`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d6d943b8fa9b8934a5ce05bf2893265e234366a62bf9ea3a09f77d5608167`  
		Last Modified: Fri, 15 May 2026 22:17:26 GMT  
		Size: 20.2 MB (20232134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38228e51f50d7a28325477b370bd57476f2a6883a023e98c0d628bc22295ad4`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7fe5a6a8d2169e19d30f03057f1cf4e3dfa71a14a9e3e2572a95d5246c205`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b9407c6ba09fc25979a724f032914bee3ded478b4366b26a09de96ef0c80`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb62b675b679633b1a24e24b203fa8ed15d941f3bbb283bae34df7d68c50af`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 23.9 MB (23901135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8874726604cb50cc54f506879180a624b7e0fc0e3ad5a8a7063d89505fd60ea`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b4c5d7c92d0e67fbdf7582c6455934c8b5f3b3a8c849173931adad0837ca3`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6f324d4756f3cd5de0642c06bbc7c60c070aa7a512c8682d7e2232291ae8b`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487382c6166366ea2b9acbadbf146f8443b6a756bfb7678718eb9c7383bc4a2c`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 11.9 MB (11926255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
