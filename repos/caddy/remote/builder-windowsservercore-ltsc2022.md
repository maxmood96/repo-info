## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:91fa965c711f0249c1450f3d078878501854c43d7f1bb51d42b799eb00addc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull caddy@sha256:04a8671661286a80e4610c868e1eeb7aff7b60d6100d7d3383089f905fb53b6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1693784844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42473f1ef295045304e1d90d19d3e1217f74230ecbd6808d9ce4a5ea26516db0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:22:22 GMT
ENV GIT_VERSION=2.48.1
# Fri, 24 Oct 2025 18:22:23 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 24 Oct 2025 18:22:23 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 24 Oct 2025 18:22:24 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 24 Oct 2025 18:22:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:22:43 GMT
ENV GOPATH=C:\go
# Fri, 24 Oct 2025 18:22:48 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 24 Oct 2025 18:22:49 GMT
ENV GOLANG_VERSION=1.25.3
# Fri, 24 Oct 2025 18:24:14 GMT
RUN $url = 'https://dl.google.com/go/go1.25.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc249a599c6fe9d0d4093c363856f6c6320dbbe05e5d5d8818b711fb4a14fc23'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:24:15 GMT
WORKDIR C:\go
# Fri, 24 Oct 2025 19:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 19:24:05 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 24 Oct 2025 19:24:06 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 24 Oct 2025 19:24:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 24 Oct 2025 19:24:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 24 Oct 2025 19:24:20 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a93391da8b89375a0f7b93247893113fff520e2fb182c4f73ef47e4d1d4e63`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd5c7be322fd38b9533ef335e9b0e5df819e13b986fe83f76a512a80e40475c`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6786e5a4ac04385fdfb0ff113da862c41c0d3662ca87a713151fddca4aeefe`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dadfde3ff14e1493314259a59c1b9f0f29b80223f394e57081e1afa7fe9c88`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e682212266a602845029854a1736609104adbc67a13946267f6a9052ec345`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf15a8c8458f6c8c9cade74ab024ed013a031d2b60c6ce5992378dc551953c7`  
		Last Modified: Fri, 24 Oct 2025 18:24:46 GMT  
		Size: 51.4 MB (51360481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432442beaacd749309a5586ab1a2c8391c351bd8202db635b260835ba9969a01`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9cf9c014f47b4134aec4132e1c38b49fc01882fecfef8c2c3d9ffef20b748a`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 347.5 KB (347529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975959d287fe8c25e985eddac22fabdedc6d8650f6b56fc0c098bfd9600b14fe`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fc4f0ebacf94880efcdb5cb1d30bff227452512d0a2b4d22c864e11602436c`  
		Last Modified: Fri, 24 Oct 2025 18:24:47 GMT  
		Size: 62.6 MB (62570208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d17a878e015ba7dbab433f011436cfe4c1d7d17b4637552f8f04f0ef087e6af`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.5 KB (1456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e3928d810d3f251f529be09a7bb0de78b889fa2fdc197d31e21a082154a486`  
		Last Modified: Fri, 24 Oct 2025 19:24:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb83cfef9c0f54333e8406a2ec890cbc814ea8072c57c0936cadec08eaa0f33`  
		Last Modified: Fri, 24 Oct 2025 19:24:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc990bea43a8e365cf9248c5f887251c4c6e943bb95b52cf336d28533a78b72`  
		Last Modified: Fri, 24 Oct 2025 19:24:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19689e2d1d60fed9134109420f9430bfa68f687f271ac187dba7a685ca7fca56`  
		Last Modified: Fri, 24 Oct 2025 19:24:34 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8386ba2121d7e6f7e2ebe0ffb2fbe05c794212321f9abb0340e8fcf7755deabd`  
		Last Modified: Fri, 24 Oct 2025 19:24:36 GMT  
		Size: 2.3 MB (2296411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc52916b65988b2e8bab09ae154248c5ed4207c6f49e3c0e3ddf4f2a933bb8c`  
		Last Modified: Fri, 24 Oct 2025 19:24:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
