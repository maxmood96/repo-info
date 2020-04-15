## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:ee4af251963046b1b708cd3b26b88464d360f4c031d4a38309ea252db87faaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `golang:1-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull golang@sha256:2f829ac03c1f1d9ca0bfd7c7f2a2271697927ea31260fb268e493ff3fbae3e9c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5906738090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9fca7ea18d754a26476dcfd3f317d24445e90006d10703b5fc2b1892df84cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 12:13:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Apr 2020 12:13:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Apr 2020 12:13:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Apr 2020 12:13:52 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Apr 2020 12:15:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 12:16:00 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Apr 2020 12:17:10 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Apr 2020 12:17:11 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 15 Apr 2020 12:20:45 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1b5a60b3bbaa81106d5ee03499b5734ec093c6a255abf9a6a067f0f497a57916'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 12:20:47 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ac0134cee91589d04e97f11994235cce86faef5c581d15f2e143ecb90e92572`  
		Last Modified: Tue, 14 Apr 2020 22:16:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e193ef3efc0b7b4d015dd4804df2f647ed95aff87065762070b713406bf404bb`  
		Last Modified: Wed, 15 Apr 2020 12:38:12 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b34c38442e3990d34fdbe6329b47ff91cd350ae0ea3b47bdabca4d881e8c42`  
		Last Modified: Wed, 15 Apr 2020 12:38:12 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b996d2b99a502b832c52702fac917d97b109a3886bc17ace34c0bbc466f3cc9`  
		Last Modified: Wed, 15 Apr 2020 12:38:08 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67510f02ca3412ca56356abd70b92d3787bf0d930cc1b4425ed8cc5640c8ce1`  
		Last Modified: Wed, 15 Apr 2020 12:38:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5392dc82c70fdf1c8e68d2a9f85056b2a9652206e9d012a167baedd1c50d7b`  
		Last Modified: Wed, 15 Apr 2020 12:38:16 GMT  
		Size: 30.5 MB (30490226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d699d144dd2b8312d08ba3f36dcfe40653883e9553b2a832efa1811dd1d0703`  
		Last Modified: Wed, 15 Apr 2020 12:38:04 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd29499166397dd36bfe2ccb0a1dd63049a0f9a08020d3daaba6fcf19693a8e`  
		Last Modified: Wed, 15 Apr 2020 12:38:11 GMT  
		Size: 5.3 MB (5341344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d320ae6428638faa51878b64aa60e4c8e98058f7da3287900ed5bb03ccf88530`  
		Last Modified: Wed, 15 Apr 2020 12:38:04 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729007e11eb95764075684691b76656f5b6f680a29705125ec3963b2756b5ace`  
		Last Modified: Wed, 15 Apr 2020 12:38:41 GMT  
		Size: 142.8 MB (142829708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74774d8bbeb62bb29e96d83919cf03e75d485f79f7db29c4d4e27ffb05a77956`  
		Last Modified: Wed, 15 Apr 2020 12:38:04 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull golang@sha256:db08e5c5bdcdca93af63aac5a3df56ae2c766ae71ddf315e487deafea2c583e2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2434071862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243ad5611aae50fe9dd1e05734468b9b7d39cd2dc737f2a387a60cabeaa4cf28`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 12:21:01 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Apr 2020 12:21:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Apr 2020 12:21:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Apr 2020 12:21:03 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Apr 2020 12:22:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 12:22:14 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Apr 2020 12:22:36 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Apr 2020 12:22:36 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 15 Apr 2020 12:25:15 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1b5a60b3bbaa81106d5ee03499b5734ec093c6a255abf9a6a067f0f497a57916'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 12:25:17 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73418a0571fcf99cda633f93148961556a000d6ca83382f82523ca5a8b0be23`  
		Last Modified: Wed, 15 Apr 2020 12:39:04 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65102d68f0797795223f1f4585ad2b34d000b8e35f180b0f16b3b493f9d3717`  
		Last Modified: Wed, 15 Apr 2020 12:39:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489945d0cac3a39fb186a751328c9ff31076871951d8fa879c17175c562a232`  
		Last Modified: Wed, 15 Apr 2020 12:39:01 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a59f7dec5086ddc5e0977d8f0ed27eb4feb8da6bebdeafb10cb3abe403026d0`  
		Last Modified: Wed, 15 Apr 2020 12:39:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aadc1abf3e539cc5d0cfe0421103007d11d6656dd1e615a26fe73a863a4710f`  
		Last Modified: Wed, 15 Apr 2020 12:39:31 GMT  
		Size: 29.8 MB (29755877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dbdd00c086e554067ca9c230fbcdb94e17c61fb645e42f17bf6aa78bf8ac32`  
		Last Modified: Wed, 15 Apr 2020 12:38:58 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2758f4c98fac0882dfcd1c09b1fc228e49982d00ebacd0cd61da9d79f7150bfa`  
		Last Modified: Wed, 15 Apr 2020 12:38:58 GMT  
		Size: 300.8 KB (300826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8702fd2c1bf8028e78d58e16657d4f879cd73c6aed154ca63df5d9bb0213b74e`  
		Last Modified: Wed, 15 Apr 2020 12:38:58 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9ecb3612c460309e122bfa58a93f2b9228ce40db45e981b554d52d43a55e6e`  
		Last Modified: Wed, 15 Apr 2020 12:39:25 GMT  
		Size: 133.3 MB (133298731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e320ddd952c25e45e063757cc86c73e032e88550d22bbb0a84e054dc9661560`  
		Last Modified: Wed, 15 Apr 2020 12:38:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
