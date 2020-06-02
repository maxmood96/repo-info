## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:7f6908e326be47c2373013a952ffd2dda26dc15bdafee1d942538407897f5c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull golang@sha256:989c87a72728291da99fe77f0b0f59da449227640a8c93ff05c0776dcb087b1d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1877459123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4305e349e769965b4555ed8d266c665d5c3b5a8bb537e6469dfc2477cb9c982b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 12:41:47 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 May 2020 12:41:48 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 May 2020 12:41:49 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 May 2020 12:41:50 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 May 2020 12:42:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 May 2020 12:42:47 GMT
ENV GOPATH=C:\gopath
# Wed, 13 May 2020 12:43:08 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2020 01:32:11 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:34:45 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e04f591219b18e7cabe73eb79c90405b5c7a5baee61377670d7a48429c5c978d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2020 01:34:47 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab29cecca7bcbda2c597002df3455f14ecd6e1e255624faeb782851f5808e123`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beddff0184164c7525ffdf35ba620099ed0de8e34ee5eac9feba1b3d1f6d8b08`  
		Last Modified: Wed, 13 May 2020 13:00:16 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d62d5306f69de301a3da0098e43f6877bcd793751aa69649fbf153e5b80844`  
		Last Modified: Wed, 13 May 2020 13:00:14 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b7f47046d1b96f631bced4b78ab3533856931a0b17151ecd686fc696a38daa`  
		Last Modified: Wed, 13 May 2020 13:00:15 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f15f0f01c8b67ae80b392c731ed4f6e8f9ece9080f4d51837906b5e001246`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 25.4 MB (25433290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777191637dda5a3401ae57c057af755a1c87b5c2b168786119f18def6d77a43b`  
		Last Modified: Wed, 13 May 2020 13:00:10 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea1f3b8205267e65831ebb254905af6cfc8a9fc30840f0f1556fd86ea6f8bca`  
		Last Modified: Wed, 13 May 2020 13:00:10 GMT  
		Size: 305.5 KB (305481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e466ee895f55b1ab26827500cf79b5885338b7a500bf56ebbe01277b61ec95`  
		Last Modified: Tue, 02 Jun 2020 01:47:47 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d29cfeb8b7f9e829ba6bbb4370bbf557bd968e622d9d775d5782765cbfe7261`  
		Last Modified: Tue, 02 Jun 2020 01:48:14 GMT  
		Size: 133.4 MB (133378060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee53ccc16171ccff8766a3d7e43f46c630d1429751cf35fed1560f46790fdfca`  
		Last Modified: Tue, 02 Jun 2020 01:47:48 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
