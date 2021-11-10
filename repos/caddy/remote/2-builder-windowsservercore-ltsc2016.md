## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:616283cce0c82245c2685b723e1f9538d1c4e926a9ad143dd66bf0e299b64ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:96a88b09cecf23cff2a8006ea25f1e037f50d01a9c74d2d3769f8bb228d2b768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450468916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fcd7b2f02771fd0b23831a7e603a01713fad078e5e205d745958ee47f638e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:31:46 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:31:47 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:31:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:33:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:33:37 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:34:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:34:35 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:37:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:37:37 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:18:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:18:53 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:18:54 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:19:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:19:56 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0c69f83a30944f5afdc948b3583f1418f71f3ae5a02382610f0898eb501f9`  
		Last Modified: Wed, 10 Nov 2021 14:05:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e4bea9e4e2ccac41591b4aed9981453c554ca498a23d01a69638d6ccab7016`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36358e1913c99dc66fbbca2e4c0f8472796bf33ceeb7fdc02d2b7096b1208d`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d071f5d45753629193f76196d769df9ff71ce3a39e5b10a16ff571cdb071a902`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79602be6489be8a0e5e82221cae33eae5692897081a79bfe959604121e2d0a4`  
		Last Modified: Wed, 10 Nov 2021 14:06:20 GMT  
		Size: 25.4 MB (25448073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30d749fb8ba78fba5cce783b8cbe233632a2ba5965d4b67168111396620aaa0`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f08b5963e19f3d28aa336d06434d4efec179b4b813e4aa4222ab064bc180f7`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 354.9 KB (354902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381a7ed29624957c6a0c2539069229be83423497216e9b19872996d3eace018`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184646a18b279b69062ae625cf768031d03c297beca44a465b8265af80e7116`  
		Last Modified: Wed, 10 Nov 2021 14:06:25 GMT  
		Size: 149.9 MB (149917271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e2acfda5cf05f260961ec16cee7c5c9e5573783c8298319e6b38846cb3b98b`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f8275e6d67e00182a573a1fea89b6fbafd29fdd9e6991bec289907772e366`  
		Last Modified: Wed, 10 Nov 2021 20:21:59 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f675d50b479c34b5e127a7560cec6198d6c06464747188b22904543e0919ffe`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dba2d80865d737653a9a4ff2db1fcac88ce9bf3521d9e7f6dc8116fd16a99b`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272648eb620ef88b428e4aac8f782d100c4e64bb6f14073ee16b5b89a3b12967`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b51ab7213b8db3f0e51ace7c64b811e81a3d838148d7c41c3a58a9ffd1eb66`  
		Last Modified: Wed, 10 Nov 2021 20:21:58 GMT  
		Size: 1.6 MB (1639511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd676bfb740256d3eae7ac606f73a7d0ad09121f54eacd3ffdeff570e4b73bd1`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
