## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:985722c5d551f2d466b61d83cd924bc7743b9a5c6dcf282be5338753ccf9ef39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:bf5f5aa34471e885aefb8f58ff42aa24d7407a2459b7c2c501fa3cefaeadf4bc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345339825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42adcada52ccb5aecec76f01713e2629403dd7a8316216ab4ebf6566bd33dfd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:31:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:31:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Jun 2025 21:31:46 GMT
ENV DOCKER_VERSION=28.2.2
# Tue, 10 Jun 2025 21:31:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Tue, 10 Jun 2025 21:31:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:31:57 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Tue, 10 Jun 2025 21:31:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Tue, 10 Jun 2025 21:31:59 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Tue, 10 Jun 2025 21:32:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:32:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Tue, 10 Jun 2025 21:32:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Tue, 10 Jun 2025 21:32:08 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Tue, 10 Jun 2025 21:32:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eab7dec2e5897372a094abf3d2153459377e2fa9ec67761fe50de5210b057`  
		Last Modified: Tue, 10 Jun 2025 21:40:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5166071c1c608806c8e7939b6f6645ab7cb894246272766f95f573bde8a1d407`  
		Last Modified: Tue, 10 Jun 2025 21:41:02 GMT  
		Size: 349.8 KB (349825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06cd1293b4ab9ab3d42ece1e276e612d2996a30116d27bd59df52d95ce8a3df`  
		Last Modified: Tue, 10 Jun 2025 21:41:08 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e082a027da8efe06ee0e734de05eee07efccad7c4208f4ddc816578bdd86f96a`  
		Last Modified: Tue, 10 Jun 2025 21:41:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca842e7542f6c81a4ee10997a7146af6ac80095c03b9939846a45b2ae366f84f`  
		Last Modified: Tue, 10 Jun 2025 22:44:13 GMT  
		Size: 20.4 MB (20447129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076f761900fc66a91368fe274161c64bef3cd6c373a1ffb3a7e38eb66a96500e`  
		Last Modified: Tue, 10 Jun 2025 21:41:15 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3167d7697f352cb71de25e3c6ce245c6e7750f493a03bce754d8591eedf39b79`  
		Last Modified: Tue, 10 Jun 2025 21:41:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83db33db83a7522d2bc93bb27bd309333add683f15120dd39ac305bd8c303e7d`  
		Last Modified: Tue, 10 Jun 2025 21:41:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad71a79e15b7cae878947090089c5c9cee021a490eb40b3dfa5e67d8d0bd6d9`  
		Last Modified: Tue, 10 Jun 2025 22:44:16 GMT  
		Size: 22.3 MB (22258686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c841a520fcb9943668ee6bc4c7426b058aeca30ea0df273c0f51e27cf89d1b`  
		Last Modified: Tue, 10 Jun 2025 21:41:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62a1b7376b2874591464adec4451d7167ab56f000c523ef431615492c8b974b`  
		Last Modified: Tue, 10 Jun 2025 22:44:16 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ca6e653689e408caeea7d4dcdea9cd774f4ab02a925490e632e856927a6ad`  
		Last Modified: Tue, 10 Jun 2025 21:41:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372e060dfdf50df8efa660ea0b080468893912f68cc61a50ca3e0f7ed98469d5`  
		Last Modified: Tue, 10 Jun 2025 22:44:20 GMT  
		Size: 22.0 MB (22021052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
