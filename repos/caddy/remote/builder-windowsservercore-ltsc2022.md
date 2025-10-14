## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:d660257095513d31ae8d35c6d2ab206b438242b15ebf38659c647bce0427eef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull caddy@sha256:4c5222c8bea15c5fb788606604840cf619407f560cca3172cf18865af68266f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2398606780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866f758e886f4c71ff0774c4ed16492a173f0b5078d1adc1f91d9890cc3d40be`
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
# Mon, 13 Oct 2025 23:10:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 23:10:21 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 13 Oct 2025 23:10:22 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 13 Oct 2025 23:10:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 13 Oct 2025 23:10:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 13 Oct 2025 23:10:32 GMT
WORKDIR C:\
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
	-	`sha256:2c53bdb7d1150dde6e78ee67e235b3347126bf71ad787493b4d0e807918e73eb`  
		Last Modified: Mon, 13 Oct 2025 23:10:45 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c4e26d35033097926110863da793928ad7413e9e8c7bedcadf0f3d128ac962`  
		Last Modified: Mon, 13 Oct 2025 23:10:45 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5013988459ca97c3f6dfbd32a052c7380cd97a08281947b66becb7c19dc0032`  
		Last Modified: Mon, 13 Oct 2025 23:10:45 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7efb5e1d367459bd21825afb3ca252cf325daca51ca50a3696fdf834bc7ca1a`  
		Last Modified: Mon, 13 Oct 2025 23:10:45 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fde1c4bc9f5ba033b28c4643948ae953188f4bc6c75a54c759cbad061ae7551`  
		Last Modified: Mon, 13 Oct 2025 23:10:46 GMT  
		Size: 2.3 MB (2296014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81778607bc2bb549a5d50f667c94ab6623e583d060c8203c5eb6bf43b0b09f9`  
		Last Modified: Mon, 13 Oct 2025 23:10:45 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
