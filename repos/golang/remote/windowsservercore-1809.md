## `golang:windowsservercore-1809`

```console
$ docker pull golang@sha256:51e12ecccfcf1779d64061f4d4ff517c3ce3abcfa140254f7d91b6d341ad2e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `golang:windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull golang@sha256:f05f285f5ff551bfc36f049591acfdbee5fe7fdcb80a3847db808a75919928a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2377238008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cce7e7c5c091762aa6231cda32d1f2dd8c6a5acd684a23270387bdbaea71a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 13:22:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Jan 2020 13:22:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Jan 2020 13:22:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Jan 2020 13:22:53 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Jan 2020 13:23:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Jan 2020 13:23:58 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Jan 2020 13:24:21 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Feb 2020 01:24:50 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 01:32:06 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'aaf0888907144ca7070c8dad03fcf1308f77a42d2f6e4d2a609e64e9ae73cf4f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 14 Feb 2020 01:32:08 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c34cd616875c2f9d033967e4516512eeda759d5d727381f68534f20a423fbc5`  
		Last Modified: Wed, 15 Jan 2020 14:19:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f8f6402962aaf689f18fb7dc48707abd1442236650fa93feafdb8a0e62b884`  
		Last Modified: Wed, 15 Jan 2020 14:19:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2ccd2aa22967996e2db31a32fa197fe049385493a27f6cac5d28e147dc77a1`  
		Last Modified: Wed, 15 Jan 2020 14:19:42 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4005eb5a3fe7e59daa2cf4c83ef39ebc3b67aa33c077f34727270a45d08386`  
		Last Modified: Wed, 15 Jan 2020 14:19:41 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123a2902604294d730658cf5b5098adc030395e96b276912489cd129282805d1`  
		Last Modified: Wed, 15 Jan 2020 14:19:55 GMT  
		Size: 29.6 MB (29634086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4abbf4635cc281d4995cae6e8ea73c4f2713f902bf6d5e500134413fc88da`  
		Last Modified: Wed, 15 Jan 2020 14:19:38 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dc6850cb4055c8c383de6b662f37153a7fd9372a26c59bdd06bfb84f8220e3`  
		Last Modified: Wed, 15 Jan 2020 14:19:39 GMT  
		Size: 292.9 KB (292910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea2b25ba84037b46e0c7efc812dec1c9c49785a7620eb16ab533970fd481e18`  
		Last Modified: Fri, 14 Feb 2020 02:44:08 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25877eac2722fb8cd2c329fbdfe3c3ef011132d1f020d6806c124249da6bba09`  
		Last Modified: Fri, 14 Feb 2020 02:46:06 GMT  
		Size: 129.9 MB (129890152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b77e850ef1a28a28a18985ca45fa8ea900a60da55fa3ef29cebfe0bf08aadf`  
		Last Modified: Fri, 14 Feb 2020 02:44:08 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
