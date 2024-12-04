## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:a9b533ad3897a104820d026bf803f1961f7a5878421714a612247124d0acef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:8f9c48d09df59573b09228e9dbfe3c594742424cae7426a5a35e8cc7aa3b36c4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311481903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97457ae6f523445fb75426553bfe303fced59f9220ae078d7e4c87715d45fc5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 04 Dec 2024 00:29:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Dec 2024 00:29:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 04 Dec 2024 00:29:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Wed, 04 Dec 2024 00:29:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:33 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Wed, 04 Dec 2024 00:29:34 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Wed, 04 Dec 2024 00:29:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 04 Dec 2024 00:29:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 00:29:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 04 Dec 2024 00:29:45 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 04 Dec 2024 00:29:52 GMT
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
	-	`sha256:7a8cf801ea0b73e0642e0b4ce32164423c74578a15913ce3c1522455550a51dc`  
		Last Modified: Wed, 04 Dec 2024 00:30:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce32181c8d548c5f3d5c7f21d6c1b4c138f11930d3b7148aca72a20670d60ef8`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 368.7 KB (368664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6383050bfd01e5a60b58e3afe6ec6d1727c6c572e4ae362fb203f6547a3d36ba`  
		Last Modified: Wed, 04 Dec 2024 00:30:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3b0dbd135c9afcb2d3a67cf6793d6b0105763d826d910b5be9f56306cf0699`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b486b2b85df328dd041bb776e8189405348f40be4026b361979170287dbf83`  
		Last Modified: Wed, 04 Dec 2024 00:30:04 GMT  
		Size: 18.9 MB (18895345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a797eeea5ccf96cfa615e788b8c83761178eaec7b197ce58af1f7617f1f47bf1`  
		Last Modified: Wed, 04 Dec 2024 00:30:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d270eee49201dcbef13d72f80110cf8520fe216813b9dbbd77a7bccb0671cb`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa40b1420cb32241d443d54fcb9c66295fc1614b803dd2b64b85b8045e88f83`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdec4827b0809606345cd494f89179f7a6a4bfa53c66de763707cc7a8a51a69b`  
		Last Modified: Wed, 04 Dec 2024 00:30:00 GMT  
		Size: 19.7 MB (19654760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b138a6306b3265d89ccf4b591674811e587f9f015dc00aa72e46fb90a33a43`  
		Last Modified: Wed, 04 Dec 2024 00:29:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ff6d4acbb626052eaf329cc2b79f40f95d3ea7e6c9dcd9fc0096b1468e0438`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c8eb7eb52107738c2ba26a34591f105b95d2313a00e6000ae6e8f6722398e9`  
		Last Modified: Wed, 04 Dec 2024 00:29:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff881f29ea45eed545b1bee34dead2669cdfd435ecee8af251e2c4265367496d`  
		Last Modified: Wed, 04 Dec 2024 00:29:59 GMT  
		Size: 20.1 MB (20067322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6532; amd64

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
