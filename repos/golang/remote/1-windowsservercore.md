## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:0e3143c2011f2aa9adca9e0ba59944078d16e94db5c88748f90bf0bba0b06387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.1249; amd64

```console
$ docker pull golang@sha256:a6b0734d2c6af282268e20d514f0176afd16af1c4b649c1354fee2e44e1413bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2665865423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d97be4b6ef931ed205366da5b519658f5a09a06ad2e3ad613c2d0a62a263c9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Tue, 08 Nov 2022 18:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 13:51:30 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Nov 2022 13:51:31 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Nov 2022 13:51:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Nov 2022 13:51:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Nov 2022 13:52:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 13:52:12 GMT
ENV GOPATH=C:\go
# Wed, 09 Nov 2022 13:52:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Nov 2022 13:52:37 GMT
ENV GOLANG_VERSION=1.19.3
# Wed, 09 Nov 2022 13:55:50 GMT
RUN $url = 'https://dl.google.com/go/go1.19.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b51549a9f21ee053f8a3d8e38e45b1b8b282d976f3b60f1f89b37ac54e272d31'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 13:55:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becc14271944025e3fa6c2ef2689bdfbf09bfc54ec339115d3082df315898e4`  
		Last Modified: Tue, 08 Nov 2022 19:38:57 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea79272e8d2a572a4d212450946bce415296eae87b6ce74df5b622cdfee02c67`  
		Last Modified: Wed, 09 Nov 2022 14:31:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a776f73cd30b265202025b98515575e21f757c88c6361190224cf46c2b7d1d`  
		Last Modified: Wed, 09 Nov 2022 14:31:53 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5268ccf7578edb6ae20eccf50b8be8c8da75b9054711b531062a365dc4fdca4`  
		Last Modified: Wed, 09 Nov 2022 14:31:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c9e4ebbf21dbe0a28faabe67fd74fca79784fefc03a56fae2e25366742aa37`  
		Last Modified: Wed, 09 Nov 2022 14:31:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671be4304252589ad8fea639a28234c14a6aeab6a0913d98704928824b355f28`  
		Last Modified: Wed, 09 Nov 2022 14:32:01 GMT  
		Size: 25.7 MB (25693161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131c64f4139ebfed8185c51abad4bbb44ad9830a76a221307d83acc03b579f2e`  
		Last Modified: Wed, 09 Nov 2022 14:31:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ceec23424e6d501387ce0ab8f96b2349ac91551e8ff768a658f97eb07430e76`  
		Last Modified: Wed, 09 Nov 2022 14:31:49 GMT  
		Size: 548.2 KB (548156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9475cb31b9e6aa94b3c8bac11dad0e1d052709c8d931bf0ae9373371ad4d7bf`  
		Last Modified: Wed, 09 Nov 2022 14:31:48 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f00ac483de739170f945938526dd868499e135b2661edf64b64a35e533d0ae`  
		Last Modified: Wed, 09 Nov 2022 14:32:45 GMT  
		Size: 157.8 MB (157844340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973945315f37c2cee022dc1f6b25fe2d420fa96edd876cad28a507515f40c18d`  
		Last Modified: Wed, 09 Nov 2022 14:31:48 GMT  
		Size: 1.6 KB (1589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull golang@sha256:7ba94a089f6e9ec6a4ab2b3270748a8dec2bf403923e718573e36b7b38167c4a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2962030404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8bd9367748ff7a3b3db655bcc430dd2ff2aacfce2b5b265f6b123d1a86310c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 13:56:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Nov 2022 13:56:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Nov 2022 13:56:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Nov 2022 13:56:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Nov 2022 13:57:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 13:57:58 GMT
ENV GOPATH=C:\go
# Wed, 09 Nov 2022 13:59:24 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Nov 2022 13:59:25 GMT
ENV GOLANG_VERSION=1.19.3
# Wed, 09 Nov 2022 14:03:31 GMT
RUN $url = 'https://dl.google.com/go/go1.19.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b51549a9f21ee053f8a3d8e38e45b1b8b282d976f3b60f1f89b37ac54e272d31'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 14:03:33 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a2b0ba4717890a5f71c35ff277f846f8f9b6668e0e7bb61c09c7be2ae6fa2b`  
		Last Modified: Wed, 09 Nov 2022 14:33:12 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ea601fe915f260a37aa95fd46906a58c4828c48a181f7fec434c255461bc3c`  
		Last Modified: Wed, 09 Nov 2022 14:33:07 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0a12f7377f09e1e60b8f98ba68c21900eb3bd8da74b27356717b7b531b1f19`  
		Last Modified: Wed, 09 Nov 2022 14:33:06 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96720d70c884dea5fd72c530b456770bdc779483b7f1d752e386360daffe6e4e`  
		Last Modified: Wed, 09 Nov 2022 14:33:06 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10a1ec572d19d510940ad8ddec14084b9e4d8300ef36b3ef50f23b477df789d`  
		Last Modified: Wed, 09 Nov 2022 14:33:16 GMT  
		Size: 25.5 MB (25457961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378cf1d27c9b1599652ca2d1c09cf3196ecbd22b40ee08813574a0fc119440d7`  
		Last Modified: Wed, 09 Nov 2022 14:33:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cd622fdb3c0fabfcb202894dc24ba2a9491bf349e487be308fb6315c43c1d`  
		Last Modified: Wed, 09 Nov 2022 14:33:04 GMT  
		Size: 326.0 KB (326032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe2ec77bf4f0673d2620baa4e0302b768acebce02398e710036bf3f656c0ecc`  
		Last Modified: Wed, 09 Nov 2022 14:33:03 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eaf4d425600774d03d9f467838fe1b18d6a9460b749c91c1024aa8904b0e334`  
		Last Modified: Wed, 09 Nov 2022 14:33:58 GMT  
		Size: 157.6 MB (157648264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6413639a75ce7d233f32964ef57abd38fc992a742736bc7e7a163fa8aa5b4b0`  
		Last Modified: Wed, 09 Nov 2022 14:33:03 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
