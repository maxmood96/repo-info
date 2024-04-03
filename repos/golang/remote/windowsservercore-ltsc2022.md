## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:15baaa5df7274dc5433324519f66fd14fb1a0dd8c0053f963c09a450161f6493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull golang@sha256:7020c0599040db3af8b3f6f175234a9e053ef8da2873446187df041b06641b15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d488909ca3f4486b1a925e0039af9e5f2c727ce47e016329cedafeed5a9d37`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Apr 2024 16:58:19 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 17:00:56 GMT
RUN $url = 'https://dl.google.com/go/go1.22.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8e581cf330f49d3266e936521a2d8263679ef7e2fc2cbbceb85659122d883596'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:00:58 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d79776ef4d83b11046bda589b9a081148d462baca2cd21e4b5451a7d232d112`  
		Last Modified: Wed, 03 Apr 2024 17:23:47 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6cb079c18ccf3ede2d3e52e97e247aecd16bd0274cefd9a9091fe20a60607c`  
		Last Modified: Wed, 03 Apr 2024 17:24:11 GMT  
		Size: 71.7 MB (71716254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b269856c3f42d0b59fa3ea2b702b5ecb6ece79c96be857736f42732d536b90bf`  
		Last Modified: Wed, 03 Apr 2024 17:23:47 GMT  
		Size: 1.6 KB (1563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
