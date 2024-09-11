## `golang:windowsservercore-1809`

```console
$ docker pull golang@sha256:a20ef70b0c075cbb1bbd707710364ae5674527c693a362fb909f16e7e6e51def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `golang:windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull golang@sha256:cb911449313ff7c9144bce748286eff1d33c663a8bbec96003b79a21587d9746
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1823383576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c1196954dc0424a87a4d7a90da28d019ac34911e106189b1923ee367e0bd10`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:01:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:44 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Sep 2024 00:01:45 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Sep 2024 00:01:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Sep 2024 00:01:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Sep 2024 00:02:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:02:04 GMT
ENV GOPATH=C:\go
# Wed, 11 Sep 2024 00:02:13 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:02:14 GMT
ENV GOLANG_VERSION=1.23.1
# Wed, 11 Sep 2024 00:04:48 GMT
RUN $url = 'https://dl.google.com/go/go1.23.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '32dedf277c86610e380e1765593edb66876f00223df71690bd6be68ee17675c0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:04:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c04bedb30d57245be0be7ce7146db3e3c564b56c572b18242a5decb16ff9dd2`  
		Last Modified: Wed, 11 Sep 2024 00:04:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b352097a953ef27941a57f1c9da3e9200cdeaedc1eee69eaaacb5db453aeb6e`  
		Last Modified: Wed, 11 Sep 2024 00:04:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b50cd90e9fa3a4f5bf519d3c39db19d418a8a6746fe474459447df2622af6ff`  
		Last Modified: Wed, 11 Sep 2024 00:04:56 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe427b2f4f242db027284ec365333af7afba7d4f159272889ac2f7ce62dca80`  
		Last Modified: Wed, 11 Sep 2024 00:04:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab171d9f058752f3a36355d4530a0447c6252214d0b9739b4b69a2440d6ae7`  
		Last Modified: Wed, 11 Sep 2024 00:04:56 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d1f00b154aea8b49eb5cb510f8636232e04b67c95e08531bd451d88b1fe823`  
		Last Modified: Wed, 11 Sep 2024 00:04:58 GMT  
		Size: 25.4 MB (25437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8024e23c792c0c1c5d31eeb589d814a03c4d630bf3d1fa26a0457d4851dac8c9`  
		Last Modified: Wed, 11 Sep 2024 00:04:54 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3ff680dde76271079ef10a54fc504f77d4c5df0ebdb5a3b94ef1527cd28d82`  
		Last Modified: Wed, 11 Sep 2024 00:04:54 GMT  
		Size: 335.8 KB (335801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5a849a0da86b63c35678b21b42b3435f645e7a59989161eee7dd5f2243a565`  
		Last Modified: Wed, 11 Sep 2024 00:04:54 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868b84a71ae6e7ebbe505ee90b01fbf644b553fb6cbbad9c16faff97f655ba5f`  
		Last Modified: Wed, 11 Sep 2024 00:05:06 GMT  
		Size: 77.3 MB (77331795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b616a32799159cf09285bd4cb65b9264e90a12c193305e8610e9d1ff67273276`  
		Last Modified: Wed, 11 Sep 2024 00:04:54 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
