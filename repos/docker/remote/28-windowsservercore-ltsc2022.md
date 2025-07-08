## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:8185f732594a0ececbe107f3af0fd3cbfe67545273273a093d6b508da8b427d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:8641152c5cd5906694524f2d1249bdea04279683354ec07426d9b54879a0ea26
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346358605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b08792087f41f29f2a37b0a5242f5e54062ccd2b96124750707a70c264411d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 08 Jul 2025 16:58:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Jul 2025 16:58:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 08 Jul 2025 16:58:52 GMT
ENV DOCKER_VERSION=28.3.1
# Tue, 08 Jul 2025 16:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Tue, 08 Jul 2025 16:59:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 08 Jul 2025 16:59:11 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 08 Jul 2025 16:59:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Tue, 08 Jul 2025 16:59:13 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Tue, 08 Jul 2025 16:59:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 08 Jul 2025 16:59:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Tue, 08 Jul 2025 16:59:25 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Tue, 08 Jul 2025 16:59:26 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Tue, 08 Jul 2025 16:59:39 GMT
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
	-	`sha256:3684e2ca7f7e2ef12271694bd6b8f496cb98271e0ad369f65f24abfa8e58380e`  
		Last Modified: Tue, 08 Jul 2025 17:07:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721b2692b293883c81b836486cd91f12162757ec70d1bc43f55c7e89d844819`  
		Last Modified: Tue, 08 Jul 2025 17:07:54 GMT  
		Size: 367.2 KB (367228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9185e859ac7c95a6e0f1b6e11ffa8211dbfb23e8a21e0b2d656ec45dd6c50984`  
		Last Modified: Tue, 08 Jul 2025 17:07:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145d2749ec4717ed1812761cd0255e240221341ab89061bd908275b63e09626d`  
		Last Modified: Tue, 08 Jul 2025 17:07:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83de8f3a956d4e4754c8bb4c09a62317e97cf49fe416727029e88e2ccecfd6be`  
		Last Modified: Tue, 08 Jul 2025 17:07:57 GMT  
		Size: 20.8 MB (20838774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0eb24c380ff6bb7cb2fe3bdd531d69baa814abadea74b3cd6888eaf4e80f5d`  
		Last Modified: Tue, 08 Jul 2025 17:07:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cd51da9d02f8cc8ed34696c63208669c8915775973896025d70caf52e981ae`  
		Last Modified: Tue, 08 Jul 2025 17:07:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144fef20df709408c73a9b4dc8666c0f0a7fa1cd1bdf27b77dc23524b7a96734`  
		Last Modified: Tue, 08 Jul 2025 17:07:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5045387c2a37ea1df485c3e85d31bc295c5b5f49e646e42342cd5ab7b31fb4`  
		Last Modified: Tue, 08 Jul 2025 17:07:59 GMT  
		Size: 22.7 MB (22664518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54cdd05c112d5c79a79130026d5c9d02f27cf28d211786e1c507f15fb4d55d7`  
		Last Modified: Tue, 08 Jul 2025 17:07:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861b09fcf7455a229339892def99eab2207c23344d952dd625a3d1f182eeda3b`  
		Last Modified: Tue, 08 Jul 2025 17:07:56 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948bc6ec5683d88e1a7f6a18a26e4d6d26d19a85549f3d899ce1b88d3bc2e6cc`  
		Last Modified: Tue, 08 Jul 2025 17:07:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed1feeac29ce5a6abe9250fe9f63f30731ae38dec887c50b3f7321af085b286`  
		Last Modified: Tue, 08 Jul 2025 17:07:59 GMT  
		Size: 22.2 MB (22224904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
