## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:f06d2055c2e10f622d21e2227032bf6ecba6d0b6444ba17059b7e4c822a3c9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull docker@sha256:a2f5603c325e20bc846be7390f49f6dd7324812808f488f3e72bc9dde2f96d57
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2069734614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4603a9f3517e481eeec493fb07aa7eb2eeb779ce43cb2e34606b68efb8e8a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 04 Dec 2024 00:29:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:50 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:30:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:30:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:30:08 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:30:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:30:22 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:30:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c8c0d9c38caabebe3b73ab4c6eba8436f7f6362870802faa333902e268fda5`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2a635d22c65bd08f6832968bbaf45742dcea846553e69cd5fb73524892186`  
		Last Modified: Wed, 04 Dec 2024 00:30:42 GMT  
		Size: 488.7 KB (488667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec026becc11bd18a346a2f61ef141260e67d4d5c5275e554a9668f99a60e2696`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437214d0ea2a048e24dd206aecfeccb6ce5ccb823890b1ca8feb925dda2c9dd`  
		Last Modified: Wed, 04 Dec 2024 00:30:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4425edecd3624e76b516e6a14bf2381a3228b5b0cd0ca91f5b52242f0b761f52`  
		Last Modified: Wed, 04 Dec 2024 00:30:43 GMT  
		Size: 18.9 MB (18886052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8c997f46007664e2420e190bd026b2d3c615f2f092e4db109bcb66fbc2c230`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b692b1d417f77186832f783e691e3886c3b8473566614323f8090f22aaf482ef`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb109cfc2d9438feb076d8b232441c406096b2b98b39bdc3d6c8b71cff4a6f8f`  
		Last Modified: Wed, 04 Dec 2024 00:30:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76412645838ed469d125fe7cbb4ee913c5e077868700d13338ed009778d34bb4`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 19.6 MB (19644914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4314d510cc852d692dd9c73cb48da4c06607bf2426a12a710a1f7f23168cf6a8`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e08b405dd71ce49510066489c12e9c6d278bb87ddfce055c2ea7a51a7a1ea67`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61005e57942a2a801aafe59b869523568ec1b842f394fd1d5881b321422de2`  
		Last Modified: Wed, 04 Dec 2024 00:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627830bfad7c6a2e11305e97939175b7844471db27f68b649091073c61f7f394`  
		Last Modified: Wed, 04 Dec 2024 00:30:40 GMT  
		Size: 20.0 MB (20049522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
