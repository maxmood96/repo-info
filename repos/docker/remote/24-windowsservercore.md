## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:6b17ef4c6ccfc6e77ae928a0cf6f521f002874a2b9a71032c2f651db79138ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.2527; amd64

```console
$ docker pull docker@sha256:c3557d30dba459d715800b375bc987d55eb912f4e771f1f9c073fc4ede050bd1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2174727542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b0c1d89e3e0eaaf1f24bb083500e551c08cfa0c1bdf927c47e182c58864f5f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:08:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:08:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:08:49 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 12 Jun 2024 18:08:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 12 Jun 2024 18:09:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:09:01 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 12 Jun 2024 18:09:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.windows-amd64.exe
# Wed, 12 Jun 2024 18:09:03 GMT
ENV DOCKER_BUILDX_SHA256=f9285890c7d0b68ed36a07d4db062bfdc8db2059fa59a812cdbef438cfa3f774
# Wed, 12 Jun 2024 18:09:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:09:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 12 Jun 2024 18:09:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 12 Jun 2024 18:09:12 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 12 Jun 2024 18:09:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7540fb47052b6eeaf079830d23ddab5a5fc55de95e552628a3969379b8e4acac`  
		Last Modified: Wed, 12 Jun 2024 18:09:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8de19414831e4b735ac3fdd8ed5c8498148d5bc60a5884dd2aae86538b152d`  
		Last Modified: Wed, 12 Jun 2024 18:09:25 GMT  
		Size: 354.2 KB (354176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acc04578f4fe93d39c139006617a55358774342b46bd4a55814aab1c74ac960`  
		Last Modified: Wed, 12 Jun 2024 18:09:24 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42c4c8dcf3d2e19018912f8f75a8ba23c621622b142a64939717f2f0e3cc3ef`  
		Last Modified: Wed, 12 Jun 2024 18:09:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8c03ce6becaafbb0e9d2865ecc72321b5f34a3ad03648a20c8e002fa107b31`  
		Last Modified: Wed, 12 Jun 2024 18:09:25 GMT  
		Size: 17.5 MB (17529934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba616f65a288aab9af151acb02fcf7f8656d6c95e2c4dd2f976752eecc018dc`  
		Last Modified: Wed, 12 Jun 2024 18:09:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51ebd2be1eb358ca5d2a1ed82aed8ea64d324c37223264e3d1f2a42c463cda`  
		Last Modified: Wed, 12 Jun 2024 18:09:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d810e186f3e6cb646a2d170e75c920d50cb7490f1b83f4d2739f3328207d85`  
		Last Modified: Wed, 12 Jun 2024 18:09:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671ae283b706970adb6e7dd0f5f057a7beaccbde96d8655b638e80fa8bf0e26e`  
		Last Modified: Wed, 12 Jun 2024 18:09:24 GMT  
		Size: 19.0 MB (19019645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aee651130886086421534541501dd341caaf0234c35b3164639b3c8474338f`  
		Last Modified: Wed, 12 Jun 2024 18:09:21 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac72ace93d6313405e9c07b4b9e0969aa3d64ad766b8bfaf87169116a8445acd`  
		Last Modified: Wed, 12 Jun 2024 18:09:21 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa946ac4ca14d56e22c7ea755a64967be9fbf314569f1baa9809717c199a96ad`  
		Last Modified: Wed, 12 Jun 2024 18:09:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39b2c7545c420f557d413ff0b9127e60449d03961c912002e912fc2c854d470`  
		Last Modified: Wed, 12 Jun 2024 18:09:24 GMT  
		Size: 19.6 MB (19633526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:94b3252430677009d968e734aef81e3e9946c2c9a36928f49fb346697a4065d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2277305286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18bf43a84a104f489ff6fea93023db33398c3226983e18e5632c6c21969be7c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:19:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:19:38 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 12 Jun 2024 18:19:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 12 Jun 2024 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:20:03 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 12 Jun 2024 18:20:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.windows-amd64.exe
# Wed, 12 Jun 2024 18:20:05 GMT
ENV DOCKER_BUILDX_SHA256=f9285890c7d0b68ed36a07d4db062bfdc8db2059fa59a812cdbef438cfa3f774
# Wed, 12 Jun 2024 18:20:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:20:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 12 Jun 2024 18:20:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 12 Jun 2024 18:20:26 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 12 Jun 2024 18:20:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d68ad59a79756a4a4e312768d9a65248b188b938ea4d09717c07a51ebeccb2`  
		Last Modified: Wed, 12 Jun 2024 18:20:55 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d60dc9c7185e1d64639b795412bb412158bf0e1b6bb5d46687328b94dd977a0`  
		Last Modified: Wed, 12 Jun 2024 18:20:55 GMT  
		Size: 471.8 KB (471823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d2a92176fa38ae94679881c41f694fda370e15e4fbc2a72def7aad944edf37`  
		Last Modified: Wed, 12 Jun 2024 18:20:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085d856c90d4d62f2be0b329a12a4dbb0b9c496a5832b5fd52a0eabbb6df1297`  
		Last Modified: Wed, 12 Jun 2024 18:20:54 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2000f436ebc6a5c62d30926b048a7010634f6f831fa69c038ba62ad2a05578e1`  
		Last Modified: Wed, 12 Jun 2024 18:20:55 GMT  
		Size: 17.5 MB (17518066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93847beceb056d2eb680aaafbdfcec7f96ce7675db630c7139d7d9bc2a59b0df`  
		Last Modified: Wed, 12 Jun 2024 18:20:53 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0161a2f05b19d94a2d165675e79fce0bf9343713f143f4ba1fcba3ef63e7eda0`  
		Last Modified: Wed, 12 Jun 2024 18:20:53 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e046f834b485d1d4ccb2db7418858110cd622c793eafbb4b17b0e09f21c9ec`  
		Last Modified: Wed, 12 Jun 2024 18:20:53 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abb18aad4762c3b4b966306b024908da742a995c73223f43d41e92f0e4e1c5b`  
		Last Modified: Wed, 12 Jun 2024 18:20:54 GMT  
		Size: 19.0 MB (19007373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1f23092fbc2ab5b88fba3306d7f595c1aafdc4f7e371bd65b8a1a22fb31268`  
		Last Modified: Wed, 12 Jun 2024 18:20:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e152d5860d248a0bbcbe171197bca3e640a024c1d4fdf96e07373ebd30c6a9`  
		Last Modified: Wed, 12 Jun 2024 18:20:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46175a31a0fdd1cd27d921679581faa09aaa13725fc65c1f0726adc09108628d`  
		Last Modified: Wed, 12 Jun 2024 18:20:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407206f78f5c5516b0d6ed6d8c5ea864233a814dc80c0a83141ba6e7c812903f`  
		Last Modified: Wed, 12 Jun 2024 18:20:55 GMT  
		Size: 19.6 MB (19615160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
