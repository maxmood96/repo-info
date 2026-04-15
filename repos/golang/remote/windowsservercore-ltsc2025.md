## `golang:windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:58f913b555d050e4ae2a9c6e4628eca8065d7186356cfd33572d46fd3cf153c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `golang:windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull golang@sha256:94f1961ff53812ac6f554fc5fd6d1f9c6986a3b6edf6512d910acce9729b2964
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251428455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec38fab49af31bece8746eda2b2b9fcffb0556197a0c57e3fb9ae9c96be18b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:11:49 GMT
ENV GIT_VERSION=2.48.1
# Tue, 14 Apr 2026 21:11:50 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 14 Apr 2026 21:11:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 14 Apr 2026 21:11:51 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 14 Apr 2026 21:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:12:04 GMT
ENV GOPATH=C:\go
# Tue, 14 Apr 2026 21:12:09 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:12:09 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 14 Apr 2026 21:13:25 GMT
RUN $url = 'https://dl.google.com/go/go1.26.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '98eb3570bade15cb826b0909338df6cc6d2cf590bc39c471142002db3832b708'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:13:26 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00876c5c306a40bdb91b29e1bfe5c5e3a30957345f5b4217492950932921f085`  
		Last Modified: Tue, 14 Apr 2026 21:03:21 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ab6f7f8c04a918d6984281136988db80e26d2e49e506c24235a6aa24d3ddf8`  
		Last Modified: Tue, 14 Apr 2026 21:13:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9a4de2d156c81a0b97862c3aab31aed462414093a7a3548c0e075dbff4df45`  
		Last Modified: Tue, 14 Apr 2026 21:13:32 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905977893c27c80019254fc21606d27924fc7e8f15995ca1e93d995d0f9da1e1`  
		Last Modified: Tue, 14 Apr 2026 21:13:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b11d045724382783805a4ed4a39e0438de91e10ce9ca26c4c1386c8c1a42022`  
		Last Modified: Tue, 14 Apr 2026 21:13:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6517fa67870dec0ffc5542cea5ab7d6f5965077f9b323899b2c9e3c769823b2e`  
		Last Modified: Tue, 14 Apr 2026 21:13:38 GMT  
		Size: 51.2 MB (51227687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0c782a756fd5efe99734cebd326bfa111492e8514da6ba7ff44f2f23b0781d`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897c264ceb6ee8f252b0fdd9730a6339aa994740a00c6ecc3702353781a65dd2`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 359.4 KB (359353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afaf9528a576024002874bdb07610060adbb25dcf8cee62e667f97304a75e6a`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd318c5f8d24379da8ea97d3b862c1a1c3fe17f62a8c3168da4a9fdccbcfa1a`  
		Last Modified: Tue, 14 Apr 2026 21:13:41 GMT  
		Size: 69.8 MB (69844776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccfb531c02a788d97bfa192c0263ddafe73165dbf8bb40ea3cc1195581d6fe`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
