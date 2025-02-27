## `golang:1-windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:22866318b70c7fd085053b676cc4aca28fa1a596108a28918646ce640375223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `golang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull golang@sha256:54a5c144b049c41eb5487db49627900db7c2596b87e152709acda6db3eac9911
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2924772412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e654ce8073d0d5a11d39b8acce5cb561cfcf46e9f4c8b3b0c98a337dfced62e1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:57 GMT
ENV GIT_VERSION=2.23.0
# Thu, 27 Feb 2025 18:18:58 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 27 Feb 2025 18:18:58 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 27 Feb 2025 18:18:59 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 27 Feb 2025 18:19:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 27 Feb 2025 18:19:11 GMT
ENV GOPATH=C:\go
# Thu, 27 Feb 2025 18:19:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 27 Feb 2025 18:19:18 GMT
ENV GOLANG_VERSION=1.24.0
# Thu, 27 Feb 2025 18:20:26 GMT
RUN $url = 'https://dl.google.com/go/go1.24.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '96b7280979205813759ee6947be7e3bb497da85c482711116c00522e3bb41ff1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 27 Feb 2025 18:20:27 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa01ef060faf0141cb578216e54ebc3b6b0155bfbfb5bbe707d5eee9f3e3c73`  
		Last Modified: Thu, 27 Feb 2025 18:20:32 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d40ee8f381c2046ea0cff6dcb06ed80c1a28179127b5db63068b1b2f35ac6b`  
		Last Modified: Thu, 27 Feb 2025 18:20:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2de67d678b054506714272dae90e485d8f71df85b83305528b116591ab4f26`  
		Last Modified: Thu, 27 Feb 2025 18:20:32 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af0f19fa478fdb846beecc69acf48bde9cb60db4f134f9f49166a5f3d38ef6f`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03114f96262ea051cbb2d176480c002cb37e66cb233b330cbb8b315dd2e9bb6`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf728f8d0101bb4eef73d48c00f340d8b2065792a835117702976957591c92f`  
		Last Modified: Thu, 27 Feb 2025 18:20:34 GMT  
		Size: 25.5 MB (25463164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c84bcd0aad3a71df87ebf7f5b2de1dca3073ece8748433ab3d94654cc16db5`  
		Last Modified: Thu, 27 Feb 2025 18:20:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8729c6adede33dcf5f73ef074ed9675bef42767a673482471bd0a2b5f96a4ab2`  
		Last Modified: Thu, 27 Feb 2025 18:20:30 GMT  
		Size: 380.4 KB (380413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610b0879db072c6b6fc28af8957c55d79c78e92a15f1054e09c3cd7afe0ee46`  
		Last Modified: Thu, 27 Feb 2025 18:20:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42620c44c30225fc5b51e3db3e1105ab20dae4e8bf2b3ca2370efef3602c892b`  
		Last Modified: Thu, 27 Feb 2025 18:20:44 GMT  
		Size: 82.3 MB (82330715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97269a605423fa0d317263672cc7aa604a3bfa7c70cef138ccc11c2a9d698b5e`  
		Last Modified: Thu, 27 Feb 2025 18:20:30 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
