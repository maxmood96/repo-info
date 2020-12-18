## `golang:rc-windowsservercore-ltsc2016`

```console
$ docker pull golang@sha256:b63d7ccc9d72b571a80fb124c7aa3bb4fbbdad17017ef3150a65b333d326e549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `golang:rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull golang@sha256:20ba4aea9b383690abfa96755842ebeccc016e0e30f9023394925d981260d4d0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5921501875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb83e063b7b856fca0e4f6e0218a921cf760d834939112abc2cd892d2054346a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jul 2020 18:34:09 GMT
ENV GIT_VERSION=2.23.0
# Tue, 14 Jul 2020 18:34:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 14 Jul 2020 18:34:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 14 Jul 2020 18:34:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 22 Jul 2020 12:14:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 22 Jul 2020 12:14:42 GMT
ENV GOPATH=C:\gopath
# Wed, 22 Jul 2020 12:15:54 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 07 Aug 2020 23:15:31 GMT
ENV GOLANG_VERSION=1.15rc2
# Fri, 07 Aug 2020 23:19:07 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '50b6be4a0713cf121af47f17b45c442e7d82b945011d762724cbf11a96fe4f7c'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 07 Aug 2020 23:19:09 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee3ab9b9080d1e70bd692e8d57c90290303771738974425a51fae906f5f2e0`  
		Last Modified: Tue, 14 Jul 2020 19:42:05 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a3797a5725c9ab05f88b09d827f86e241534e2af05cfc8b3cf1adc4db02d9b`  
		Last Modified: Tue, 14 Jul 2020 19:42:03 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cbaf2f9226d4e95015744a147b4d71ed139d49387bb1754be2cea42f7e65d1`  
		Last Modified: Tue, 14 Jul 2020 19:42:02 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5858d0ce03227049cc45ebc24ac93ddd12fbb92612093e84d3f1cfd6d8429115`  
		Last Modified: Tue, 14 Jul 2020 19:41:59 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4db578771a17334db0c8584e45d8f9ae9c1ff85bc0a7ee107098bf30bd4faa`  
		Last Modified: Wed, 22 Jul 2020 12:25:43 GMT  
		Size: 35.0 MB (34958446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb4bbdbae4293e41d5a0dfdcbc7c5dbd3ffdc9a4b4e9dd303f10d9b1f850a00`  
		Last Modified: Wed, 22 Jul 2020 12:25:30 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ca7be50ce16595f05952e633b26d328fdc818344139949895e4b5c6ea5c0f2`  
		Last Modified: Wed, 22 Jul 2020 12:25:31 GMT  
		Size: 5.4 MB (5353071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2da8c18baf6309c990aa5935b2065e7340b2c8b4b89340827a61448118d480`  
		Last Modified: Fri, 07 Aug 2020 23:26:48 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff3bd845a01f6251568b4dac9d487cdf81b72a1f517d75c39e5628ac2735197`  
		Last Modified: Fri, 07 Aug 2020 23:27:19 GMT  
		Size: 143.7 MB (143718900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7099729aff5f7c46140d8c869a131d6141a8466fa70e45e00ad0b14f5390c741`  
		Last Modified: Fri, 07 Aug 2020 23:26:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
