## `golang:1-windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:9ad4b09283c237a79e4e933dee14be5b533cc77beaa022644285dd5b51c79134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `golang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:b6af61b322abcc1a226323244997ef584b3a4168c1854aa9847b2a48063ab608
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1609923828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c977248f255a0d81e6d3f3ad0b63c1ea335fe45bda5ff90698aa3ac4579e4d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:58:08 GMT
ENV GIT_VERSION=2.48.1
# Tue, 13 Jan 2026 22:58:08 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 13 Jan 2026 22:58:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 13 Jan 2026 22:58:09 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 13 Jan 2026 22:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 22:58:22 GMT
ENV GOPATH=C:\go
# Tue, 13 Jan 2026 22:58:27 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Jan 2026 22:58:28 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 22:59:45 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 22:59:46 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed7aff12eed6d468fbfd98c5cdb643204448d37e6b4376b4863d715fe54870b`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b4eaaba04e227dbac7e450ab1ffdf3d3905685ca42d4695f97547c52406b6f`  
		Last Modified: Tue, 13 Jan 2026 23:00:17 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa85d051bb301e618af33b90c6e47848cb7837668eea10db25dd8f643e5dfa48`  
		Last Modified: Tue, 13 Jan 2026 23:00:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ee91dda9a8bf0cab01f5453eaa5a87fd7563fbe148524b1a6ded50a3b9cfd3`  
		Last Modified: Tue, 13 Jan 2026 23:00:17 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1be918c8b8754e23c65ffd13c32d07ada30c95259c490d454e069bb0658164`  
		Last Modified: Tue, 13 Jan 2026 23:00:17 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f862c0b39185a8ab6f92bdd1018c36e7d7c1284c73686ff39338b0a950f4384`  
		Last Modified: Tue, 13 Jan 2026 23:00:21 GMT  
		Size: 51.2 MB (51214988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8e7a2a6caced74227a4dad6fa920e503157687d6583a5251698bb073d87490`  
		Last Modified: Tue, 13 Jan 2026 23:00:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e21dbcb1b42e349e4ff1fb424b5afe3d0cb5ca87a916468663acade53f4f3e`  
		Last Modified: Tue, 13 Jan 2026 23:00:18 GMT  
		Size: 354.2 KB (354198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2753748a83e4fedd8c435ed91bcddf72a3a9c04c0de200bdb981c12dfd88ea5f`  
		Last Modified: Tue, 13 Jan 2026 23:00:17 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d052020f91437d564377b6fbf8b985ed8ebdbfc973a73771acbc96b15d46e9`  
		Last Modified: Tue, 13 Jan 2026 23:00:21 GMT  
		Size: 62.6 MB (62583576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e3ee39dc863f2291b15c37f3b1c8615b0b8262ab151c897642c392fd13bd73`  
		Last Modified: Tue, 13 Jan 2026 23:00:17 GMT  
		Size: 1.5 KB (1469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
