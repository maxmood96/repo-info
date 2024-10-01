## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:7f4bfdf26bef6f859fbb671ae4c05d98a5205da99e6361a4db8ee73172222e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

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
