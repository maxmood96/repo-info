## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:e23c1097f4422e0afd160973bdf739969e3f554176a203e74c9516e578f93eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull docker@sha256:861ad32b4aea6ebcafe15263de5392e2b96e68ae72982bbe6c3ee5842a392d2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2736709359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b8a1ae2c2bd7da22c9fb3204f2d1906f3d638f0a4fe37d7f63041107380a9e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 02:41:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 18:19:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Aug 2021 21:14:18 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 04 Aug 2021 21:14:21 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Wed, 04 Aug 2021 21:15:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dd3b24b55401566ea01a5005138a23766b6b6408c2276b7ebd097da01de80897`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca81d46af1fb75d88c51bffddab081ffb30e74d3771ee61adfcad7c1b2c6298e`  
		Last Modified: Wed, 14 Jul 2021 18:21:15 GMT  
		Size: 369.1 KB (369149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261da88a9739468f39a6c5afea5001a7636ff158c9f6d3c55c781c7a5e25f03d`  
		Last Modified: Wed, 04 Aug 2021 21:15:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65914705f95c4725772744ad7f2007bde657f07e7e22b9fdd99ceee0e321b00d`  
		Last Modified: Wed, 04 Aug 2021 21:15:58 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649fb723a4e40f18c7aafb9c9da6b3cf4745259262599aad41308db2de8ed8c8`  
		Last Modified: Wed, 04 Aug 2021 21:16:09 GMT  
		Size: 50.9 MB (50889139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
