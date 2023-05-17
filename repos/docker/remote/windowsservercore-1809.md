## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:665b4c02c553f700f3903f0f5ac07ad8b6bd51bff964865f0fb9d1bfa704dd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:fcb85505ec865447d0aed1b5bab48a698051ff070db02daaa5bd870a058758ef
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123337444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edeceb20c70d9069b5a0fc3b8d4dd79ef4e8f8f20215655f7b3ed669f6d5655`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 17 May 2023 00:16:49 GMT
ENV DOCKER_VERSION=24.0.0
# Wed, 17 May 2023 00:16:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.0.zip
# Wed, 17 May 2023 00:18:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 17 May 2023 00:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 17 May 2023 00:18:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 17 May 2023 00:18:11 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 17 May 2023 00:19:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 17 May 2023 00:19:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Wed, 17 May 2023 00:19:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-windows-x86_64.exe
# Wed, 17 May 2023 00:19:30 GMT
ENV DOCKER_COMPOSE_SHA256=a98df8912c7a5cc7be00c1819a920e0ecdd5e2a7402bb390606c7f3f3b28b24e
# Wed, 17 May 2023 00:20:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb10affc8126734dd238241f8b3d9b71ceb5438dbbf84ee566a608cabf606cf`  
		Last Modified: Wed, 17 May 2023 00:24:26 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2fa9db965b5b82349ba01960f80952db3950276056ab9d6bb71b6d03285657`  
		Last Modified: Wed, 17 May 2023 00:24:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488def41cc4d70f5f7d926c623387e4f9de65a96a76a26c93c69f8793794ff52`  
		Last Modified: Wed, 17 May 2023 00:24:28 GMT  
		Size: 17.5 MB (17474717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19e5946eb44fb1d2408597a8aa7c915a48a67152dd3580b096f2a2ef09ebe56`  
		Last Modified: Wed, 17 May 2023 00:24:23 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba14be958dafdb9c8bddb473c4d9f6a413ea8000553bc33052a094f072e7c81`  
		Last Modified: Wed, 17 May 2023 00:24:23 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7ee67a691dc1e667d0b7f5a05c35d769e974da4d0610c7b33baeafff6e747`  
		Last Modified: Wed, 17 May 2023 00:24:23 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af36c6acb9577a67a110ace2b0eceb25a9bc040e3f0b139c60365116199d177d`  
		Last Modified: Wed, 17 May 2023 00:24:26 GMT  
		Size: 16.5 MB (16489581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4666710f418290fa73b37425fd70664b5225d7f3db0911d6fa516b156ed9e76`  
		Last Modified: Wed, 17 May 2023 00:24:21 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc16c515a2893706cf28df91b18301845e669020c787da40e3829b4b5e7061`  
		Last Modified: Wed, 17 May 2023 00:24:21 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7db07e583aca75ac9f8e3c7a696c79216b441ca799ea4aea1e19d81f8efb9e0`  
		Last Modified: Wed, 17 May 2023 00:24:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ac593855ec5ef54040bdd7847c5dd2e71fda55d1f38b7e67441fa4ed0fe0a6`  
		Last Modified: Wed, 17 May 2023 00:24:26 GMT  
		Size: 16.9 MB (16873694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
