## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:37ab941648d8b1f9edd52496d9c037bb2b8ca9a9790173015706eb1afa067db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.405; amd64

```console
$ docker pull docker@sha256:8077c62078f4481e46059306d95470c64e7b32cfd0778fe146839ff98f316dfc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244828735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111bb52d01d2b46191751cdf6b050a755983cc66d13975fd0ce6a1064b7b4d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 08 Dec 2021 01:54:07 GMT
RUN Install update ltsc2022-amd64
# Sat, 18 Dec 2021 00:09:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 08 Jan 2022 00:14:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 08 Jan 2022 00:14:19 GMT
ENV DOCKER_VERSION=20.10.12
# Sat, 08 Jan 2022 00:14:21 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Sat, 08 Jan 2022 00:15:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d1d74adc6a92e44b3cd592ec9459f1fff926eaf6fc20bb7526360bec71aefc0`  
		Size: 939.1 MB (939072515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5bc74beb7593c703ac99379d225f3a9a445549cc06a3fe18f44e356a45f225f3`  
		Last Modified: Sat, 18 Dec 2021 01:18:31 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d54f3cedaba1daf96a5b2033a05519d03375f2395c4b40484ab4faf25daed06`  
		Last Modified: Sat, 08 Jan 2022 00:15:44 GMT  
		Size: 633.8 KB (633765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c456a522d5894ced0d26a67dd465d1006d64822e3c6640dd2133e219ec25edd6`  
		Last Modified: Sat, 08 Jan 2022 00:15:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675b1bf3efb67d477eb16d5de78451d639a67e1f6dd0bef707c9e8708932e5d6`  
		Last Modified: Sat, 08 Jan 2022 00:15:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d9437c8b27e1ab1588cd93ebecbc461569488f4d992b33573c6287ec9822f9`  
		Last Modified: Sat, 08 Jan 2022 00:16:44 GMT  
		Size: 53.4 MB (53419120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
