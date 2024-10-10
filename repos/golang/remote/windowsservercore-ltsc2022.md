## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:4c1e2bd5db5605a03b9959f7c810f78f186cd2eb268de014ffeca61d979c0d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull golang@sha256:67fc9f9fdbc9791a990ed4c7884ae6ae0f8307807c13b357441c63e29a427ace
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902581230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35af519f2a81290d7577c119cb68c94f587219186b0f3f207ebc41c769bc3a8d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:00:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:00:01 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:00:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:00:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:00:08 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:00:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:00:29 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:00:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:00:35 GMT
ENV GOLANG_VERSION=1.23.2
# Wed, 09 Oct 2024 23:01:52 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:01:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5ee69cc7a7c00cdf4c7f1dbff132533631d0ad0ceaa5b5ff3db486c5b53c91`  
		Last Modified: Wed, 09 Oct 2024 23:02:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cbbe74f967f0f9a9ef684fce9a9aa625821acdbfe105c34435074aef0d4d18`  
		Last Modified: Wed, 09 Oct 2024 23:02:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf92431dccc391f1ee38a98f1ca77b1097bda8214d7419e6969cb3abf8430c4`  
		Last Modified: Wed, 09 Oct 2024 23:02:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41eaca868705c9e05560d53495acf3d495d0b7a06c6ca9b329fbd507d7d6edea`  
		Last Modified: Wed, 09 Oct 2024 23:02:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba929dd024b4609634374ae5172ba04b23b9a0d30aa37a2b7ca3d881d55c2b6`  
		Last Modified: Wed, 09 Oct 2024 23:01:59 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1298a5450abb7290201ff8c77efe56187bfa7a3ebef66eff603c77c1b506b6fa`  
		Last Modified: Wed, 09 Oct 2024 23:02:02 GMT  
		Size: 25.6 MB (25565156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64778e8a77ed158cfedca607e2abc463e88daa09877472b22079c2d7bb486626`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ce14ff8404e31e6ceaaaaa071eea060149cdb4568c12d3539669a2744c2fff`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 335.7 KB (335731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b91e7a00fd9533319ca369401b4fe2dcefda3dfa70aa511d56ca40081abd57`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd6e8a148665bc2d68668af00265458e6f605be340e500fc302c1c9ca4e7437`  
		Last Modified: Wed, 09 Oct 2024 23:02:09 GMT  
		Size: 77.3 MB (77328388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da972d21cb88b99cb078df72e224aff083f94475d206d2cd1f1536774545cd`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
