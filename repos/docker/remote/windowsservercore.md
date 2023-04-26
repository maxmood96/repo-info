## `docker:windowsservercore`

```console
$ docker pull docker@sha256:7165a95fa5b824386b10c7d6fe4dfa2a4e39242b1145a30fcacced9dfd79239e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `docker:windowsservercore` - windows version 10.0.20348.1668; amd64

```console
$ docker pull docker@sha256:0e85c813c5d8b908bb4728b4072e073ae5c772aca799ab2a840c369abd3f7a70
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1814756790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba27a6375d261f1bff02c528433384f0a5efc14d811571b133566dbbf21976c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Wed, 05 Apr 2023 00:38:27 GMT
RUN Install update 10.0.20348.1668
# Tue, 11 Apr 2023 23:37:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 03:16:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 26 Apr 2023 20:52:28 GMT
ENV DOCKER_VERSION=23.0.5
# Wed, 26 Apr 2023 20:52:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.5.zip
# Wed, 26 Apr 2023 20:52:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 26 Apr 2023 20:53:00 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 26 Apr 2023 20:53:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 26 Apr 2023 20:53:03 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 26 Apr 2023 20:53:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 26 Apr 2023 20:53:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 26 Apr 2023 20:53:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 26 Apr 2023 20:53:39 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 26 Apr 2023 20:54:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ecfa9c953d28a9da9d422b57cd0361c57c44e1faaaed7e50a2537d1c29cee1`  
		Last Modified: Wed, 12 Apr 2023 00:50:33 GMT  
		Size: 376.6 MB (376573004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98474c9b39bb0e3a2d79dca81a90952011b65d1fa352021dacd30335d1bb69f4`  
		Last Modified: Wed, 12 Apr 2023 00:49:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9122c88a621359fadd2c1ab6702c4106dd74f6703813469a0911060138dfc8f4`  
		Last Modified: Wed, 12 Apr 2023 04:07:19 GMT  
		Size: 766.2 KB (766237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce906a77e57e58fd15c60b6b74df55d8d219f6860ce94a3a314c9e8f4ee6155b`  
		Last Modified: Wed, 26 Apr 2023 20:58:44 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0ffe1a779a224bcfaa7f5b479d42c58ac1223c1e543b6e5b2258e86d91542`  
		Last Modified: Wed, 26 Apr 2023 20:58:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8e3207c5d3f35edf9f1b67affcfdf97d98f86bda5fbeab265e97729fd10ba9`  
		Last Modified: Wed, 26 Apr 2023 20:58:46 GMT  
		Size: 17.6 MB (17589860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6f43a9a13d4c038a8f9b1d0210cf1543f2d4fb5d0cae0034b15955c9ddfeb5`  
		Last Modified: Wed, 26 Apr 2023 20:58:42 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e316ae6bb0a502c8aec4e12990338fe9c2c53fe8ad4624f7618ee5ad8e659b74`  
		Last Modified: Wed, 26 Apr 2023 20:58:42 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19703a78856ec16dc932152add0eccefdb287cd25f8a24024ab9a062b42db8b`  
		Last Modified: Wed, 26 Apr 2023 20:58:41 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342af7454ce546cb480236bc5f04372e0ac8acad1e91e15280c1501d3d72d82b`  
		Last Modified: Wed, 26 Apr 2023 20:58:44 GMT  
		Size: 16.7 MB (16704927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2583b2e1a77dbeed6b360eef3633d1b28a4ce08b2b2e0ab8ed07fbb6faf09013`  
		Last Modified: Wed, 26 Apr 2023 20:58:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25643d305e7a83e30b48450b6ab5e69dac4d0aa6cf81320d865d3fd481b9cc74`  
		Last Modified: Wed, 26 Apr 2023 20:58:39 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1e0f6787d9105302b38578f520fce4851943dfeb8ee6547602629050d9f8c3`  
		Last Modified: Wed, 26 Apr 2023 20:58:40 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065899044d761231d825984a2fa9342d4fbad9018a1863994f49d7c35ac1ffd0`  
		Last Modified: Wed, 26 Apr 2023 20:58:44 GMT  
		Size: 17.1 MB (17080988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.4252; amd64

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
