## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:9eb84a3057694512aba203d547540d3225322b236989b58157385d8fc4b1120f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `golang:1-windowsservercore` - windows version 10.0.26100.32860; amd64

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

### `golang:1-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull golang@sha256:37efb7ae977b3bb35ced546106570515ee011c9151646c0712b14c69db8a0cf2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244047396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8e73d5f1d22986f560c5f1f069164c3e1b6ad993ce431fe46a2c17870cd946`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:52 GMT
ENV GIT_VERSION=2.48.1
# Tue, 12 May 2026 23:50:53 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 12 May 2026 23:50:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 12 May 2026 23:50:55 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 12 May 2026 23:51:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:51:09 GMT
ENV GOPATH=C:\go
# Tue, 12 May 2026 23:51:14 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 May 2026 23:51:14 GMT
ENV GOLANG_VERSION=1.26.3
# Tue, 12 May 2026 23:52:41 GMT
RUN $url = 'https://dl.google.com/go/go1.26.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '20d2ceafb4ed41b96b879010927b28bc92a5be57a7c1801ce365a9ca51d3224a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:52:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72ddab0326e6089ca74907ae3ac383e56049d5df737a07aea5f46d67a27c95`  
		Last Modified: Tue, 12 May 2026 23:39:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c786151110a633b23a3d5a21f6d68fa1c85ce68ee08ef2bdfc5b6063bae53eed`  
		Last Modified: Tue, 12 May 2026 23:52:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2943e972166905753bf6aeb1a45c4c85d10b3ab89d9cc65b6329316ccf931e`  
		Last Modified: Tue, 12 May 2026 23:52:53 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c49d75a1ad63b82f5e3eafbf0c69d418743bbc9fe9695d29af5cfb8fa331f3`  
		Last Modified: Tue, 12 May 2026 23:52:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1803b15b0f5c1e461aaf31398c09ce51da901213b18d89c44358f1ce67a5a1`  
		Last Modified: Tue, 12 May 2026 23:52:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de632000c1f51a8288200e7bd95871971165d705b9bc807d44879ed90d1fa1c3`  
		Last Modified: Tue, 12 May 2026 23:52:59 GMT  
		Size: 51.4 MB (51354733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cdad373139589a9a7f1e20aed9122a11c58a74893f40afaedc05435b6005c1`  
		Last Modified: Tue, 12 May 2026 23:52:51 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c815b70192733d3edbd92533de648fa2f307977af6dd4f5ce5fe4f5dbe64ff`  
		Last Modified: Tue, 12 May 2026 23:52:51 GMT  
		Size: 349.6 KB (349644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2fcb2eb8a1331c4db4075a6a31bc452f100a513231d87ab045018ff2b6d58e`  
		Last Modified: Tue, 12 May 2026 23:52:51 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1760b032a2aec7609f8d0d4d8f235347e97673aee9f43fc3c0971fed2f3c7f`  
		Last Modified: Tue, 12 May 2026 23:53:02 GMT  
		Size: 69.9 MB (69911750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b43d31166ffdff0744efdb2fd7a85c80822f2891fa2e1b9ff392ccabc6eab3e`  
		Last Modified: Tue, 12 May 2026 23:52:51 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
