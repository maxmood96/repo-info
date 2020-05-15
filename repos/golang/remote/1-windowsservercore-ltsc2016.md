## `golang:1-windowsservercore-ltsc2016`

```console
$ docker pull golang@sha256:0aeb951b6f85225e427838ff89e3b7b59f27ec0dd0f89595d46c40153e59f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `golang:1-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull golang@sha256:92e6f263158b5956fbfbe6fe319ea9a48d597e6c621638507032476e3f8621a4
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5910560970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77e623ba27bb28c0225c748453dc58e2d8234283e0c54156df9bbec1fc95f2f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 12:34:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 May 2020 12:34:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 May 2020 12:34:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 May 2020 12:34:36 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 May 2020 12:36:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 May 2020 12:36:44 GMT
ENV GOPATH=C:\gopath
# Wed, 13 May 2020 12:37:56 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2020 21:15:19 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 21:19:08 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6811c14341fa0e5ebe05b28a4a8086e51a25ee54bc860f83183e1c478e3b1b60'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 15 May 2020 21:19:10 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0def164752638b449f9492fb38909585e5cecedf0ad008fda42fc5ab6f2b63`  
		Last Modified: Wed, 13 May 2020 12:59:26 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f3d9a8e5516c776c8a7744e47a8786a40d09fad03883dea4cdc16ec53cc2a7`  
		Last Modified: Wed, 13 May 2020 12:59:26 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7002013292f0cf6c3247142fe800a11df319c8a5091a1f1d1c88b7bb5984506`  
		Last Modified: Wed, 13 May 2020 12:59:22 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9f2f2b2d4d24a76d76287822317d40ef275186c2cfd887d031e98a75d13a37`  
		Last Modified: Wed, 13 May 2020 12:59:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f04778fd3d0864d7fdbbd94565b68e3894dd87024ff8e76002c226cb26a0c7`  
		Last Modified: Wed, 13 May 2020 12:59:32 GMT  
		Size: 30.5 MB (30487090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b80400248193be1deee93a1d84f2b772e0e5db5b4456452e62c4d9f6e8b0d`  
		Last Modified: Wed, 13 May 2020 12:59:19 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86a93f290f4d57c447fd96fe7ddef78404efcafb5ea4d930daa9e6a4fa97f8`  
		Last Modified: Wed, 13 May 2020 12:59:21 GMT  
		Size: 5.3 MB (5338685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c157202d38dc032220d77ea7a2170d72899485f07f2cfcb9987259910b1b2c`  
		Last Modified: Fri, 15 May 2020 21:35:01 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f01e442620679e28ebcda113278b5f0f04409c9f58cb54cee4e257a6e1896f`  
		Last Modified: Fri, 15 May 2020 21:35:29 GMT  
		Size: 142.8 MB (142836041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2032514dde1cd6db30e7fdc2b768fe2e671281f4f669ba5f898c0b576ccf0986`  
		Last Modified: Fri, 15 May 2020 21:35:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
