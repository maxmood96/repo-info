## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:20-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
