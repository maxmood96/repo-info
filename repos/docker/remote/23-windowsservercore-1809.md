## `docker:23-windowsservercore-1809`

```console
$ docker pull docker@sha256:71703614c8903a1bc56929c35ae5689bee39d84a39ad3652dc46050d89863186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `docker:23-windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull docker@sha256:0a17d6ab496b8123bfc26f4dc9a3343f956fb7f97d908bb0432a764f34f36fc9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2122570190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e9d6ac29697970c330f73312970eb7d9e4ad2d2a62cb6565421ab621819e91`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 03:25:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 26 Apr 2023 20:54:11 GMT
ENV DOCKER_VERSION=23.0.5
# Wed, 26 Apr 2023 20:54:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.5.zip
# Wed, 26 Apr 2023 20:55:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 26 Apr 2023 20:55:24 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 26 Apr 2023 20:55:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 26 Apr 2023 20:55:25 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 26 Apr 2023 20:56:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 26 Apr 2023 20:56:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 26 Apr 2023 20:56:34 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 26 Apr 2023 20:56:35 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 26 Apr 2023 20:57:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103f1e2cdefe8f16dae9619b88e38aa659abb17276d2362d435ad0721d3bf41`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f180306e9d61cdf6a72f401f1f32a79e350f22b096e8dd7910d6afe20e3e23e9`  
		Last Modified: Wed, 12 Apr 2023 04:07:41 GMT  
		Size: 500.1 KB (500143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d3a5dd56dfc515dd425ff14eccbb6d8e73800f683b019ada9f025216517f06`  
		Last Modified: Wed, 26 Apr 2023 20:59:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c411787970f4364520e4e2ecc51ff95d772ea23bf4c3ec7daa17da3ac4c9de1f`  
		Last Modified: Wed, 26 Apr 2023 20:59:05 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6742b548a22a104ee04c1ddf6ee1f82cf7d47ae8d213f9815108c715a3d6d304`  
		Last Modified: Wed, 26 Apr 2023 20:59:08 GMT  
		Size: 17.4 MB (17389577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32671fca0d4ad2c39b26bf761ee605e6d16e805ed4086651b105980e790f3e5e`  
		Last Modified: Wed, 26 Apr 2023 20:59:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40207302a52e7d36167bedb4ff19c66fea74e54fbbf2dc33ddf93293b76a9c3d`  
		Last Modified: Wed, 26 Apr 2023 20:59:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d526969d7a09e8aa021ec1626d3afb45757fb1046d76ac6fa89afff9853fc7d`  
		Last Modified: Wed, 26 Apr 2023 20:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9769ca72cc9d273ace860e443e4d49fe1ea7e03bd591f55a6835bc984fe395cc`  
		Last Modified: Wed, 26 Apr 2023 20:59:06 GMT  
		Size: 16.5 MB (16503721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94b213da264e7914e807cb5f9faae7c9f917ace14a41e1df6aaba9ea67a5af2`  
		Last Modified: Wed, 26 Apr 2023 20:59:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead3b8b30b053121e7f67c5bcd7271e0cf37b56508bb325b2f86d23350393731`  
		Last Modified: Wed, 26 Apr 2023 20:59:01 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9e3e1dd65a6e4d1e0af0bad5e1817a3b52ef79bec6bfe8ec7cad2d016840bc`  
		Last Modified: Wed, 26 Apr 2023 20:59:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446e2b7f4e4c2c344befcc899faab381677344439aca98d19097821873c240ca`  
		Last Modified: Wed, 26 Apr 2023 20:59:06 GMT  
		Size: 16.9 MB (16873676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
