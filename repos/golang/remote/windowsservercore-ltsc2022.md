## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:33cb6381ca78e0b93f7efd7182054663773cfbeb7b597ab4eb97e38a76762127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.288; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.288; amd64

```console
$ docker pull golang@sha256:311bb6d05cec77fecffba9065f9abc420257a2250324f372feb229c04fed7e5a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313347894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaa5f37c77d77d379757afbd058cebab0d554cc7fb459eeac62f639b290c8b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 07 Oct 2021 11:33:56 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Oct 2021 12:26:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 12:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Oct 2021 12:26:45 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Oct 2021 12:26:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Oct 2021 12:26:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Oct 2021 12:28:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Oct 2021 12:28:31 GMT
ENV GOPATH=C:\go
# Wed, 13 Oct 2021 12:29:01 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Nov 2021 20:15:11 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:17:36 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 04 Nov 2021 20:17:44 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b03bbc71f9254a4ad2fba472595c859655b9d0cfefa638928416e277e0f0d497`  
		Size: 889.8 MB (889767519 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b201e45e5b11128e36517715f5b6ae98e5782737c1b112a5fae2aa83206f57bf`  
		Last Modified: Wed, 13 Oct 2021 13:23:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2567242b2a3285f24a11ecba702f0e8b3101e1bdaa300b874ba21e16a41b243`  
		Last Modified: Wed, 13 Oct 2021 13:23:57 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6489a6e74029239fb6c471499059266518bce590609bab375525b8cda02168d`  
		Last Modified: Wed, 13 Oct 2021 13:23:55 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523db4167183ae79d9e363507d248619537805b522b84a3e996a859b61adbe00`  
		Last Modified: Wed, 13 Oct 2021 13:23:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8854acf2bd25d9e39c1d4b2387dab690473b72507a036371bc721d43be7c8348`  
		Last Modified: Wed, 13 Oct 2021 13:23:54 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f893930da68e8c7375a58d2327848d1d80af63c8c28a750e40b3e2a0cc53b`  
		Last Modified: Wed, 13 Oct 2021 13:24:21 GMT  
		Size: 25.7 MB (25710356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3721e5d0ad0c109458f60c7543d626e543fbe9f992e8f56d387090ba96cb07`  
		Last Modified: Wed, 13 Oct 2021 13:23:51 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145661d5dbf5dce3611b59d5a48a1fc641250e534b0e93a0ee8dcb792c34db12`  
		Last Modified: Wed, 13 Oct 2021 13:23:52 GMT  
		Size: 552.1 KB (552063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc7bab962c000a17829d08c517a74c799844fbce96ff636c5f30f2b63e1b11`  
		Last Modified: Thu, 04 Nov 2021 20:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b48ec46717f45dfcb227eed525825561a31c3148058f7ec2b833f26dc652e0`  
		Last Modified: Thu, 04 Nov 2021 20:49:29 GMT  
		Size: 145.6 MB (145607690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794c597c157c987d3a522f5719c27e32507a6d44fb4cd243055885b53b0f5a78`  
		Last Modified: Thu, 04 Nov 2021 20:48:56 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
