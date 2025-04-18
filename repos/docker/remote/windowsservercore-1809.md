## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:326ac27545ba0438a8e7108c0385c6d32985cf8b0949d07389e38b03eed5bc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
