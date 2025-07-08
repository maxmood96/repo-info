## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:18e4d50a971e51cc0af71b95a5a87c22d7881739fa07e867ea83bd01c743496a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull golang@sha256:cd2216e7373980ba056b824c1b45e36d2e50208ba096ab37cdfbe0f9fd03044c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2414053135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fe0fe256dc96575e6e95ef5d64c6dce3ea178a4f67cff808b60bd024c4b497`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 08 Jul 2025 18:04:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Jul 2025 18:04:06 GMT
ENV GIT_VERSION=2.48.1
# Tue, 08 Jul 2025 18:04:07 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 08 Jul 2025 18:04:08 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 08 Jul 2025 18:04:09 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 08 Jul 2025 18:05:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 08 Jul 2025 18:05:22 GMT
ENV GOPATH=C:\go
# Tue, 08 Jul 2025 18:05:29 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 08 Jul 2025 18:05:30 GMT
ENV GOLANG_VERSION=1.24.5
# Tue, 08 Jul 2025 18:07:23 GMT
RUN $url = 'https://dl.google.com/go/go1.24.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '658f432689106d4e0a401a2ebb522b1213f497bc8357142fe8def18d79f02957'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 08 Jul 2025 18:07:25 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f2ebec6d2a482525f7974590ef34c80777296c52936275675e0ef5b5138f47`  
		Last Modified: Tue, 08 Jul 2025 19:07:54 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb9a44a154f7f11f59a861940f77ecce1c5a419cca236f2551a07e8d802986`  
		Last Modified: Tue, 08 Jul 2025 19:07:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72b318f3d64a8b43f1fbfaf2eeb4cd9b013f7915f1cca0c49e506372d239784`  
		Last Modified: Tue, 08 Jul 2025 19:07:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e40f5eb3bdf7c96079ab2f3e6ebdea0ae19b7a76ae70576ed84f8e388218c5d`  
		Last Modified: Tue, 08 Jul 2025 19:07:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003a428e80e39f686c3b2be0d57b699010d77873582c7eee2e493dc60dea16a7`  
		Last Modified: Tue, 08 Jul 2025 19:07:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867fb251b061c80fcfe126886e218b8618a8f103546686c083183a460948431f`  
		Last Modified: Tue, 08 Jul 2025 19:08:08 GMT  
		Size: 51.2 MB (51209168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84446cf4e7c2f48561d32170bb72d6860a8c4eabe39c6cccb48f706e9709a012`  
		Last Modified: Tue, 08 Jul 2025 19:07:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ec0eb7ca701628aa54aaec40f8b9651af15ba66d32420d257129aca4a39342`  
		Last Modified: Tue, 08 Jul 2025 19:07:57 GMT  
		Size: 314.0 KB (313951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bb493afef36c59a12452aeada982a324a4befdf9332dc2420861759edc799d`  
		Last Modified: Tue, 08 Jul 2025 19:07:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f84ed02adc343c7b38ce3914e339010f52a694cd1482bdc2fc96e4cdfad32ae`  
		Last Modified: Tue, 08 Jul 2025 19:08:14 GMT  
		Size: 82.3 MB (82267980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445b5bc62a1e11dac010e911ae4f33e1c945f5f4766534749c52c73d7cfe11f6`  
		Last Modified: Tue, 08 Jul 2025 19:07:59 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
