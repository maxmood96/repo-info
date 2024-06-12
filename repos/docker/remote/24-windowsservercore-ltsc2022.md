## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:935c627068aee0a78ccf75a46d75cbcc25c321522dec5b3cfda2cbaa1d9b4a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

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
