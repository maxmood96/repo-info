## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:264ad4d93e724c22bc25a17032932a3653c16183d65d86e7e48b21c967c5e957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull docker@sha256:79fc8be3bdef5064ef7f628bd5a2548c7089f13e1881e6a3df8b1361779b635e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169099195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9b435124756dbdd7bf480e8f93bbe634cb186b493170830a565f72383ca5a8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:00:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:00:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 29 May 2024 23:00:50 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 29 May 2024 23:00:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 29 May 2024 23:01:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 29 May 2024 23:01:03 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 29 May 2024 23:01:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 29 May 2024 23:01:04 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 29 May 2024 23:01:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 29 May 2024 23:01:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 29 May 2024 23:01:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 29 May 2024 23:01:16 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 29 May 2024 23:01:26 GMT
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
	-	`sha256:9d06f489df5a98bf931107ca17873f52903ad25b3771501dbf8b8e5973b9efc0`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55ddedd2336c073741d5a65a7d90aa4f56004df8e58cb22fbe3d914f912e8ef`  
		Last Modified: Wed, 29 May 2024 23:01:36 GMT  
		Size: 348.0 KB (347987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda49ee8486ae33af9526575b3575484c0d607cebfa18f6d3e89b7a674b645b7`  
		Last Modified: Wed, 29 May 2024 23:01:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fbd53809eebb47e5d35e9af326aec7344bfa51dbd68a266d960a7bb0f1db44`  
		Last Modified: Wed, 29 May 2024 23:01:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14be890adacbd78fe7ee0cdfd8f3f5500dc758d3426ce839bd81a6c97ceed1e`  
		Last Modified: Wed, 29 May 2024 23:01:36 GMT  
		Size: 17.5 MB (17520778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e39e24b786228352a0cfd7fdaa52f6b4f0d9c0ad645181f1d7d69559f8a3091`  
		Last Modified: Wed, 29 May 2024 23:01:33 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a82d4c2e934bcd9968ebccca5d778323adc306dd7b18d930a504fa8d5dcda2`  
		Last Modified: Wed, 29 May 2024 23:01:32 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda2d1da628e18418ad64bbe3b5f14336bc4196a3f34e7b6687e5ce234d69565`  
		Last Modified: Wed, 29 May 2024 23:01:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6d01b0f9466d165e2f0f9ab85cf2b98c5523215b341f91bc6d198bfc10bc2`  
		Last Modified: Wed, 29 May 2024 23:01:33 GMT  
		Size: 18.9 MB (18920341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f8021ae0718394866c6d61a28832cca3e5f15fba195b4380a54983932c989a`  
		Last Modified: Wed, 29 May 2024 23:01:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a222e93e4e81fb120f48757d40f3ccfd9a75a24aa2339d904216179df9e3fe`  
		Last Modified: Wed, 29 May 2024 23:01:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865dfc74d79ac9564b4816014a4559376b358a6b7df3ec4f01c1a569a214d110`  
		Last Modified: Wed, 29 May 2024 23:01:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b26802744d6e6573600707fe24398454ba8ac18e9450fbd0569d8562a1d72f`  
		Last Modified: Wed, 29 May 2024 23:01:33 GMT  
		Size: 19.6 MB (19626842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
