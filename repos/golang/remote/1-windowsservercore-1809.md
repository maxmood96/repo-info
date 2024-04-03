## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:1a64f06c26e2956fbd93a47523e86b6e2017a3a2eb4f19f970c92ef23723ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull golang@sha256:52481ed71abf38b5a77afd28371cecff4c287d72939e9187f0f528a174e2944b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2222651997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fb560fd4a6fa1f2cd244f9d7e4f72e4c1ab8799a41afe461512e3d0720265b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Apr 2024 17:01:19 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 17:05:04 GMT
RUN $url = 'https://dl.google.com/go/go1.22.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8e581cf330f49d3266e936521a2d8263679ef7e2fc2cbbceb85659122d883596'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:05:05 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de886aeed15758cf8b9bae5634a3a3dd543c2e38a90211ee033df50442240fe3`  
		Last Modified: Wed, 03 Apr 2024 17:24:25 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9227bdea87c0d8de35c5273461506ee96fea45a5c908f39b37e2ebc24ddbb4d9`  
		Last Modified: Wed, 03 Apr 2024 17:24:48 GMT  
		Size: 71.7 MB (71727714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c7a4b73225817caa17a90d0dba9c6b05a399c4a60a7d99b143d5fba4ce93e`  
		Last Modified: Wed, 03 Apr 2024 17:24:25 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
