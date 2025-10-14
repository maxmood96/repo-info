## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:dbee536d331f6172e4b9f107fda6d1b57d45695980923e7170dcf96ba8581046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `golang:1-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull golang@sha256:752d8c8439a21fb83d6dbb0195faf72b5cb97bf996708cbdb759882ffe5178ba
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3685647005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab344e2793dd55a6a2e2086da48da38667f93f6614748ca902ccfd5cd9955793`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 13 Oct 2025 22:34:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 22:34:31 GMT
ENV GIT_VERSION=2.48.1
# Mon, 13 Oct 2025 22:34:32 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Mon, 13 Oct 2025 22:34:33 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Mon, 13 Oct 2025 22:34:34 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Mon, 13 Oct 2025 22:35:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Mon, 13 Oct 2025 22:35:35 GMT
ENV GOPATH=C:\go
# Mon, 13 Oct 2025 22:35:40 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 13 Oct 2025 22:35:40 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 22:36:57 GMT
RUN $url = 'https://dl.google.com/go/go1.25.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc249a599c6fe9d0d4093c363856f6c6320dbbe05e5d5d8818b711fb4a14fc23'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Mon, 13 Oct 2025 22:36:58 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de816070e98e5429b5b5b08098a2519854cb5273a9e9e20c30044c96f73a2d7`  
		Last Modified: Mon, 13 Oct 2025 22:53:20 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ab90c029098ec9c45312477da41adcdcb4f30b8a60c00570c17ace67b14bc0`  
		Last Modified: Mon, 13 Oct 2025 22:53:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0beb61d08874ce193e0ca10af6b86974d232768058f5547b11901b3224a1ca8`  
		Last Modified: Mon, 13 Oct 2025 22:53:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a909bbea9ca85678606f88408e14798abd03d45664d419aa55ebf6ebaf72a7`  
		Last Modified: Mon, 13 Oct 2025 22:53:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70ad25be99638eb351ab650b35ab29ce87679f813fb45c07d1de6ded3551ce4`  
		Last Modified: Mon, 13 Oct 2025 22:53:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78752c5045ba4d11ba55a9a1f73e04aeffffcd343c3c72998879ae77f78a7a5d`  
		Last Modified: Mon, 13 Oct 2025 22:53:26 GMT  
		Size: 51.2 MB (51243102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d971844854c1e2ad8b5e32a97067dad861a1b7e92221342392f98d76938d2`  
		Last Modified: Mon, 13 Oct 2025 22:53:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4105de880acd6b215be2d7e72d573e1653c58577805f64260cbd28731cf5a6b`  
		Last Modified: Mon, 13 Oct 2025 22:53:22 GMT  
		Size: 365.1 KB (365101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036d6274b9f54097f6a984b8dc41462886add50a1e05c0ca40b16ec6084f1bb5`  
		Last Modified: Mon, 13 Oct 2025 22:53:22 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438dea1181d2420eadd464cca51f645e9700d0486c76ae2a9779d39060a0aab8`  
		Last Modified: Mon, 13 Oct 2025 22:53:27 GMT  
		Size: 62.6 MB (62588429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fa31d9c8590b0f69570d31dd4db2b7514c11d4849a4c08fcc5f5823c9fc148`  
		Last Modified: Mon, 13 Oct 2025 22:53:19 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull golang@sha256:6a797620102c1b83d5b3611077cc05332fc7335d8e1094b2b2b5e3d4f04b240a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396304148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147b2bae4635f24924bc28000c29b7ad7fc9c5753dce6d3557636e11dea3878f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 13 Oct 2025 22:34:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 22:34:17 GMT
ENV GIT_VERSION=2.48.1
# Mon, 13 Oct 2025 22:34:19 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Mon, 13 Oct 2025 22:34:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Mon, 13 Oct 2025 22:34:21 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Mon, 13 Oct 2025 22:35:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Mon, 13 Oct 2025 22:35:32 GMT
ENV GOPATH=C:\go
# Mon, 13 Oct 2025 22:35:37 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 13 Oct 2025 22:35:38 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 22:37:19 GMT
RUN $url = 'https://dl.google.com/go/go1.25.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc249a599c6fe9d0d4093c363856f6c6320dbbe05e5d5d8818b711fb4a14fc23'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Mon, 13 Oct 2025 22:37:20 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b463a51def04d000f1e166e1cf647540bc680954a59b86d95ac106efecc040`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e382475565f5b080cab03906314833b98c6dfdada679c0ce9a48955f86d2b9f`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807eae41cb9b42c5dff95704303c2526aa4ba6c4c93e10c3adfe09dc17259f77`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7799396636e20e466239284f9f13075da8769818332f34bed61c3eafdbfa2bee`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab186f85e4bdffcfb2b27b9add6ff748b86bd818f75d2b6d317ab53969c1cc13`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6c7967ffcc8e35686a094fb1ce1b5750ae46a4e1d22abeaab14dc171d834b9`  
		Last Modified: Mon, 13 Oct 2025 22:48:36 GMT  
		Size: 51.2 MB (51221272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ffadb6c99663421ea17c0e1446454eb39888b1bd7f0c219aedaf247c609d`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25a07d2c318ce90671274e2ae6531709f1397f00b8d9a217e615abe4d6d6d9f`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 352.8 KB (352839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff70804c2f7796d906ff3c720847675c4a1ba31a5fd72689b92467643919a9ff`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c351ae320ddef070a1807f4ace3d61a218b498c463261dbec5aaa00fadb37400`  
		Last Modified: Mon, 13 Oct 2025 22:48:36 GMT  
		Size: 62.6 MB (62574403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ee3c1a9fa5d9579c8f4a1626861208c660faf0b27a91bdc5f11e163e20813c`  
		Last Modified: Mon, 13 Oct 2025 22:48:32 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
