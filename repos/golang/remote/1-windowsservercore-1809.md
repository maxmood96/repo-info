## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:634aec306c155014666909ffc0a38bed687a8c4bd009007fd25357bf5b2276c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull golang@sha256:e573a6bfeb48bace6d3db6336dc0c2d5bbc0bd2ba4d6ee068c9ea75201c4babe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2225352781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8f2e6faf81174ec2771aa9d6970ad59b3e0c168aecb1e53686680c372ae596`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 04 Feb 2025 19:32:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Feb 2025 19:32:38 GMT
ENV GIT_VERSION=2.23.0
# Tue, 04 Feb 2025 19:32:39 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 04 Feb 2025 19:32:39 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 04 Feb 2025 19:32:40 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 04 Feb 2025 19:34:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 04 Feb 2025 19:34:11 GMT
ENV GOPATH=C:\go
# Tue, 04 Feb 2025 19:34:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Feb 2025 19:34:20 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 19:36:45 GMT
RUN $url = 'https://dl.google.com/go/go1.23.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '53fec1586850b2cf5ad6438341ff7adc5f6700dd3ec1cfa3f5e8b141df190243'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 04 Feb 2025 19:36:46 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82eb40173ea3287a6a5c3f160da83734526554e7aee77609b0e68a67f81bcd6b`  
		Last Modified: Tue, 04 Feb 2025 19:36:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fc4b408102b6b0f07b13baff385495fcbd880c6744f6038fbe3e3a853bcb04`  
		Last Modified: Tue, 04 Feb 2025 19:36:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ab4d639aacbfa3fa19028e1f5bd64a7ac8c1051b94c98f81839ebd961e82b9`  
		Last Modified: Tue, 04 Feb 2025 19:36:50 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00868d1da45d0520206b7f79d61ea5855b16c61ea6bbeee3e16a203cb91ad92f`  
		Last Modified: Tue, 04 Feb 2025 19:36:50 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0178b2c6f9188abf3b85d474689b9cf472f7be4c1f934bc9c85000c4c5b9e1`  
		Last Modified: Tue, 04 Feb 2025 19:36:50 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f776de48a48682671bdaefed422db654408d7957e8667e047f164d58399f748`  
		Last Modified: Tue, 04 Feb 2025 19:36:52 GMT  
		Size: 25.4 MB (25433046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c65c7a56852f8dd3bdee3039cb226700ce8dcf52e70faf0472da262b6d6064`  
		Last Modified: Tue, 04 Feb 2025 19:36:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1db18a7157796e70b40866650b83768c327e752c4bd524efb461c367f1967aa`  
		Last Modified: Tue, 04 Feb 2025 19:36:49 GMT  
		Size: 344.0 KB (344030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637efa3754a9e181df6568f33803c876c1995e8a5ab178bba82eda8ef70db9a7`  
		Last Modified: Tue, 04 Feb 2025 19:36:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5565330f5da214b8acc86342818066b88f38e6633d04f357ca9daefda19ed0`  
		Last Modified: Tue, 04 Feb 2025 19:37:01 GMT  
		Size: 77.4 MB (77352974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f75ad3719ed83c184730c5a9b9fa96d6ce9aade1ca38aac333025bccae77b28`  
		Last Modified: Tue, 04 Feb 2025 19:36:49 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
