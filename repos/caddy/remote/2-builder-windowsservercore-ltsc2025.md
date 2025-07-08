## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:ed25ed21d4f58c95d78c4e4be98f0f2ed494f2d1f18b1433597f1072dca7450a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull caddy@sha256:f9a09e3e13f53a87e9584edce29d9fa0cc469cf877ef78f49e5e9a4303403908
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3607842474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002fa6c732fa1a720252d735b3c3a18eb8ec953032cbd0ae4207374d4e282ac1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 08 Jul 2025 18:09:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Jul 2025 18:09:39 GMT
ENV GIT_VERSION=2.48.1
# Tue, 08 Jul 2025 18:09:40 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 08 Jul 2025 18:09:41 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 08 Jul 2025 18:09:42 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 08 Jul 2025 18:09:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 08 Jul 2025 18:09:58 GMT
ENV GOPATH=C:\go
# Tue, 08 Jul 2025 18:10:06 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 08 Jul 2025 18:10:07 GMT
ENV GOLANG_VERSION=1.23.11
# Tue, 08 Jul 2025 18:11:28 GMT
RUN $url = 'https://dl.google.com/go/go1.23.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1dbcf0b4183066550964b22890fe119b0b867b51f12c1eea4445c71494d98cbb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 08 Jul 2025 18:11:30 GMT
WORKDIR C:\go
# Tue, 08 Jul 2025 19:14:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Jul 2025 19:14:00 GMT
ENV XCADDY_VERSION=v0.4.4
# Tue, 08 Jul 2025 19:14:01 GMT
ENV CADDY_VERSION=v2.10.0
# Tue, 08 Jul 2025 19:14:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 08 Jul 2025 19:14:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 08 Jul 2025 19:14:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dd1b479d0f9d99e9f06686f24e2cab290cb5366326ea1f306f2924c44d0b0d`  
		Last Modified: Tue, 08 Jul 2025 19:08:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98a18306c0f1b21b8f6b52f48bc585a20fb711f91c08805537af6cbff66b7ea`  
		Last Modified: Tue, 08 Jul 2025 19:08:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a1d6cad3308d183e27a48ee10c51a21d8a7ab35c64321340ccacbaff416e9e`  
		Last Modified: Tue, 08 Jul 2025 19:08:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e4a88556128a415f1c56547eb80556be555adaf27ddf4dc7cf0cb7f4413450`  
		Last Modified: Tue, 08 Jul 2025 19:08:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adebd78e3f4d7c15c7e880f60c2ddab02ce49f602cecfd1593838cce69b990c`  
		Last Modified: Tue, 08 Jul 2025 19:08:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbb9912aabb5b952e38c170592dcdc420531c8c0c14f70939648177e9b7ccec`  
		Last Modified: Tue, 08 Jul 2025 19:08:19 GMT  
		Size: 51.3 MB (51274970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd99946201dc607dc15204b585f697ffb8f80cabf5d0d27540fcb02f6036f09`  
		Last Modified: Tue, 08 Jul 2025 19:08:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d850602cac507f49df095aff4d9d7d207de087e96bd0830f93c6e687a02fa241`  
		Last Modified: Tue, 08 Jul 2025 19:08:22 GMT  
		Size: 397.8 KB (397755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8345f7e3f27cda4d009ca18b4c2d32f714e001f47b9cdc0b381de424c2f0cd7f`  
		Last Modified: Tue, 08 Jul 2025 19:08:24 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac32eb45e79bad47a34235738c9e70d5dd1419e56c524ffa711c6883604d1caa`  
		Last Modified: Tue, 08 Jul 2025 19:08:35 GMT  
		Size: 77.6 MB (77609966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74a18847eb435eda71e45232037d0e36119b15709bb44e82cb3bcbe85005dd7`  
		Last Modified: Tue, 08 Jul 2025 19:08:26 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e200546a7b287019be75cfdb5f6114341a162c3330d0c693e7a2159d61d6766`  
		Last Modified: Tue, 08 Jul 2025 21:53:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a457dadd0af5b8d144b24b01cca574ee963aabec80d9096d9609d084e1830cbb`  
		Last Modified: Tue, 08 Jul 2025 21:53:08 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524215a35200ca9c288992e151a9ff9f1f5811185a3d64dd51b0c6207ad2baa0`  
		Last Modified: Tue, 08 Jul 2025 21:53:06 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769c4ffff37ae18c206c4e724d46e36950f8d4d7aeb16ad4522c099fc67aac26`  
		Last Modified: Tue, 08 Jul 2025 21:53:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27f00eac43312d36d716b8965ecb8ccc13b3a43da25b02863acc08908ab0092`  
		Last Modified: Tue, 08 Jul 2025 21:53:08 GMT  
		Size: 2.4 MB (2368631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b5abef0338d7ed01036f2a01339d37c6d4155da35401ab19cef9d444807443`  
		Last Modified: Tue, 08 Jul 2025 21:53:08 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
