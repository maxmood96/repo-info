## `golang:windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:f6c7d4b8c744a5c6fad6b960c86c35de1e00f78c25e3ba9232b197fd17098dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `golang:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:2225d7c7c0cb9d23f6f3e5eb77284fe9e017fab2a77074d88665c918dbd9eae3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1617274557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70b500467b8263ab259ede71703c586a43980218edcdd7b00c828e4ab222665`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 10 Feb 2026 21:26:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 21:26:46 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Feb 2026 21:26:47 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Feb 2026 21:26:49 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Feb 2026 21:26:49 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Feb 2026 21:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 21:27:42 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 21:27:48 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 21:27:49 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:29:18 GMT
RUN $url = 'https://dl.google.com/go/go1.26.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9bbe0fc64236b2b51f6255c05c4232532b8ecc0e6d2e00950bd3021d8a4d07d4'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 21:29:19 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f0ce23bf20e4e4b723c48737da5a809eaa74eaae29a6baa0c98c3a7aaf662e`  
		Last Modified: Tue, 10 Feb 2026 21:29:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5701c59a7f8317bd28e0da7cfa531b9eb5d25b8a9b98d6b7047db31ce46d33`  
		Last Modified: Tue, 10 Feb 2026 21:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7b7d3ea42a0e191b8407a1b5b569e0b161fc76c0ab8011088b51b9c833623e`  
		Last Modified: Tue, 10 Feb 2026 21:29:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c79d245bad43d9d1c5771497a6134a98623f4fb016628394bc9ba8fabbe243`  
		Last Modified: Tue, 10 Feb 2026 21:29:27 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d030477899e7ce381c5decec028af460368c2cc35145ae71cb07c3dd1b77b1`  
		Last Modified: Tue, 10 Feb 2026 21:29:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f55fa67d9c26d94e30082d3a9ae25c258190674c0814a9cd9852948b469b33`  
		Last Modified: Tue, 10 Feb 2026 21:29:33 GMT  
		Size: 51.3 MB (51263578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514b7b61912d146534043f561a8897989b1194c2118d2bced912590ed91adde0`  
		Last Modified: Tue, 10 Feb 2026 21:29:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aec0225718c7856de0bc21f0aa9fbae0ea63d27564ad4199d9c5a11b7aefd4`  
		Last Modified: Tue, 10 Feb 2026 21:29:25 GMT  
		Size: 398.3 KB (398324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ef57c9d89a0c311d8d894f68dcfe663719e915ef6782371e1645c1a22598a`  
		Last Modified: Tue, 10 Feb 2026 21:29:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e285b7425b87af7e90a0d0539cbe391eb639586a7f533cef5f335da2e3969f6f`  
		Last Modified: Tue, 10 Feb 2026 21:29:36 GMT  
		Size: 69.8 MB (69841755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734603d9c9b5b37f9a3cb2516dd133366febab9cf9009d77e74aeffc5eb4b81a`  
		Last Modified: Tue, 10 Feb 2026 21:29:25 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
