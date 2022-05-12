## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:44251ae4b6e381ac726b35292cd0cedc2c9273e3b83991b56eca7290f59ee4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.707; amd64
	-	windows version 10.0.17763.2928; amd64

### `docker:20-windowsservercore` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
