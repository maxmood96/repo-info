## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:f8c0aaf5c22398b62a7e56531ae275223784996a8f31b5f216fcdb30692f5a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull caddy@sha256:01d48451603819d5f62407081ac2373062a72b82aedcbcd4e1ee404bdc1cfcc2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3687994635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cdfda788e7a170df24deeb6f0e7a152bf4cc739c23933427a14ed4b4d95fca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 13 Oct 2025 22:34:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 22:34:31 GMT
ENV GIT_VERSION=2.48.1
# Mon, 13 Oct 2025 22:34:32 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Mon, 13 Oct 2025 22:34:33 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Mon, 13 Oct 2025 22:34:34 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Mon, 13 Oct 2025 22:35:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Mon, 13 Oct 2025 22:35:35 GMT
ENV GOPATH=C:\go
# Mon, 13 Oct 2025 22:35:40 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 13 Oct 2025 22:35:40 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 22:36:57 GMT
RUN $url = 'https://dl.google.com/go/go1.25.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc249a599c6fe9d0d4093c363856f6c6320dbbe05e5d5d8818b711fb4a14fc23'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Mon, 13 Oct 2025 22:36:58 GMT
WORKDIR C:\go
# Mon, 13 Oct 2025 23:10:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 23:10:19 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 13 Oct 2025 23:10:19 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 13 Oct 2025 23:10:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 13 Oct 2025 23:10:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 13 Oct 2025 23:10:28 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de816070e98e5429b5b5b08098a2519854cb5273a9e9e20c30044c96f73a2d7`  
		Last Modified: Mon, 13 Oct 2025 22:53:20 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ab90c029098ec9c45312477da41adcdcb4f30b8a60c00570c17ace67b14bc0`  
		Last Modified: Mon, 13 Oct 2025 22:53:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0beb61d08874ce193e0ca10af6b86974d232768058f5547b11901b3224a1ca8`  
		Last Modified: Mon, 13 Oct 2025 22:53:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a909bbea9ca85678606f88408e14798abd03d45664d419aa55ebf6ebaf72a7`  
		Last Modified: Mon, 13 Oct 2025 22:53:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70ad25be99638eb351ab650b35ab29ce87679f813fb45c07d1de6ded3551ce4`  
		Last Modified: Mon, 13 Oct 2025 22:53:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78752c5045ba4d11ba55a9a1f73e04aeffffcd343c3c72998879ae77f78a7a5d`  
		Last Modified: Mon, 13 Oct 2025 22:53:26 GMT  
		Size: 51.2 MB (51243102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d971844854c1e2ad8b5e32a97067dad861a1b7e92221342392f98d76938d2`  
		Last Modified: Mon, 13 Oct 2025 22:53:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4105de880acd6b215be2d7e72d573e1653c58577805f64260cbd28731cf5a6b`  
		Last Modified: Mon, 13 Oct 2025 22:53:22 GMT  
		Size: 365.1 KB (365101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036d6274b9f54097f6a984b8dc41462886add50a1e05c0ca40b16ec6084f1bb5`  
		Last Modified: Mon, 13 Oct 2025 22:53:22 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438dea1181d2420eadd464cca51f645e9700d0486c76ae2a9779d39060a0aab8`  
		Last Modified: Mon, 13 Oct 2025 22:53:27 GMT  
		Size: 62.6 MB (62588429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fa31d9c8590b0f69570d31dd4db2b7514c11d4849a4c08fcc5f5823c9fc148`  
		Last Modified: Mon, 13 Oct 2025 22:53:19 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9894952f59ac6dc850456e39bd1cd6ff1e2544369e90d5679f42ff18b13ffc0c`  
		Last Modified: Mon, 13 Oct 2025 23:10:41 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b53a45457cc11edcff4ba38aa983a1c2c79efbcbdaffeb403bad7908fc990f`  
		Last Modified: Mon, 13 Oct 2025 23:10:41 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1d3991131a5b99cc451d57ddc33248a7cf369178f613ed8ece8eb242e8808c`  
		Last Modified: Mon, 13 Oct 2025 23:10:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa967f4e9a6f94a4c20b28b13c3a89fab62ebc3f811a0e6f01473a86e08184b0`  
		Last Modified: Mon, 13 Oct 2025 23:10:41 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbe8eb8317e9c7409dbdb22c8e15f974a87d1f2df1252fde3586671ef20193e`  
		Last Modified: Mon, 13 Oct 2025 23:10:42 GMT  
		Size: 2.3 MB (2341022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08539cad8d732602a036ed59cf1c78d14e6209a2781497b99d348955226f683e`  
		Last Modified: Mon, 13 Oct 2025 23:10:41 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
