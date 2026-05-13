## `golang:windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:6d60aa70512f962bcdd726612ce53cd870c49d0a61cab7ec2e21a63639bc2015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `golang:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull golang@sha256:ec782b7b22ad42aa34cba7d21b6f2956b3e91ca0fbea063dc6c9413ab5347c7d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327478726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c65f7d67dd755aa1fd9ce70ed003fdef4180ed350f8652dd64939f69964dce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:47:14 GMT
ENV GIT_VERSION=2.48.1
# Tue, 12 May 2026 23:47:14 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 12 May 2026 23:47:15 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 12 May 2026 23:47:16 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 12 May 2026 23:47:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:47:32 GMT
ENV GOPATH=C:\go
# Tue, 12 May 2026 23:47:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 May 2026 23:47:38 GMT
ENV GOLANG_VERSION=1.26.3
# Tue, 12 May 2026 23:49:05 GMT
RUN $url = 'https://dl.google.com/go/go1.26.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '20d2ceafb4ed41b96b879010927b28bc92a5be57a7c1801ce365a9ca51d3224a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:49:07 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13a0a1577960fa531425b91d33669fb7199b354c1a80de6a7083edf47fba1a5`  
		Last Modified: Tue, 12 May 2026 23:49:18 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1a06e6db53001adf05747edaaca1741fc4ccec08af2ea774805acf1da39cb9`  
		Last Modified: Tue, 12 May 2026 23:49:17 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5821d5fff8a46fa82ce7615d3b36faaf417a725bee9a0007f85b6ea84f6c0c`  
		Last Modified: Tue, 12 May 2026 23:49:17 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0833fe93928440fd7ff427b2193a37336fc5629eb1ce8feb24d3943d84bdc8d`  
		Last Modified: Tue, 12 May 2026 23:49:17 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcd521987c61ceb33fb79a1c1cdedc0c62a65e6b3676159df971f0c6cacf3cb`  
		Last Modified: Tue, 12 May 2026 23:49:23 GMT  
		Size: 51.2 MB (51239978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b2196ccc04aebc12a61e09bccca2fb14e8fcbbb57c87ed5fc70019f757620c`  
		Last Modified: Tue, 12 May 2026 23:49:15 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b2d7a2af3c6124c96358896cd7aeaa82cefcdd32c5116eeb8172ce4006a4b5`  
		Last Modified: Tue, 12 May 2026 23:49:15 GMT  
		Size: 366.0 KB (366013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181a98e8f044d70822a8f5f715d0d309441bc685621edb1e488c106c45eb0849`  
		Last Modified: Tue, 12 May 2026 23:49:15 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c4f32310d1bd3dd205d4bd6a51f42ccef3e1ad90e011b8e4447840a3b02912`  
		Last Modified: Tue, 12 May 2026 23:49:27 GMT  
		Size: 69.9 MB (69920067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5e90c81dab405fe633f21cf14a67e16b5317cc241b132252fec8653746c6ee`  
		Last Modified: Tue, 12 May 2026 23:49:15 GMT  
		Size: 1.5 KB (1469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
