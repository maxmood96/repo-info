## `golang:windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:586fd40bef38919ba41e900efd1020abfd0bb97fad22e8228c1b400f42bad711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `golang:windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull golang@sha256:13a2f6c37e6eb4876132863c5a0c51b314d23b39005fb27cfc5d24da7da1fd2b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3016934538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79d731dacc5f455dfe287ac3506ba2a2633fe4b5dbd4a7eade29fef5f168141`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:07 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Mar 2025 18:48:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Mar 2025 18:48:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Mar 2025 18:48:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Mar 2025 18:48:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:48:24 GMT
ENV GOPATH=C:\go
# Wed, 12 Mar 2025 18:48:31 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:48:32 GMT
ENV GOLANG_VERSION=1.24.1
# Wed, 12 Mar 2025 18:49:49 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:49:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09532e16aa87511fb49b28bb570f0bb61cbed9cbd50dbfa6411975f535503a0`  
		Last Modified: Wed, 12 Mar 2025 18:49:58 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1a17b843ba71216046788a30fd7a09a76f598c3d48c7fc50145834cba52eab`  
		Last Modified: Wed, 12 Mar 2025 18:49:58 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae00198dd7a1791182679c90ed520a830253d2d123ab45438029aad375a68d1`  
		Last Modified: Wed, 12 Mar 2025 18:49:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74b644228771ee2ecf792ae199af3f8c32f0e127d978fc5adafeb4e72abf32c`  
		Last Modified: Wed, 12 Mar 2025 18:49:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7363130a79a5f52779cae972b6cae82cd7fb7c3634ead57b9e4b885eb9948`  
		Last Modified: Wed, 12 Mar 2025 18:49:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841759932365ab3337665a3293010a8be72b6410601659f134d4d7357954bea`  
		Last Modified: Wed, 12 Mar 2025 18:49:58 GMT  
		Size: 25.5 MB (25471307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4799ef1f8b2a25fcb5a8d153b28227942d46dd185dacd485c2c87795c61ba35f`  
		Last Modified: Wed, 12 Mar 2025 18:49:54 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daa6438e7831cd88e38c8b63d59e604dc5d51aa42dff384936a012a8872456e`  
		Last Modified: Wed, 12 Mar 2025 18:49:54 GMT  
		Size: 363.0 KB (363023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc403de966483b7a4ab49489e49645c95cc37bebd268a93a02d40033b2d46a75`  
		Last Modified: Wed, 12 Mar 2025 18:49:54 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fd0d7ebf47a55b260ba5aa7269b74af473f1fc674abd399a0491f00a916ba9`  
		Last Modified: Wed, 12 Mar 2025 18:50:07 GMT  
		Size: 82.4 MB (82441818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d73e32b1f1214fd7a318e1f403c6cbe0fe593eabe63edd60b1dc933e0c420d`  
		Last Modified: Wed, 12 Mar 2025 18:49:54 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
