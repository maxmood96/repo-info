## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:74840b0ac0bbf6390542a172d5e2ee58b4c2d31e0143d980bfa702245f3a0098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull golang@sha256:497a8266b9f927fa610f703656a43bf1e7a164e3bd101e06650cb2f1aead0d91
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2371840125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c224d75095e071280950dd254986ef6b2c77412ba74c8b8259a262444ad97ce4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 04 Mar 2025 21:16:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 21:16:58 GMT
ENV GIT_VERSION=2.23.0
# Tue, 04 Mar 2025 21:16:58 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 04 Mar 2025 21:16:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 04 Mar 2025 21:17:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 04 Mar 2025 21:18:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 21:18:13 GMT
ENV GOPATH=C:\go
# Tue, 04 Mar 2025 21:18:24 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Mar 2025 21:18:24 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 21:21:10 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 21:21:11 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc78866de321603261bf5787e02ebf66370ddcf10832f7b81e070d0730323e5`  
		Last Modified: Tue, 04 Mar 2025 21:21:16 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d16a5be1753ef22b6fecb7fbbcd7d451916dc14bc3431130f617f5f873285b9`  
		Last Modified: Tue, 04 Mar 2025 21:21:16 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44657fe8a754de7142652b08e033aa46afcea5dcae17b8ff229529d76014d8c`  
		Last Modified: Tue, 04 Mar 2025 21:21:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaf4b1a3e294bd12428d1ee4810c0f3928e759dc98a415b89bb6593f9410d4d`  
		Last Modified: Tue, 04 Mar 2025 21:21:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d0c8cec5173fd4eb593ff4678e08146a08cae721be3deea77b1b0a8a73aa68`  
		Last Modified: Tue, 04 Mar 2025 21:21:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a473d4102287c0ae62320b13f33b8996b9b9299e86d00a1a1f35e3f7b02061d`  
		Last Modified: Tue, 04 Mar 2025 21:21:18 GMT  
		Size: 25.5 MB (25452075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb46df50c3c910bf1ee1fcda9f775710547d98d19a30461f3792420add71ea5`  
		Last Modified: Tue, 04 Mar 2025 21:21:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbfebc121fd4a74c62818b17805c8f8b8f81174ed621343d6c9d3d68c6bf3ee`  
		Last Modified: Tue, 04 Mar 2025 21:21:14 GMT  
		Size: 315.0 KB (315022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7288448e592f2abed8bde531fd14c835c809171c2cfdc19f53b9ba579497af5e`  
		Last Modified: Tue, 04 Mar 2025 21:21:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5abcf8e3a1840584a9c1f95c2df8a9b58945fedcafa96be242badf7aa38974a`  
		Last Modified: Tue, 04 Mar 2025 21:21:26 GMT  
		Size: 82.2 MB (82204599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e44324d5df747e7cb581a5aa53ad8b6f2d1912130f3d867a5f54048b750f1af`  
		Last Modified: Tue, 04 Mar 2025 21:21:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
