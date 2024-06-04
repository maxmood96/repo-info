## `golang:windowsservercore`

```console
$ docker pull golang@sha256:0c071fd458394be584f4211b8c95a62b67a8717c3f386c5730a9004b16ebed6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `golang:windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull golang@sha256:d53b2aaf2204315fa10934220a92bb81899d0b631ffee821780c1258fccbcb97
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2210279642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30af7939d7d1e1f9f68fa40f6ccb91fe90457891a12b5c707963e840fffa1821`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Tue, 04 Jun 2024 20:15:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Jun 2024 20:15:59 GMT
ENV GIT_VERSION=2.23.0
# Tue, 04 Jun 2024 20:16:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 04 Jun 2024 20:16:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 04 Jun 2024 20:16:01 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 04 Jun 2024 20:17:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 04 Jun 2024 20:17:42 GMT
ENV GOPATH=C:\go
# Tue, 04 Jun 2024 20:17:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Jun 2024 20:17:49 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 20:20:18 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 04 Jun 2024 20:20:20 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b13a4609f9a6e3adcd441daf5191d96a3998895e30af09d0a260e4e002486d`  
		Last Modified: Tue, 04 Jun 2024 20:20:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2081caa461ea21161a1b47467b9c1256d3737e9e4036322f041ccdb6e72a1474`  
		Last Modified: Tue, 04 Jun 2024 20:20:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec3a1ed471605d3fb37e95974cbe02328c1e364bbbb27e292aee68b9c60debc`  
		Last Modified: Tue, 04 Jun 2024 20:20:24 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a299e795728d68eaedac4f56df3d877fb5534da2fd4ad258ae0f4f1a7bb0c90`  
		Last Modified: Tue, 04 Jun 2024 20:20:24 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ac08530d390b5c7a5d75f94cabb24d58fd7bcc0c5b71bc0ddd354889774bcf`  
		Last Modified: Tue, 04 Jun 2024 20:20:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccd29d6c43564183f69231e22ab5febf745e6b4d5148a33b590bbde519ac547`  
		Last Modified: Tue, 04 Jun 2024 20:20:27 GMT  
		Size: 25.5 MB (25450276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d365c5c26472e659c20e2c7792d094e723507477c42917c814185fdc9af31`  
		Last Modified: Tue, 04 Jun 2024 20:20:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71b21cef7c30ff1b50336b672ec0e5e171940f7b8a91bbb1ea4ca054bd86fd2`  
		Last Modified: Tue, 04 Jun 2024 20:20:23 GMT  
		Size: 311.3 KB (311321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bf4f9b369a8a62552ce8950d93d80ff972ba25a1afd63b3c4f7a2c3b78e4b3`  
		Last Modified: Tue, 04 Jun 2024 20:20:23 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485309d78fe2de5460898bb4cca36de19d4cce5106d8026560b9656c5800ffde`  
		Last Modified: Tue, 04 Jun 2024 20:20:34 GMT  
		Size: 71.8 MB (71836154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dcf5437ad64c0382df272c9af89272774e8a30ae7f2bb8804b01aff72090c2`  
		Last Modified: Tue, 04 Jun 2024 20:20:23 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull golang@sha256:1cf9b502880bb159934e66d1a9365b2a6e5e2143d826e46e5c52d2e9b2c49369
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2277470988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58669f886d01e15c44f45f11d0fb9ca140bfeabe639aede46a0717d837d9db6f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Tue, 04 Jun 2024 20:15:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Jun 2024 20:15:55 GMT
ENV GIT_VERSION=2.23.0
# Tue, 04 Jun 2024 20:15:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 04 Jun 2024 20:15:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 04 Jun 2024 20:15:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 04 Jun 2024 20:17:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 04 Jun 2024 20:17:32 GMT
ENV GOPATH=C:\go
# Tue, 04 Jun 2024 20:17:53 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Jun 2024 20:17:54 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 20:21:12 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 04 Jun 2024 20:21:13 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d30bb96fb5c036dde09b633b02a41a5867134fdf4a4f98add8eceb5ba261d9`  
		Last Modified: Tue, 04 Jun 2024 20:21:21 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0541f1be0a83a1db5c0035e90a801b4e5659934cf2e3daae11ecd847dbfacd4f`  
		Last Modified: Tue, 04 Jun 2024 20:21:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faccb150265d61ceeb4fbb669ba3fc6425d87bb7b4dd6f239a965947955bfe3`  
		Last Modified: Tue, 04 Jun 2024 20:21:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e58f2843de5db22dfa1b95e86d9e23ad3168e3f13d52b9d0efdbd0eab98457a`  
		Last Modified: Tue, 04 Jun 2024 20:21:19 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780a126a0bbdbfc86550ac7e2c14e40ab07f22dd040df9927b6ae10bf71f97f7`  
		Last Modified: Tue, 04 Jun 2024 20:21:19 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93785b6e93fe7063be8f0d8da78ada458dcab558c6d5cb8deca43dd00995a6`  
		Last Modified: Tue, 04 Jun 2024 20:21:22 GMT  
		Size: 25.6 MB (25594042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b5c3b80469297976f5a4d0d94f6435964481d5b92d10b3d067f705b86c182b`  
		Last Modified: Tue, 04 Jun 2024 20:21:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510cad2b50e086e739fc4d983850f4b52a37199ff4c9286fb54c02a8e7ac6673`  
		Last Modified: Tue, 04 Jun 2024 20:21:18 GMT  
		Size: 356.0 KB (355953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f309c22cd07f0ca0dc3a14bc430f736cf2df275567ffc0aee9749951463bfc`  
		Last Modified: Tue, 04 Jun 2024 20:21:18 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94705bc22d0c7d9f9751fcbc454948d2958fd2ef5f0d6fa93feccb726ac45cdb`  
		Last Modified: Tue, 04 Jun 2024 20:21:29 GMT  
		Size: 71.8 MB (71798965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94221426e35e681ee9b6443461c1a00b0ecfdb34c453aaa2402977f1ce91d121`  
		Last Modified: Tue, 04 Jun 2024 20:21:17 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
