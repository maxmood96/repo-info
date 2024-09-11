## `golang:windowsservercore`

```console
$ docker pull golang@sha256:32fc1907073be88d902774b8ef9bcb2f7883f34d4df1ce2b0254568208c8d633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `golang:windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull golang@sha256:5d5a07a31ab9dfd63886e061d350bdf794c3431137efe077fbd060d3abc5ca18
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1565299402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300435b66223816997abcfdb6f31d49e3830dacc240d7ae2415371a4a132f2b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:01:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:13 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Sep 2024 00:01:14 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Sep 2024 00:01:14 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Sep 2024 00:01:15 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Sep 2024 00:01:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:01:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Sep 2024 00:01:37 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:01:38 GMT
ENV GOLANG_VERSION=1.23.1
# Wed, 11 Sep 2024 00:03:40 GMT
RUN $url = 'https://dl.google.com/go/go1.23.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '32dedf277c86610e380e1765593edb66876f00223df71690bd6be68ee17675c0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:03:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e70f49c20671d030640819fe99e5b846a1ee5d8fb54950cedc8bffd9c6e29a`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7599a220d99a5983979a2065f169fff89d4ac209d3ad341f6e11abeece8339d6`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f726ad3a1e48a9ea73e77512f6f3aaf77051e52138fef0fabe83d10356188556`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeedd49da6baf674ed68e04cfa55364041bfd3b70d60c5f46f3b5c673b0508b`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a120805c5139fe19432413b01774c55fe1593495966fedfb484316001dd50a`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5010db3b75e0a589feff552b65d39808ef3ac6e6ae01cd982d64ffdf4c9dfe`  
		Last Modified: Wed, 11 Sep 2024 00:03:49 GMT  
		Size: 25.4 MB (25430526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bf413e96f658b2a166655b10f293f82c04512e88f3c05145dcedba34f8f0ce`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7beb51ae082094234d5bb9a42204cb0805c7d4c3a4d5f1b30f08f6dfc3dd67`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 336.3 KB (336263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede37f38dfa3cd5022991843081e14382488928f40fca1ecc38efc74bfaa8c3`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bdfe800dc36d8ceb8f648238c2c0e6f0d72274752fe15497e99f69712c7cad`  
		Last Modified: Wed, 11 Sep 2024 00:03:57 GMT  
		Size: 77.3 MB (77329741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bfc9fd2237a63248c24f2d2b4341b9597abe5da57d5f8a3c18bf279b7ce63e`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.17763.6293; amd64

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
