## `docker:27-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:63091641d6e86a51bfe431461da6a453bc4e00ed1d0bf398a4189dffe33c411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `docker:27-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:0bcc18d8c3b63dd4a87645f0d75e3c8b47824943cc1bf2bf5f3f43b0291ce53f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311598719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca528775b79258035fcc0dfb5775a74ae12eef97995f403b732ea9460ed7c198`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 04 Dec 2024 00:29:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:30:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:30:10 GMT
ENV DOCKER_VERSION=27.4.0-rc.3
# Wed, 04 Dec 2024 00:30:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.4.0-rc.3.zip
# Wed, 04 Dec 2024 00:30:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:30 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:30:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:30:32 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:30:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:30:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:30:42 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:30:51 GMT
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
	-	`sha256:a417254b87614ce399a3f209f1ce99d9c7a63a2375cf0f64ad462a418e086dbf`  
		Last Modified: Wed, 04 Dec 2024 00:31:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0028b1e443ed806d834a5386620c137e579cdf75edc4af252eab68760af1535f`  
		Last Modified: Wed, 04 Dec 2024 00:31:00 GMT  
		Size: 368.9 KB (368904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a14e0ee044dcc7646b8f8cbada8c9106d03eea8ea6917e3fa99e9ce60b49372`  
		Last Modified: Wed, 04 Dec 2024 00:30:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf99ed6aea90afc819a9a9334157a006b4c7fad3ebcdf9c218c5373006e7298`  
		Last Modified: Wed, 04 Dec 2024 00:30:58 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff05f7c7d1fd1f5b9e540636e3517c240e0641c402a2e27d698e0dba087d6750`  
		Last Modified: Wed, 04 Dec 2024 00:31:00 GMT  
		Size: 19.0 MB (19011911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd536bb89340ac63876ed73e1b3457e42ccd6f10a47d5d976dbb455f51136cee`  
		Last Modified: Wed, 04 Dec 2024 00:30:57 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6965175e4ae932171a2fc30991640cf3d413f81cc5a559d6dfa3d35478000660`  
		Last Modified: Wed, 04 Dec 2024 00:30:57 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9d62e24f0d2d6a0f1428300d9db627bdca90dba74e65ce85649313fd2815cb`  
		Last Modified: Wed, 04 Dec 2024 00:30:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d8b7f9cf6699ddd17f089f23df9aaefeb2cdfd50a0c7097bd9dd15e7df90b4`  
		Last Modified: Wed, 04 Dec 2024 00:30:58 GMT  
		Size: 19.7 MB (19654410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda32802fbaa3099e89e0660e9b7b547e60c5807123fa4718518e2ecd2b2911c`  
		Last Modified: Wed, 04 Dec 2024 00:30:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31925b5b495a23d2c2a793b8f4610ac7e643e11f563d0770e1059af7fa3649ac`  
		Last Modified: Wed, 04 Dec 2024 00:30:55 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba32209596d74d79f565f202e37a439eb8154c03790936d249408160f5a77fa`  
		Last Modified: Wed, 04 Dec 2024 00:30:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7878c5996e460a37f1f78e634e8d5b81f88ab1da0cb30e8f6cc5d5bc3579ff3e`  
		Last Modified: Wed, 04 Dec 2024 00:30:58 GMT  
		Size: 20.1 MB (20067417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
