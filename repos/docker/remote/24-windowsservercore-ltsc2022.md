## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b7f625062cbf91ced14dae914283aa350584533b4e8124ec9fb9d2a568174ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull docker@sha256:22ae3509f6dc12d22c574c17090cc3e94907739851bad016154a2718514be5ea
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2168985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8957b44034cdd95ba000b281cb033b1039253c55142aebd2f45369005293f4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:51:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:53:15 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 15 May 2024 21:53:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 15 May 2024 21:53:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:53:36 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Wed, 15 May 2024 21:53:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Wed, 15 May 2024 21:53:37 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Wed, 15 May 2024 21:53:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:53:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 15 May 2024 21:53:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Wed, 15 May 2024 21:53:47 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Wed, 15 May 2024 21:53:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe05c32199b41220d6f9930f50de413aca29b732946660a7ff693f2b29e10ee`  
		Last Modified: Wed, 15 May 2024 21:54:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154ee6ec80ebb8a46b0c364551196b3f294a1b375a7951a91cc31cf5d73c5718`  
		Last Modified: Wed, 15 May 2024 21:54:06 GMT  
		Size: 349.7 KB (349663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3a08019200ea7b2193c9ab2bec555bb0684004eab3e9efc3493d389f442f6a`  
		Last Modified: Wed, 15 May 2024 21:54:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a241fc08c6793d2f9f2981618cb565cc482925a4ec1010436ce22caa54e5780e`  
		Last Modified: Wed, 15 May 2024 21:54:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f257e7bf19b5f29d5f2c99daf868a76e73e1463aa1b653c1e391323011debe`  
		Last Modified: Wed, 15 May 2024 21:54:07 GMT  
		Size: 17.5 MB (17492643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc1d9c78007720b03e118d2c0984c441e02b58da18dc19e34226f73ac0aae56`  
		Last Modified: Wed, 15 May 2024 21:54:03 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849882ca3ccb6002866a2833a1d2e782a3e3136a7c5a03b0300c15cbed56c14b`  
		Last Modified: Wed, 15 May 2024 21:54:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60d3dce71d60fee20f24e6d7432aafc39c9c40b3558c0541cef035ca8bcdb26`  
		Last Modified: Wed, 15 May 2024 21:54:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48289ef2719f5eb6447168cdcc39bdd92d6a2a43f3ccb676f5bf16d8f3ceda6d`  
		Last Modified: Wed, 15 May 2024 21:54:03 GMT  
		Size: 18.9 MB (18874843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae5c64ca79862a5808af28786ef7171dade14779093e1832e5147bc384dc16d`  
		Last Modified: Wed, 15 May 2024 21:54:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c5bda1b363dad65bf716fd549091f6558f3b3000ff7dce04f37c4e0e9f3a86`  
		Last Modified: Wed, 15 May 2024 21:54:01 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6848f9a148cf694c795aa562e19af06e1640e2878453909a325c185ed1ed7e`  
		Last Modified: Wed, 15 May 2024 21:54:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fa7f7b0c45fe055018a950624e434644e6948ede2786f13c0a7eaba9a8ef8e`  
		Last Modified: Wed, 15 May 2024 21:54:04 GMT  
		Size: 19.6 MB (19585790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
