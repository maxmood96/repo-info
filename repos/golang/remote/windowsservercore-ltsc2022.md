## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:2ff51d992fd367c36cc99134abc6441bad62d8fee7d0d8f8463fc6c7ab751a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull golang@sha256:f50a62a024e851fe1d9684010d18b6dd3db48288cfeeab250726d1e7423e66ad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404810921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89491f6a50d6ba7c3221a93691258c9181e343d5d9ef694d4f372a183832f4fe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:59:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:59:51 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Apr 2025 00:59:51 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Apr 2025 00:59:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Apr 2025 00:59:53 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Apr 2025 01:00:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:00:11 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 01:00:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:00:18 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 01:01:28 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:01:29 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345c6a4265223fc889b761aac9cfe0402e9e7ba36ff92c9041a7e01af827238`  
		Last Modified: Wed, 09 Apr 2025 01:01:38 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c0bc025e49b96a98e158aa3628492681560a9b66371cafa674a13baffb2a0`  
		Last Modified: Wed, 09 Apr 2025 01:01:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b147f042085899dbe15fbcbc97b157dadc056218a793c091f8da26fc35b080`  
		Last Modified: Wed, 09 Apr 2025 01:01:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88330bb9180b967b8f1ddf3ebb374d770def047428f52d4735e71e7a99e5c150`  
		Last Modified: Wed, 09 Apr 2025 01:01:36 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414252e9ec98fb3ee28bc6c024d35e323011170f9662b4e95d501f8494e2cb7`  
		Last Modified: Wed, 09 Apr 2025 01:01:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ad7c06935374ce4f49b6691c8491cb0a04fbe87314498c7a0eb0fc56be2052`  
		Last Modified: Wed, 09 Apr 2025 01:01:42 GMT  
		Size: 51.2 MB (51209846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bce03b9acb963d134c3f4e69e3472732ebccc067518a62e69db5353b82f613`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3181b8f7ca8d16a5332510aa93def630fd3ea6b003489ed120843ba48a1c9bbf`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 344.1 KB (344106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de3a3af62347b91455ddc9ebaad5b04aa71cb5c9a01aba9f633e99f023e0cc`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242c423f37cbf4329c08684df4d886ef6f2fe1db3fb69c651eff20ee85a345d8`  
		Last Modified: Wed, 09 Apr 2025 01:01:47 GMT  
		Size: 82.3 MB (82250859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d64572c273c292cc9d00c8b1835d833c74c4589a70b2fd6536b3220a1c960`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
