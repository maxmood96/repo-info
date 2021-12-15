## `golang:rc-windowsservercore-1809`

```console
$ docker pull golang@sha256:3010aa8b9447b5c727126c5655a08f5b305cd4a539fd6e865d6fc355e6ad5c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `golang:rc-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:7ff1f2b9b7ef8b12693f83eaa6203fb597fc1e8c753833d89467441c7752da22
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2886417754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c442b97961db89da58b3267a31e96465b82be8b7d2ea005387db661066bb19ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Wed, 15 Dec 2021 00:45:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:45:53 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:45:54 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:45:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:45:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:48:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:48:32 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:50:15 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 00:50:16 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 00:53:49 GMT
RUN $url = 'https://dl.google.com/go/go1.18beta1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3a43ab4ec28eee6b10fd412a055724d962227f1c27a78960d6d229d741f8353d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:53:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aabd70b2463e8240ac41c7d726f6fcfc25424b74f20bb5e8642dbb9bc2b789c8`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8639e414e28c147782b979f15c11cacfe3670dc5a898f9d0fc95ebadeb3f5a`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a032d0c95307404bb3f5ccd3d69031082f2a3a1ab0eadd1ce3b12d931bd3e6`  
		Last Modified: Wed, 15 Dec 2021 01:53:54 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ddbbfd5905588817615b135bf7431f7a67d054028d23d234b326a68097b39`  
		Last Modified: Wed, 15 Dec 2021 01:53:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22bfacbdbf128875fdbf7e39f4d3b2030fe3e310d9069f2a55924a2cf3e91ac`  
		Last Modified: Wed, 15 Dec 2021 01:53:53 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d739bb0bdf88e33c8c46b5751f6dcdf79a57d123fc0a559e3e189924cf4c`  
		Last Modified: Wed, 15 Dec 2021 01:54:00 GMT  
		Size: 25.5 MB (25463347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e73a67af47aee0d209f8dfd5ea371efb1b0c5205c8d5be95680c9675c302cb`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9036358af62e5d57f75caa56f99c1236c8bd7a61e2dd902f023c4ab45877aee`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 341.0 KB (341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3bcf72ba9a6930431ae06b4db502b15984779b5ac966b6a9d3344d5effa312`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ebb35ce0ce1792d2209c4e10ac146af70fb711d87e535d787ecbc107f3aefc`  
		Last Modified: Wed, 15 Dec 2021 01:54:29 GMT  
		Size: 152.0 MB (151997368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee95d777af991f26dff195dbec4239cd84385837257a40d55b12dff07d93f8f`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
