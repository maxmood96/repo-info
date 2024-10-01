## `golang:windowsservercore`

```console
$ docker pull golang@sha256:a110e31c597a3503d20eeb51984b5cda3455f2227fc823abb01a73bf7bea0438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `golang:windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull golang@sha256:70b267eff5df18566e4043fa7ed504252a5f586e2ef80b3d4ad3e96e9e9d0386
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1565291235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a78ac90cf660b3f6f5b1b08d87bacec600d62a63189727b000a9e9d1f3703`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Tue, 01 Oct 2024 22:18:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Oct 2024 22:18:40 GMT
ENV GIT_VERSION=2.23.0
# Tue, 01 Oct 2024 22:18:40 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 01 Oct 2024 22:18:41 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 01 Oct 2024 22:18:41 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 01 Oct 2024 22:19:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 01 Oct 2024 22:19:56 GMT
ENV GOPATH=C:\go
# Tue, 01 Oct 2024 22:20:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 01 Oct 2024 22:20:03 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 22:21:54 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 01 Oct 2024 22:21:55 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b441674e73b085e49867d7d6b3ad8f575b8cf5583a0157ee2a9cad391413572`  
		Last Modified: Tue, 01 Oct 2024 22:22:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ee36cfe4e46233dadf9e7b74868dfe37a0822a312fa54491a4a1e3728610e`  
		Last Modified: Tue, 01 Oct 2024 22:22:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e6cef0cc8b8cddaceaaddf4c33407d9e4ea0b2de66f92960da8cad4082464`  
		Last Modified: Tue, 01 Oct 2024 22:21:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117064c18283de224f7ed4b9d915a49ed91950304024ba1bb91a0f6a0fac5677`  
		Last Modified: Tue, 01 Oct 2024 22:21:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a57c69c2648bde86d9208ec71b9dae6322192f0004749d17f05d9eb475b4341`  
		Last Modified: Tue, 01 Oct 2024 22:21:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787f41284445188aca00c20578c15af503490138ac10490a43295e2cdfb9abaa`  
		Last Modified: Tue, 01 Oct 2024 22:22:01 GMT  
		Size: 25.5 MB (25453811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eec2a5fa4821f330ad627a361991c7b274319b2f55458ca33be49df11f64c2`  
		Last Modified: Tue, 01 Oct 2024 22:21:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76a9c22edcb4adb2a9941d5c942b1aad9b12fd2bede08bdce58b2a6cc739fc9`  
		Last Modified: Tue, 01 Oct 2024 22:21:58 GMT  
		Size: 321.8 KB (321751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95949413c47e23ea6d33354cefd4f15bc73782a5cad00328d65a81d440f7e2f2`  
		Last Modified: Tue, 01 Oct 2024 22:21:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814b4e0655bd9e00b80e5e71b8961b7edbb435a42caebc59a544ce768788220`  
		Last Modified: Tue, 01 Oct 2024 22:22:08 GMT  
		Size: 77.3 MB (77312852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47afec2151d1cc1ae44c39acb638b250bd5081f1b7e120de11b207b39c270ae7`  
		Last Modified: Tue, 01 Oct 2024 22:21:58 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull golang@sha256:e2acd95276734d902a01d090ddab45972d91d1d12b5baf7aef3eee76b0f7d439
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1823375865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f109e7120d4646782bc446e582ec2137845f8642eecd2971a9b6f391ca24fe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 01 Oct 2024 22:18:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Oct 2024 22:18:47 GMT
ENV GIT_VERSION=2.23.0
# Tue, 01 Oct 2024 22:18:48 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 01 Oct 2024 22:18:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 01 Oct 2024 22:18:48 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 01 Oct 2024 22:19:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 01 Oct 2024 22:19:49 GMT
ENV GOPATH=C:\go
# Tue, 01 Oct 2024 22:19:56 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 01 Oct 2024 22:19:56 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 22:22:46 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 01 Oct 2024 22:22:48 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9bc77286e905b87ac9620178d2533946c48d845bcd2bd500baf99cb3d8ed75`  
		Last Modified: Tue, 01 Oct 2024 22:22:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0344de86aa372f2865265aa1dd1e85b76b6cee031e0032653a56df7b3fc69a06`  
		Last Modified: Tue, 01 Oct 2024 22:22:55 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96cdbb3ee782c414d0d01c4233606df3e0a89150872debbe55ae325821b1391`  
		Last Modified: Tue, 01 Oct 2024 22:22:54 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ba8246f68dea1d573652e5717889e1216bc6c6753e99427e4b68a973be969`  
		Last Modified: Tue, 01 Oct 2024 22:22:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfb417f469a4c5e07f31ff10315dca60f01f6b6a631fad59c96f21cf420de09`  
		Last Modified: Tue, 01 Oct 2024 22:22:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d48f0b811a99ff51a1e2ea3122535daf9334670d2e638f09e5163764a02590d`  
		Last Modified: Tue, 01 Oct 2024 22:22:56 GMT  
		Size: 25.4 MB (25430775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8500d4eaa4164a2276c547c82c4aad4dc122e49bf130739336110a4a180bba7c`  
		Last Modified: Tue, 01 Oct 2024 22:22:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35b48ac656599d82b2f6ccf0cd09eac07151b09cc8d6355a31e1d4d201ee50d`  
		Last Modified: Tue, 01 Oct 2024 22:22:52 GMT  
		Size: 338.4 KB (338361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9e0c43310a463c4279582c26034647c2f2c8d35ddf71ace70fe738acfbe2bd`  
		Last Modified: Tue, 01 Oct 2024 22:22:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ebfc312bd9c2105564268675f52b514bcbaa39e0b1a496b3dd037455137129`  
		Last Modified: Tue, 01 Oct 2024 22:23:03 GMT  
		Size: 77.3 MB (77327873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0b12ec4348d7ad7dced32ee067402a8a1853237f3116c1b3e7657f71e5bd75`  
		Last Modified: Tue, 01 Oct 2024 22:22:52 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
