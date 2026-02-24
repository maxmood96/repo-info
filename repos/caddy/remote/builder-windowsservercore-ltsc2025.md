## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:12a4274121733b6b007de7f14abace113217cb55daf78d827d9b9ebe83245433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull caddy@sha256:48c15c8bf33e8a643e06d2d594a958292476a0e2d9e2811f07d315b58896d946
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088458263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b465487c17bd47d4b7b5429162cc7d16b2033628f435ca6dd17667eaf72f7aa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:51:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:57:18 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Feb 2026 22:57:18 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Feb 2026 22:57:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Feb 2026 22:57:19 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Feb 2026 22:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 22:57:33 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 22:57:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 22:57:38 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 22:59:03 GMT
RUN $url = 'https://dl.google.com/go/go1.26.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9bbe0fc64236b2b51f6255c05c4232532b8ecc0e6d2e00950bd3021d8a4d07d4'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 22:59:05 GMT
WORKDIR C:\go
# Mon, 23 Feb 2026 20:12:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 20:12:46 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 23 Feb 2026 20:12:47 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:12:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 23 Feb 2026 20:13:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 23 Feb 2026 20:13:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f3641b48551abf691e707ba76f8b07a225d509249237749ad0c13cbcab89a6`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dfafe2e4ec15681b59b09b2ea2f218a811a349d078b2cbaecc126feb929e2b`  
		Last Modified: Tue, 10 Feb 2026 22:59:18 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f90df82fe50dd6b5833a746c782a70988b3984ddf21c090d7d36129fe0f89f0`  
		Last Modified: Tue, 10 Feb 2026 22:59:17 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f052a5d8bf4f2827a95141c0b3c89390a04a735787707ab026025e7a498d313e`  
		Last Modified: Tue, 10 Feb 2026 22:59:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cab7931b4ab9cb79911a3504fff59396a710a90f2c03153fcda4d656c5fd8e5`  
		Last Modified: Tue, 10 Feb 2026 22:59:16 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f3a56265f2532de676a227871566bf54f8aa0026966ec6e24d84ee7a7cbaf`  
		Last Modified: Tue, 10 Feb 2026 22:59:22 GMT  
		Size: 51.2 MB (51219241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec15bdcd174dd912379cd564ff80e30cacf595c1dceb3fa6174646abf3abb717`  
		Last Modified: Tue, 10 Feb 2026 22:59:15 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06e75f82ef8f5b262944577e66118aeb52f772e8651231eeaf6f719423cd29c`  
		Last Modified: Tue, 10 Feb 2026 22:59:15 GMT  
		Size: 343.4 KB (343397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43e1c213d08a1667262b342e75f91b58cc736a17a346da75a58db846e3a068`  
		Last Modified: Tue, 10 Feb 2026 22:59:15 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62d46925baf3f405c1809cda2db6ee089e816de622c99360f77333d1a7bb267`  
		Last Modified: Tue, 10 Feb 2026 22:59:27 GMT  
		Size: 69.8 MB (69801863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445170f32e0feca8c866e6ee97a68bbcd335db232e7dc5a3da15ebd8d60c9f00`  
		Last Modified: Tue, 10 Feb 2026 22:59:15 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f763f15b862a0a070879e91790a15449f306dad7e60536a1e878b80a74b74d3`  
		Last Modified: Mon, 23 Feb 2026 20:14:02 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3d0ffcd67ddc2bc8d9b200475b39504b9da7f3eba241015b57961db42b74ec`  
		Last Modified: Mon, 23 Feb 2026 20:14:01 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6079269b9a7149e343deb96550aeff4a06ca860744224a50cf0928cfa75e54`  
		Last Modified: Mon, 23 Feb 2026 20:14:01 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9424cae5ca245419daa881e820a83a32be0a135b558afcb2c05e70dd3d1bae`  
		Last Modified: Mon, 23 Feb 2026 20:14:01 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c2fc05164e08c5f8db62e3f29230232c5df3a64b6134be54c492378af6eeac`  
		Last Modified: Mon, 23 Feb 2026 20:14:02 GMT  
		Size: 2.3 MB (2316580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ff37c9c2b65a54ed98ad5410cbb4dd721c6378c123893eea1f7a7762461b82`  
		Last Modified: Mon, 23 Feb 2026 20:14:01 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
